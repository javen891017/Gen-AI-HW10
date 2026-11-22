---
title: "AI or human? Exploring the effects of user awareness in conversational dynamics with virtual avatars"
type: source
tags: [hci, virtual-avatars, anthropomorphism, user-awareness, llm, sentiment-analysis, social-presence, mind-perception]
updated: 2026-11-20
sources: ["1-s2.0-S0747563226000816-main.pdf (Kober et al., 2026)"]
---

# AI or human? Exploring the effects of user awareness in conversational dynamics with virtual avatars

## 書目資訊
- **論文標題**：AI or human? Exploring the effects of user awareness in conversational dynamics with virtual avatars
- **作者**：Silvia Erika Kober, Simon Streit, Guilherme Wood（University of Graz, Austria）
- **發表期刊與年份**：*Computers in Human Behavior*, Vol. 181 (2026), Article 108984（2026 年 3 月線上發表）
- **DOI**：`10.1016/j.chb.2026.108984`
- **原始檔案**：待補存於 `raw/papers/`（目前來源為對話上傳之 `1-s2.0-S0747563226000816-main.pdf`）

---

## 一句話教學摘要
透過 42 位女性受試者的 2（身分知情 vs. 不知情）× 2（真人控制 vs. ChatGPT-4o 控制 3D 虛擬化身）混合實驗，發現當使用者「不知情」時幾乎無法分辨對手是真人還是 AI，心理與情緒反應也無差異；但一旦「知情」，對真人控制化身的積極情感、社會臨場感與心智歸因會顯著高於 AI——證實**對 AI 的先驗認知偏見與身分揭露，會覆蓋擬人化外觀帶來的表面效果**。

---

## 核心研究問題與貢獻
1. **檢驗「知情與否（User Awareness）」對高擬人化虛擬化身互動的影響**：過去研究多在純文字聊天機器人上測試，本篇結合 Unity 3D 動畫化身、唇形同步與語音合成（TTS），檢視當互動媒介高度擬人化時，知道「對方是 AI 或真人」是否仍會改變體驗。
2. **區分「客觀對話內容差異」與「主觀心理偏見」**：透過 [VADER 對話情感分析法](../methods/vader-sentiment-analysis.md) 檢查實際對話語氣，證實知情組的主觀感受差異並非因為 AI 回覆品質較差，而是來自使用者內化的預期與刻板印象。
3. **控制實驗混淆變項的示範**：刻意抑制 ChatGPT-4o 的 [阿諛奉承（Sycophancy）](../concepts/llm-sycophancy-and-identity-transparency.md) 傾向，並透過略帶卡通感的視覺設計與微幅動作成功避開 [恐怖谷效應（Uncanny Valley）](../concepts/anthropomorphism-and-uncanny-valley.md)。

---

## 研究方法與關鍵發現

### 實驗設計與系統配置
- **實驗架構**：2（Awareness：知情組 vs. 不知情組，受試者間因子）× 2（Interaction Partner：真人實驗者 vs. ChatGPT-4o，受試者內因子）混合設計。
- **樣本**：**N = 42** 位女性受試者（知情組 21 人、不知情組 21 人；全採女性受試者搭配女性 3D 化身，以排除性別刻板印象干擾）。
- **虛擬場景與對話任務**：以 Unity 與 Ready Player Me 建立固定外觀的 3D 女性化身（搭配 Oculus Lipsync 與 Amazon Polly 語音合成）。每位受試者進行兩段各 15–20 分鐘的日常閒聊（主題為「上一次暑假」與「上一次寒假」，採隨機對抗平衡），分別由另一房間的真人實驗者或 ChatGPT-4o（2024 年 5 月版）即時生成回覆（由實驗者複製貼上以維持一致的回應延遲時間）。
- **評估工具**：
  - [PANAS 正負向情感量表與社會臨場感／心智歸因量表](../methods/panas-and-social-presence-scales.md)（包含 PANAS、Modified Reysen-Liking Scale、Social Presence Scale、Perceived Self-Concept / Mind Attribution、Trust in AI）。
  - [VADER 對話情感分析法](../methods/vader-sentiment-analysis.md)（分析受試者與 AI／真人雙方傳送的文字情緒效價）。

