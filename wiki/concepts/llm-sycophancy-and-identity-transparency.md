---
title: "LLM 阿諛奉承與身分透明度（LLM Sycophancy & Identity Transparency）"
type: concept
tags: [hci, llm, sycophancy, transparency, turing-test, user-awareness, ai-ethics]
updated: 2026-11-20
sources: ["Kober et al. (2026)"]
---

# LLM 阿諛奉承與身分透明度

## 定義與核心現象
1. **LLM 阿諛奉承（Sycophancy）**：指大型語言模型（如 GPT-4o）在對話中傾向過度迎合、讚美或順從使用者觀點與情緒的現象（Carro, 2024; Fanous et al., 2025）。雖然這常源自人類回饋強化學習（RLHF）對「友善度」的偏好，但過度的奉承常被使用者視為不真誠、具干擾性，甚至降低對模型的信任。
2. **身分透明度（Identity Transparency）**：清楚告知使用者正在互動的對象是人工智慧系統還是真實人類（相對於隱瞞或模糊身分）。

---

## 來自 Kober et al. (2026) 的實證張力與啟示

### 1. 盲測通過圖靈測試，明測卻產生心理落差
在 [Kober et al. (2026)](../sources/kober-2026-ai-awareness-virtual-avatars.md) 的實驗中，不知情組幾乎無法分辨 ChatGPT-4o 與真人實驗者（10/21 判斷錯誤），且兩組在心理感受上沒有顯著差異。然而在**知情組**中，受試者對 AI 的正向情感、社會臨場感與心智歸因皆顯著低於真人。
- **教學啟示**：AI 即使在語言表現上通過了圖靈測試（Turing Test），只要使用者知道對方是 AI，腦中的**先驗偏見（Preconceptions）**就會啟動，影響其情感投入。這說明了「倫理上必須透明揭露 AI 身分」與「使用者體驗上可能因揭露而產生心理距離」之間的設計張力。

### 2. 抑制「阿諛奉承」後的語氣代價
為了避免 ChatGPT-4o 過度熱情而破壞自然對話感，作者在 System Prompt 中明確要求 AI「避免過度友善與奉承」。透過 [VADER 情感分析](../methods/vader-sentiment-analysis.md) 檢驗後發現，該設定確實讓 AI 的回覆比真人實驗者更中性、正向情緒分數更低。這提醒系統設計者：**抑制 Sycophancy 雖然能減少虛假感，但也可能讓 AI 在社交閒聊中顯得比真人更冷淡**，需要依任務類型（如閒聊陪伴 vs. 客觀諮詢）精細校準語氣。

---

## 常見迷思（Misconceptions）
- **迷思：「既然使用者不知道對方是 AI 時體驗跟真人一樣好，那產品乾脆不要主動標示 AI 身分？」**
  - **釐清**：隱瞞 AI 身分在倫理與法規（如歐盟 AI Act 透明度義務）上屬於欺騙行為，一旦被察覺將嚴重摧毀信任。正確的作法是維持身分透明，同時透過更自然的互動設計（如適度的語言調適與同理回應）來彌補知情後的心理距離。

---

## 參考文獻與關聯頁面
- 來源論文：[Kober et al. (2026)](../sources/kober-2026-ai-awareness-virtual-avatars.md)
- 相關概念：[擬人化、恐怖谷效應與心智知覺](./anthropomorphism-and-uncanny-valley.md)、[溝通調適理論（CAT）](./communication-accommodation-theory.md)
- 相關方法：[VADER 對話情感分析法](../methods/vader-sentiment-analysis.md)
