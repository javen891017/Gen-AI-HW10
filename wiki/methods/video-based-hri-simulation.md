---
title: "情境影片模擬實驗法與 LLM 操弄檢驗（Video-Based HRI Simulation & Manipulation Check）"
type: method
tags: [hci, hri, experimental-design, video-simulation, llm-validation, manipulation-check]
updated: 2026-11-20
sources: ["Lee et al. (2027)"]
---

# 情境影片模擬實驗法與 LLM 操弄檢驗

## 方法定位與適用階段
**情境影片模擬實驗法（Video-Based Simulation）**是在真實硬體尚未普及、或需要高度控制變因（如固定語速、停頓秒數、機器人動作與環境光線）時，人機互動（HRI）研究中常用的**受控實驗方法**（Broadbent, 2017）。
- **適用階段**：適合在**原型設計驗證（Early Concept Validation）**與**理論假設檢驗**階段使用，能以低成本安全地測試多種互動腳本與多組受試者。

---

## 執行步驟與嚴謹度設計（以 Lee et al., 2027 為例）
[Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md) 展示了一套結合生成式 AI 工具與雙重驗證機制的標準流程：
1. **高擬真刺激物製作（Stimuli Construction）**：
   - 使用 3D 建模與動畫（Rhino / Keyshot）呈現機器人移動、MidJourney 生成符合受試者文化脈絡的居家客廳／廚房場景、並透過支援情緒與停頓秒數控制的 TTS 服務（Typecast.ai）合成語音。
   - 採用**第一人稱視角（First-person Perspective）**與情境引導提示，讓線上受試者更容易代入主角。
2. **LLM 預實驗腳本驗證（Pre-experimental Validation via GPT-4o）**：
   - 在正式招募人類受試者前，先參考 Chiang & Lee（2023）的作法，讓 GPT-4o 擔任獨立評估者，在各自獨立的對話視窗中依 5 點李克特量表評分：確認 Convergence 腳本分數 > 4、Maintenance 腳本分數 < 2，且四類任務腳本與 McGrath 模型定義高度吻合（> 4）。
3. **注意力檢驗與操弄檢驗（Attention & Manipulation Checks）**：
   - 在主實驗中安插注意力題（例如：「影片中人類發生了什麼口誤？」、「這屬於哪一類任務？」）過濾不專心填答者（該研究從 159 人中篩選出 129 份有效樣本）。
   - 使用配對樣本 t 檢定確認受試者確實能區分兩種 CAT 策略，並用單因子 ANOVA 確認跨任務的策略操弄強度一致。

---

## 優點、限制與常見偏誤
- **優點**：
  - **實驗控制力極高**：能精準控制「2 秒停頓」、「特定口誤詞彙」等細微變因，避免實體機器人現場當機或辨識延遲造成的干擾。
  - **高擴展性**：可透過線上問卷平台快速觸及不同年齡層（如 20–30 歲與 40–50 歲）的較大樣本。
- **限制**：
  - **生態效度與沉浸感限制**：受試者只是「觀看並想像自己互動」，缺乏真實物理共處（Physical Embodiment）與即時語音打斷的臨場壓力。
  - **單一 LLM 評估者的敏感性**：預實驗若只依賴單一 LLM（如 GPT-4o）驗證腳本，結果可能對 Prompt 措辭敏感，且無法計算人類評分者間信度（Inter-rater Reliability），因此仍需搭配正式實驗中的人類操弄檢驗。

---

## 課堂小活動建議（20 分鐘）
- **「低成本 Wizard of Oz / 影片原型」設計**：讓學生分組選定一個還沒做出實體的 AI 互動概念，設計兩段 30 秒的對話腳本（對照組 vs. 實驗組），並討論如何設計 1 個「注意力檢驗題」與 1 個「操弄檢驗題」，確保受試者真的看懂了你想測試的差異。

---

## 參考文獻與關聯頁面
- 來源論文：[Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md)
- 評估工具：[機器人社交屬性量表（RoSAS）](./rosas-scale.md)
