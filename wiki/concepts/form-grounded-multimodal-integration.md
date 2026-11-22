---
title: "基於形式的多模態整合與控制權委派（Form-Grounded Multi-Modal Integration & Artistic Delegation）"
type: concept
tags: [hci, multimodal-interaction, design-principles, generative-ai, user-agency, affective-computing]
updated: 2026-11-20
sources: ["Wang et al. (2026)"]
---

# 基於形式的多模態整合與控制權委派

## 設計原則一：基於形式的多模態整合（Form-Grounded Multi-Modal Integration）
傳統多模態情感運算（Multimodal Affective Computing）常把文字、聲音、影像視為各自獨立的資訊通道，平行處理後再透過演算法做特徵融合（Feature/Decision Fusion）。[Wang et al. (2026)](../sources/wang-2026-emotistage.md) 指出，這種「拆解再重組」的技術邏輯往往會失落人類情感體驗原本的整體性（Wholeness）。

**基於形式的多模態整合**提出了一種截然不同的設計思考路徑：
- **核心作法**：設計者不應先問「我要選哪些模態、怎麼把檔案拼在一起」，而是先尋找一種**人類文化中原本就具意義的複合形式（Human-meaningful Composite Form）**——例如「劇場（Theater）」、「儀式（Ritual）」或「典禮敘事（Ceremonial Narrative）」——由這個形式本身的內在邏輯來規定每個模態的角色分工，再把生成式 AI 的輸出映射到各個角色上。
- **在 EmotiStage 中的分工範例**：背景圖負責建構「故事場域與氛圍」、歌詞與人聲負責承載「情感基調」、化身動作同步「具身演繹」、雙角色劇本則把矛盾情緒外顯為「戲劇對質」。

---

## 設計原則二：委派藝術渲染以保留情感主體性（Delegating Artistic Rendering to Preserve Emotional Ownership）
在生成式 AI 協作系統中，「使用者該控制多少、AI 又該接手多少」不只是可用性問題，更是深刻影響情感體驗的設計決策：
- **為什麼不能讓使用者全手動創作？**：在過去的 VR 繪畫或音樂創作反思工具中，使用者必須親自負責低階的繪圖、編曲與建模執行，龐大的創作勞動會把注意力從「感受情緒」拉走，轉而陷入「技術操作焦慮」，反而破壞了反思所需的抽離感（Levy et al., 2021）。
- **最佳分工邊界**：
  - **使用者掌控「情感意義與校準」**：提供故事種子（Narrative Seed）、調整高階情緒參數（如節拍 BPM、音色冷暖、曲風）並決定何時觸發次要情緒。
  - **AI 接手「技術與藝術渲染」**：自動生成旋律、背景插畫與角色動畫執行。這不僅保留了使用者對故事的情感主體性（Emotional Ownership），同時讓 AI 產出保有適度的「驚喜感與陌生化」，促成更深層的覺察。

---

## 在 GenAI 介面設計中的教學延伸
這兩項原則非常適合用來檢視各類「人機共創（Human-AI Co-creation）」工具：
- **何時該還給使用者控制權？** 當參數調整本身能促進「自我校準與意義建構」時（如 EmotiStage 讓 12/13 的使用者去調 BPM 與音色）。
- **何時該由 AI 接手？** 當執行細節會造成認知過載、或需要適度「不可控的驚喜」來打破使用者慣性思維時。

---

## 參考文獻與關聯頁面
- 來源論文：[Wang et al. (2026)](../sources/wang-2026-emotistage.md)
- 系統實作：[EmotiStage 多模態情感演出系統](../systems/emotistage.md)
- 心理機制：[情緒覺察與自我抽離](./emotional-awareness-and-self-distancing.md)
