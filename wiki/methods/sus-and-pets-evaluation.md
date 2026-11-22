---
title: "系統易用性量表與科技同理心感知量表（SUS & PETS）"
type: method
tags: [hci, evaluation-method, sus, pets, usability, perceived-empathy, psychometric-scale]
updated: 2026-11-20
sources: ["Wang et al. (2026)"]
---

# 系統易用性量表與科技同理心感知量表（SUS & PETS）

## 方法定位與適用階段
在評估具備「情感支持」或「對話陪伴」性質的生成式 AI 系統時，僅測量功能是否好操作是不夠的，還必須了解使用者是否覺得系統「懂我」。[Wang et al. (2026)](../sources/wang-2026-emotistage.md) 在使用後評估（Post-study Evaluation）階段結合了兩套經典與新興的標準化量表：

---

## 1. 系統易用性量表（System Usability Scale, SUS）
- **出處與結構**：由 John Brooke（1996）提出，為 HCI 領域最通用的 10 題（正反向題各半）5 點李克特量表。
- **計分方式**：將各題分數轉換後加總並乘以 2.5，換算為 **0 至 100 分**的總分（需注意 SUS 總分並非百分比，依據 Bangor et al., 2009 的形容詞等級，約 70 分以上屬可接受／Good，80 分以上屬優良）。
- **在 EmotiStage 的應用**：測得平均 **81.35**（SD = 13.05），證明即使串接了對話、音樂、圖像與劇場多階段流程，並未造成過度的認知負荷。

---

## 2. 科技同理心感知量表（Perceived Empathy of Technology Scale, PETS）
- **出處與結構**：由 Schmidmaier 等人（2024）於 *CHI '24* 發表並驗證，專門用來測量使用者主觀感受到「科技系統對自己展現多少同理心」。
- **維度與計分方式**：包含 10 個題項、採 0–101 點滑桿（Slider）評分，分為兩個核心子構面：
  1. **情緒回應性（Emotional Responsiveness, PETS-ER）**：系統是否能敏銳且溫暖地回應使用者的情緒（EmotiStage 得分 80.76）。
  2. **理解與信任（Understanding and Trust, PETS-UT）**：系統是否真正理解使用者的處境並讓人感到可信賴（EmotiStage 得分 74.79；總分 78.37）。

---

## 課堂小活動建議（15 分鐘）
- **「好用 ≠ 懂我」量表對照練習**：請學生回想最近用過的一款 AI 聊天機器人或客服系統，思考「如果一個系統 SUS 拿到 85 分（很好用），但 PETS 只有 40 分，它大概長什麼樣子？」（例如：反應極快、介面簡潔，但回覆制式冷漠、完全沒接住使用者的情緒），藉此理解為什麼情感運算系統需要雙軌評估。

---

## 參考文獻與關聯頁面
- 來源論文：[Wang et al. (2026)](../sources/wang-2026-emotistage.md)
- 系統案例：[EmotiStage](../systems/emotistage.md)
- 其他評估量表：[機器人社交屬性量表（RoSAS）](./rosas-scale.md)、[S-DERS 與情緒自由列舉法](./s-ders-and-emotion-free-listing.md)
