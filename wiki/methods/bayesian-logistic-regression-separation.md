---
title: "處理分離現象的貝氏邏輯迴歸（Bayesian Logistic Regression for Separation）"
type: method
tags: [hci, quantitative-method, bayesian-statistics, logistic-regression, separation, brms]
updated: 2026-11-20
sources: ["Klütsch et al. (2026)"]
---

# 處理分離現象的貝氏邏輯迴歸（Bayesian Logistic Regression for Separation）

## 方法定位與問題背景
在 HCI 實驗中，當結果變數是二元選擇（例如：`0 = 不安裝` vs. `1 = 安裝`）時，研究人員通常會使用傳統頻率學派（Frequentist）的邏輯迴歸（Logistic Regression）。

然而，如果某個實驗操弄非常強烈，導致預測變數幾乎完全區分了結果——例如在 [Klütsch et al. (2026)](../sources/kluetsch-2026-privacy-nudges-app-download.md) 的第二階段中，看到「低隱私評分」的人幾乎都不安裝（僅 1.64%–5.36% 安裝），看到「高隱私評分」的人幾乎都安裝（86.21%–88.52% 安裝）——數據就會出現**完全分離或幾近完全分離（Complete / Quasi-Complete / Almost Perfect Separation）**。

此時傳統最大概似估計（MLE）會崩潰，產生**極度膨脹的迴歸係數（$\beta$）與標準誤（Standard Errors）**，甚至無法收斂。**貝氏邏輯迴歸（Bayesian Logistic Regression）**搭配**弱資訊先驗分布（Weakly Informative Priors）**正是解決此問題的標準統計解法（Gelman et al., 2008）。

---

## 執行步驟與判讀要點（以 Klütsch et al., 2026 為例）
1. **設定弱資訊先驗分布（Weakly Informative Priors）**：
   - 弱資訊先驗不會主導最終結果，但能對極端參數空間給予溫和約束，防止係數發散至無限大（該研究設定截距 $\alpha \sim \text{Normal}(0, 10)$、斜率 $\beta \sim \text{Normal}(0, 5)$）。
2. **使用 MCMC 取樣與收斂診斷**：
   - 使用 R 語言的 `brms` 套件（底層為 Stan），跑 4 條鏈（Chains）、各 2,000 次迭代（含 1,000 次暖身 Warm-up）。
   - 檢驗收斂指標：有效樣本數（bulk-ESS 與 tail-ESS > 2,000）、Gelman–Rubin 診斷值 $\hat{R} = 1.00$，以及檢視跡線圖（Trace Plots）與自相關圖。
3. **以 95% 可信區間（Credible Interval, CrI）取代 p 值判讀**：
   - 貝氏架構不依賴傳統 $p < .05$ 顯著性檢定，而是檢視參數的 **95% 可信區間（95% CrI）是否包含 0**。若 95% CrI 完全排除 0（例如高隱私評分的 $\beta = 12.27$，95% CrI = [7.69, 18.21]），即認定該變項對結果具有實質影響。

---

## 優點與注意事項
- **優點**：
  - 在小樣本或出現極端分離（Separation）的二元決策數據中依然穩健收斂。
  - **95% 可信區間（CrI）的機率解釋更直覺**（直接代表真實參數落於該區間的 95% 機率），相較傳統信賴區間更容易正確解讀（Morey et al., 2016）。
- **注意事項**：
  - 需明確報告先驗分布的設定理由，並進行先驗與後驗分布的敏感度／密度比較，確認數據本身對後驗估計提供了充分資訊。

---

## 課堂小活動建議（15 分鐘）
- **「效果太好反而算不出來？」**：讓學生思考一個直覺悖論——為什麼當「低隱私組 0 人安裝、高隱私組 50 人安裝」這種效果最明顯的時候，傳統邏輯迴歸反而會報錯或得出荒謬的標準誤？藉此帶出「完全分離（Separation）」的幾何意義與貝氏先驗約束的直覺。

---

## 參考文獻與關聯頁面
- 來源論文：[Klütsch et al. (2026)](../sources/kluetsch-2026-privacy-nudges-app-download.md)
- 其他量化方法：[兩階段 Heckman 選擇模型](./heckman-selection-model.md)
