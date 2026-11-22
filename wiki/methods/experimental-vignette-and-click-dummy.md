---
title: "實驗情境與點擊原型法（Experimental Vignette & Click-Dummy Study）"
type: method
tags: [hci, experimental-design, vignette-study, click-dummy, prototyping, usable-privacy]
updated: 2026-11-20
sources: ["Klütsch et al. (2026)"]
---

# 實驗情境與點擊原型法（Experimental Vignette & Click-Dummy Study）

## 方法定位與適用階段
**實驗情境法（Experimental Vignette Methodology）**是透過精心建構的文字與視覺情境描述，讓受試者在高度受控的條件下做出判斷或決策（Atzmüller & Steiner, 2010）。在 HCI 與可用隱私（Usable Privacy）研究中，常搭配**圖片式點擊原型（Image-based Click-Dummy）**模擬真實軟體介面（如 Google Play 商店頁面），讓受試者實際點擊按鈕來測量行為選擇。
- **適用階段**：適合在**介面機制驗證與因果變因隔離（Mechanism Isolation）**階段使用，特別是當真實 App 商店環境難以直接進行 A/B 測試、或想排除真實品牌知名度干擾時。

---

## 執行步驟與嚴謹度設計（以 Klütsch et al., 2026 為例）
1. **設計平衡的虛構介面（Fictional Click-Dummies）**：
   - 為了執行「受試者內（Within-subject）」比較（例如比較商店推薦 vs. 朋友推薦），設計兩款外觀與版型一致但名稱、圖示與開發商不同的虛構 App（如 *Chatland* 與 *InstantChat*），並將「設計版本 × 推薦來源」的呈現順序做對抗平衡（Counterbalancing），排除順序效應。
2. **兩階段行為漏斗紀錄（Two-Stage Behavioral Funnel）**：
   - **Stage 1**：呈現按鈕（安裝 / 不安裝 / 了解更多資料保護），直接記錄受試者的實際點擊行為（而不只是問「你會不會想看隱私政策？」）。
   - **Stage 2**：僅針對點開資訊的受試者動態呈現下一層混合式隱私介面，再記錄最終安裝決策。
3. **搭配歷程追蹤與倫理揭露（Debriefing & Consent）**：
   - 實驗前先隱去「測試隱私推力」的真實研究目的，以避免社會期許偏誤（Social Desirability Bias）；實驗結束後於事後說明頁（Debriefing）完整揭露目的，並讓受試者點擊「確認並儲存資料」才納入分析。

---

## 優點、限制與常見偏誤
- **優點**：
  - 相較純文字問卷，點擊原型能提供更真實的視覺決策空間與行為數據（Behavioral Data）。
  - 能嚴格隔離單一介面元素（如按鈕顏色、文字提示、位置排列）的效果，避免真實 App 的評價星等或品牌濾鏡干擾。
- **限制**：
  - **生態效度（Ecological Validity）限制**：線上模擬環境中沒有真實下載後個資外洩的切身風險，受試者也不會面臨真實社交情境下的同儕壓力（FoMO），因此點擊率可能高於真實場域。
  - **對照組設計的潛在干擾**：若在「對照組」中新增了一個現實 App 商店原本沒有的顯眼按鈕，該按鈕本身就可能產生曝光效應（Mere-Exposure）或位置效應，進而稀釋實驗組與對照組的差異。

---

## 課堂小活動建議（15 分鐘）
- **「抓出對照組的隱形推力」**：展示 [Klütsch et al. (2026)](../sources/kluetsch-2026-privacy-nudges-app-download.md) 的對照組與四種實驗組介面設計（Figure 2），請學生討論：為什麼作者在論文檢討中認為「對照組的按鈕位置本身就是一種推力」？如果要重新設計一個更貼近真實 Google Play 商店的對照組，介面該怎麼改？

---

## 參考文獻與關聯頁面
- 來源論文：[Klütsch et al. (2026)](../sources/kluetsch-2026-privacy-nudges-app-download.md)
- 同類模擬實驗：[情境影片模擬實驗法（Video-Based HRI Simulation）](./video-based-hri-simulation.md)
