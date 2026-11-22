---
title: "McGrath 群體任務環狀模型（McGrath's Group Task Circumplex Model）"
type: concept
tags: [hci, theoretical-framework, task-taxonomy, human-ai-collaboration, mcgrath]
updated: 2026-11-20
sources: ["Lee et al. (2027)"]
---

# McGrath 群體任務環狀模型（McGrath's Group Task Circumplex Model）

## 定義與直覺比喻
**McGrath 群體任務環狀模型（Group Task Circumplex Model）**由社會心理學家 Joseph E. McGrath（1984）提出，用來系統性分類與理解團隊協作任務的認知與行為需求。該模型將群體任務劃分為四大類型（象限）：
1. **發想（Generate）**：構思新點子、腦力激盪與擬定計畫，強調概念發散與創意合作。
2. **選擇（Choose）**：智力決策與問題解決，從多個替代方案中評估並選出最適合的選項。
3. **執行（Execute）**：進行具體行動並產出實際成果（如依步驟製作飲品、體力或操作型任務）。
4. **協商（Negotiate）**：解決衝突、協調不同立場或偏好以達成共識（如家電節能與舒適度的權衡）。

- **教學直覺比喻**：就像你在組隊做專題時會經歷的四種狀態——「一起天馬行空想題目（Generate）」、「投票決定用哪個方案（Choose）」、「分工把成品做出來（Execute）」、「吵架時協調彼此底線（Negotiate）」。

---

## 在人機互動與 Human-AI 協作中的價值
過去許多 HRI 或對話式 AI 評估只用單一任務測試系統表現，容易得出「某種設計全面較好」的過度推論。[Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md) 將 McGrath 模型引入同處一室（Co-located）的家用陪伴機器人實驗，清楚證明了**任務類型會調節 AI 語言策略的有效性**：
- **創意與偏好導向（Generate / Choose）**：使用者重視腦力激盪的夥伴感與個人偏好被理解，因此採用 [溝通調適理論（CAT）](./communication-accommodation-theory.md) 中的「趨同（Convergence）」策略能顯著提高信任感。
- **結果與衝突導向（Execute / Negotiate）**：使用者更在乎步驟正確性、效率與客觀中立，此時「維持（Maintenance）」策略的簡潔精準同樣有效，甚至更顯專業。

---

## 代表性正反案例
- **善用任務分類的設計**：一個智慧居家助理在幫使用者規劃週末派對菜單時（Generate / Choose）能用輕鬆、呼應使用者喜好的語氣聊天；但當使用者在廚房照著食譜切菜或處理爐火警示時（Execute），自動切換為簡短、清晰且無冗言的指令語氣。
- **忽略任務分類的盲點**：若系統在緊急執行或高壓協商情境下，依然學使用者「嗯⋯⋯呃⋯⋯」地停頓並重複口誤，會拖慢節奏並引發不耐或焦慮。

---

## 常見迷思（Misconceptions）
- **迷思：「這四類任務是彼此互斥的，一個系統只能對應其中一種。」**
  - **釐清**：真實的長期人機協作往往會動態穿梭於這四種任務之間，因此重點在於讓 AI 辨識「當下正在進行哪一類任務」，並據此切換互動策略。

---

## 參考文獻與關聯頁面
- 來源論文：[Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md)
- 搭配策略：[溝通調適理論（Communication Accommodation Theory, CAT）](./communication-accommodation-theory.md)
