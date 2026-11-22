---
title: "兩階段 Heckman 選擇模型（Two-Step Heckman Selection Model）"
type: method
tags: [hci, quantitative-method, econometrics, sample-selection-bias, heckman-model]
updated: 2026-11-20
sources: ["Mourelatos & Liontou (2026)"]
---

# 兩階段 Heckman 選擇模型（Two-Step Heckman Selection Model）

## 方法定位與適用階段
**兩階段 Heckman 選擇模型**（Heckman, 1976, 1979）是一種計量經濟學與量化研究中用來修正**樣本選擇偏誤（Sample Selection Bias）**的統計方法。
- **適用階段**：屬於實證研究的**資料分析與穩健性檢驗（Robustness Check）**階段。當研究樣本並非隨機抽取，而是經過「自我篩選」才進入分析時（例如：只有擁有智慧型手機、或主動使用特定 App 的人才會出現在 App 使用量的迴歸模型中），就需要使用此方法。

---

## 執行步驟與核心邏輯
在 [Mourelatos & Liontou (2026)](../sources/mourelatos-2026-ai-m-integration.md) 中，作者之所以不只做一般的最小平方法（OLS）迴歸，是因為「會不會用手機」或「會不會用整合 App」本身就可能與年齡、教育程度、健康狀況等未觀測因素有關。兩階段流程如下：
1. **第一階段（Selection Equation 選擇方程式）**：建立機率模型，預測受試者進入特定子樣本的機率（例如：納入性別、年齡、高等教育學歷、移居年數、健康狀態 EQ-VAS 與語言學校出缺席等變數，預測誰會擁有手機並使用 m-Integration App）。
2. **第二階段（Outcome Equation 結果方程式）**：將第一階段估計出的選擇偏差修正項（即 Inverse Mills Ratio）納入主要迴歸模型中，重新估計核心變數（例如人格特質與心理因素）對 AI 應用使用數量的影響，確認結果在排除選擇偏誤後是否依然顯著。

*(註：該論文亦使用 Stata 的 `gtsheckman` 指令進行異質變異數的穩健性檢驗，結果維持一致。)*

---

## 優點、限制與常見偏誤
- **優點**：能有效避免「只看有使用工具的人」所造成的估計偏差，提升研究推論的內部效度（Internal Validity）。
- **限制**：
  - 對第一階段選擇方程式的變數設定較敏感。
  - **無法單獨解決橫斷面資料的反向因果問題（Reverse Causality）**：如論文第 7 節所述，即便修正了樣本選擇偏誤，橫斷面問卷仍無法完全證明是「高自尊促進 AI 使用」還是「使用 AI 提升了自尊」，這仍需透過縱貫追蹤（Longitudinal）或實驗設計來驗證。

---

## 課堂小活動建議（15 分鐘）
- **「倖存者偏誤與選擇偏誤」思辨**：請學生假設自己要研究「使用 AI 寫作助手是否提高學生期末成績」，如果只統計「有主動安裝該 AI 插件的學生」成績，會出現什麼樣的樣本選擇偏誤？（例如：原本就比較積極、數位能力較強的學生才去安裝），並引導他們理解為何需要控制「誰會進入實驗組／使用群體」。

---

## 參考文獻與關聯頁面
- 來源論文：[Mourelatos & Liontou (2026)](../sources/mourelatos-2026-ai-m-integration.md)
- 相關研究方法：[族群融合指標（Ethnosizer Index）](./ethnosizer-index.md)
