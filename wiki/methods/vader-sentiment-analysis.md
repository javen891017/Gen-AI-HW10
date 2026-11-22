---
title: "VADER 對話情感分析法（VADER Sentiment Analysis）"
type: method
tags: [hci, text-analysis, sentiment-analysis, vader, nlp, mixed-methods]
updated: 2026-11-20
sources: ["Kober et al. (2026)"]
---

# VADER 對話情感分析法（VADER Sentiment Analysis）

## 方法定位與適用階段
**VADER（Valence Aware Dictionary and Sentiment Reasoner）**是由 Hutto 與 Gilbert（2014）開發的規則與詞典式情感分析工具，原本針對社群媒體短文本設計，因為無須額外標註訓練資料且具備語氣強度（如驚嘆號、程度副詞、否定詞）的規則處理，在 HCI 領域常被用來作為**對話逐字稿的客觀情感指標**，與受試者的主觀問卷互相對照。

---

## 核心輸出指標（以 Kober et al., 2026 為例）
在 R 語言的 VADER 套件中，分析每則訊息會輸出四個指標：
1. **Compound（綜合情感分數）**：正規化至 **$-1$（極負向）至 $+1$（極正向）** 的整體情感指標。
2. **Pos（正向情感比例）**：訊息中帶有正向效價詞彙的比例。
3. **Neu（中性情感比例）**：訊息中屬於中性語氣的比例。
4. **Neg（負向情感比例）**：訊息中帶有負向效價詞彙的比例。

### 在人機對話實驗中的關鍵用法
[Kober et al. (2026)](../sources/kober-2026-ai-awareness-virtual-avatars.md) 示範了一個極具價值的分析設計——**將「系統／實驗者發出的訊息」與「受試者發出的訊息」分開計算 VADER 分數**，進行 2（知情與否）× 2（真人 vs. AI）× 2（傳送者 vs. 接收者）的三因子變異數分析，藉此回答兩個重要問題：
- 主觀問卷的體驗落差，究竟是因為 AI 講話客觀上比較冷淡，還是使用者心理偏見所致？
- 人類受試者在與 AI 對話時，是否會出現與面對真人不同的用詞情緒傾向？

---

## 優點、限制與注意事項
- **優點**：輕量、可重現性高、不需昂貴算力，且能提供獨立於自陳式問卷之外的客觀行為文本證據。
- **限制與注意事項**：
  - 詞典式方法對反諷（Sarcasm）、高度依賴上下文的隱喻或非英語系語言（若未經適當翻譯或本地化詞典）準確率較低。
  - 在小談話（Small talk）語境下，大多數日常語句會落在中性區間（如該研究中 Neu 約佔 0.85–0.89），解讀時應關注組間相對差異而非絕對值。

---

## 參考文獻與關聯頁面
- 來源論文：[Kober et al. (2026)](../sources/kober-2026-ai-awareness-virtual-avatars.md)
- 相關概念：[LLM 阿諛奉承與身分透明度](../concepts/llm-sycophancy-and-identity-transparency.md)
