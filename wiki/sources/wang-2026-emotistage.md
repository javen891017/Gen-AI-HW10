---
title: "EmotiStage: Designing an Emotion-Driven Performance System with Multi-modal Generative AI to Support Emotional Awareness"
type: source
tags: [hci, multimodal-ai, affective-computing, emotional-awareness, generative-ai, multi-agent, icmi26]
updated: 2026-11-20
sources: ["3776574.3831173.pdf (Wang et al., 2026)"]
---

# EmotiStage: Designing an Emotion-Driven Performance System with Multi-modal Generative AI to Support Emotional Awareness

## 書目資訊
- **論文標題**：EmotiStage: Designing an Emotion-Driven Performance System with Multi-modal Generative AI to Support Emotional Awareness
- **作者**：Ziying Wang, Yihong Lin, Xianglin Zhao, Yirui Huang, Ziya Zhou, Wei Xue, Wanling Cai, Yucheng Jin
- **發表會議與年份**：*Proceedings of the 2026 International Conference on Multimodal Interaction (ICMI '26)*, October 5–9, 2026, Napoli, Italy
- **DOI**：`10.1145/3776574.3831173`
- **原始檔案**：待補存於 `raw/papers/`（目前來源為對話上傳之 `3776574.3831173.pdf`）

---

## 一句話教學摘要
這篇論文打造了多模態生成式 AI 系統 [EmotiStage](../systems/emotistage.md)，透過「引導式情緒探索 → 情緒音樂創作 → 內在劇場雙角色演出」的三階段互動，協助使用者從「創作者（Creator）」轉換為「觀眾（Spectator）」，將抽象且交織的混合情緒轉化為可被第三人稱觀察的舞台表演，藉此提升情緒覺察與顆粒度。

---

## 核心研究問題與貢獻
1. **突破單一標籤與純文字反思的限制**：現有數位工具多將情緒簡化為單一標籤或線性文字日記，難以呈現真實生活中同時並存、甚至相互衝突的混合情緒（Mixed Emotions）。
2. **提出「創作者到觀眾（Creator-to-Spectator）」轉換機制**：結合 [情緒覺察與自我抽離（Emotional Awareness & Self-Distancing）](../concepts/emotional-awareness-and-self-distancing.md)，讓使用者先透過對話與音樂參數參與創作，最後退居觀眾席觀看 AI 演出，利用「適度放手控制權」製造審美距離與陌生化效果（Estrangement Effect）。
3. **提出「基於形式的多模態整合（Form-Grounded Multi-Modal Integration）」**：不同於傳統把各模態視為平行獨立通道再做技術融合（Fusion）的作法，主張先選擇一個人類本來就理解的複合文化形式（如「劇場」），由該形式自然定義文字、音樂、背景與虛擬化身動作的分工關係。
4. **實證探索多模態系統的可行性與同理心感知**：透過 N = 13 的探索性混合方法研究，驗證系統在情緒覺察、情緒詞彙豐富度、易用性與感知同理心上的潛力。

---

## 研究方法與關鍵發現

### 探索性混合方法評估（Exploratory Mixed-Methods Study）
- **受試者與流程**：於中國招募 **N = 13** 位大學生／年輕成人（女性 8 人、男性 5 人，19–27 歲），每人攜帶一段願意反思的個人經歷，在獨立安靜環境中進行 50–60 分鐘的自我引導體驗（研究人員於 Zoom 線上待機支援），並於前後測填寫問卷與進行約 22 分鐘的半結構式訪談（採 Braun & Clarke 反思性主題分析）。
- **評估指標**：
  - [情境情緒調節困難量表（S-DERS）與情緒自由列舉法](../methods/s-ders-and-emotion-free-listing.md)（前後測比較）。
  - [系統易用性量表（SUS）與科技同理心感知量表（PETS）](../methods/sus-and-pets-evaluation.md)（後測評估）。

### 主要實證發現
1. **易用性與科技同理心表現良好**：
   - **SUS 平均 81.35**（SD = 13.05，屬「Good」等級），13 人中有 11 人評為容易使用（中位數 5/5）。
   - **PETS 平均 78.37**（SD = 15.31），其中「情緒回應性（PETS-ER）」為 80.76、「理解與信任（PETS-UT）」為 74.79。
2. **情緒覺察與顆粒度顯著提升**（Figure 3）：
   - **S-DERS（Awareness 與 Clarity 子量表）**：使用後顯著改善（$t(12) = 5.53, p < .001, M_{\text{diff}} = 2.15, d = 1.53$）。
   - **情緒詞自由列舉（Free-Listing）**：受試者能辨識出的不同情緒詞數量顯著增加（$t(12) = 10.44, p < .001, M_{\text{diff}} = 2.54, d = 2.90$），顯示情緒顆粒度（Emotional Granularity）提升。
3. **三階段體驗的心理機制**：
   - **階段一（Guided Emotional Inquiry）**：結構化提問作為檢索線索，幫使用者找回被壓力過濾掉的正面片段（如 P4 同時憶起挫敗與 2 萬追蹤者的喜悅），並將模糊的自我歸因轉化為具體情境歸因。
   - **階段二（Emotional Music Creation）**：13 人中有 **12 人主動修改 AI 預設音樂參數**（以 BPM 最多，10/12 人），將調音過程轉化為「這是不是我真正的感受？」的自我校準儀式。
   - **階段三（Inner Theater）**：獨唱與雙情緒虛擬化身對話讓受試者從第一人稱轉為第三人稱旁觀者，重新連結被遺忘的身體感受（如 P3 看到憤怒化身揮拳才意識到自己當時氣到發抖），並看見次要情緒（如 Surprise、Disgust、Fear）與主要情緒的張力。
4. **研究限制**：小樣本（N = 13）單次實驗且無對照組，屬探索性可行性證據而非因果證明；僅聚焦單一事件（Situational EA）而非跨時間的結構性追蹤；角色動畫與六大基本情緒（Ekman）為預先定義素材，細膩度仍有擴充空間。

---

## 教學切入點與課堂討論題
1. **「多代理（Multi-Agent）設計如何服務情感體驗？」**：帶學生拆解 [EmotiStage](../systems/emotistage.md) 的 6 個 AI 代理如何透過結構化 JSON 協作，特別討論「為何對話代理要嚴格限制每輪只問一個問題（One-question-per-turn）？」以及「為何把音樂、繪圖、劇本交給不同代理並行處理？」。
2. **「失去控制權」也能是一種設計資源？**：對照一般 HCI 強調「使用者完全掌控（User Control）」，討論為什麼在情緒覺察系統中，適度把藝術渲染與演出控制權交給 AI，反而能創造有助於自我反思的「陌生化距離」。
3. **Form-Grounded 設計練習**：如果要設計一個幫助大學生處理「期末考或畢業焦慮」的多模態 GenAI 系統，除了「劇場」之外，還有哪些人類熟悉的複合文化形式（例如：廣播電台節目、展覽策展、漫畫分鏡、書信往返）可以用來統整多模態輸出？

---

## 關聯頁面
- 系統架構詳解：[EmotiStage 多模態情感演出系統](../systems/emotistage.md)
- 核心概念：[情緒覺察與自我抽離（Emotional Awareness & Self-Distancing）](../concepts/emotional-awareness-and-self-distancing.md)
- 設計原則：[基於形式的多模態整合與控制權委派（Form-Grounded Multi-Modal Integration）](../concepts/form-grounded-multimodal-integration.md)
- 評估方法：[SUS 與科技同理心感知量表（SUS & PETS）](../methods/sus-and-pets-evaluation.md)、[S-DERS 與情緒自由列舉法（S-DERS & Emotion Free-Listing）](../methods/s-ders-and-emotion-free-listing.md)