### 主要實證發現
1. **不知情組無法分辨 AI 與真人（通過圖靈測試）**：
   - 不知情組有 **10/21 人**無法正確辨識哪一場是 AI、哪一場是真人（接近隨機猜測水準）。
   - 在不知情組中，與 AI 互動和與真人互動在所有情緒與心理量表上**均無顯著差異**。
2. **知情組出現顯著的「身分認知落差」**：
   - **正向情感（Positive Affect, PANAS）**：在知情組中，與真人互動的正向情感提升顯著高於與 AI 互動（$t(20) = 3.04, p < .01$）。
   - **社會臨場感（Social Presence）**：知情組與真人互動的社會臨場感（60.4）顯著高於與 AI 互動（50.7, $t(20) = 3.17, p < .01$），也顯著高於不知情組的真人互動（47.9, $t(39.99) = 2.67, p < .05$）。
   - **心智歸因（Emotion & Intention Attribution）**：知情組對真人化身歸因的情感（17.2 vs. 10.9, $t(20) = 3.99, p < .01$）與意圖（15.6 vs. 11.9, $t(20) = 4.18, p < .01$）顯著高於 AI 化身；對認知能力（Cognition）的歸因亦呈現知情組高於不知情組的邊緣顯著趨勢（$p = .059$）。
3. **客觀情感分析（VADER）揭示的對話動態**：
   - 不論是否知情，**真人對話的整體正向情緒（Compound 與 Positive Valence）皆高於 AI 對話**（原因之一是實驗刻意在 Prompt 中要求 AI「避免過度熱情與奉承」）。
   - 不論對象是真人還是 AI，**AI／實驗者發出的訊息皆比受試者發出的訊息更正向、更中性**，而受試者表達了較多的負向情緒詞彙。
4. **一般 AI 信任度與恐怖谷**：兩組對 AI 的整體信任度無顯著差異（$p = .77$）；整體負向情感在互動後微幅下降，未觀察到恐怖谷不適現象。

---

## 教學切入點與課堂討論題
1. **「透明揭露 AI 身分，反而讓體驗變差了怎麼辦？」**：討論本研究的核心兩難——倫理上必須告知使用者「這是 AI」（避免欺騙），但知情卻會讓使用者更敏銳地察覺「它只是沒有真實情感的機器」，進而降低社會臨場感與正向情感。AI 介面該如何在「透明揭露」的前提下維持溫暖體驗？
2. **Sycophancy（阿諛奉承）的兩面刃**：作者為了實驗自然度刻意抑制 ChatGPT-4o 的過度討好，結果讓 AI 語氣在 VADER 分析上比真人更不正向。請學生討論：在教學輔導、心理陪伴或日常閒聊場景中，LLM 應該維持「適度平實」還是「高度正向熱情」？
3. **研究方法亮點——「盲測 vs. 明測」與 VADER 雙重驗證**：帶學生欣賞為什麼這篇只靠 42 人就能得出深刻結論——因為「不知情組無差異、知情組有差異」加上「VADER 證實不知情組對話情感其實就有差但人沒感覺」，完美證明了心理體驗落差來自**使用者腦中的先驗偏見**。

---

## 關聯頁面
- 核心概念：[擬人化、恐怖谷效應與心智知覺（Anthropomorphism & Uncanny Valley）](../concepts/anthropomorphism-and-uncanny-valley.md)
- 核心概念：[LLM 阿諛奉承與身分透明度（LLM Sycophancy & Identity Transparency）](../concepts/llm-sycophancy-and-identity-transparency.md)
- 評估方法：[PANAS 正負向情感與社會臨場感／心智歸因量表](../methods/panas-and-social-presence-scales.md)
- 分析方法：[VADER 對話情感分析法](../methods/vader-sentiment-analysis.md)
