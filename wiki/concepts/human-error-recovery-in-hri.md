---
title: "人機互動中的錯誤復原與口誤處理（Error Recovery & Slips of the Tongue in HRI）"
type: concept
tags: [hci, hri, error-recovery, human-error, slips-of-the-tongue, llm-dialogue]
updated: 2026-11-20
sources: ["Lee et al. (2027)"]
---

# 人機互動中的錯誤復原與口誤處理

## 核心概念與問題意識
在真實的人機互動中，溝通失敗（Communication Breakdowns）是常態而非例外。傳統 [人機互動（HRI）](../sources/lee-2027-linguistic-convergence-hri.md) 錯誤復原研究幾乎都聚焦在**「機器人犯錯後該怎麼道歉或補救」**（Robot-generated Errors），例如系統辨識失敗、動作失誤後給予道歉、解釋原因、補償或幽默化解。

然而，[Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md) 指出了另一個長期被忽略的面向：**人類發起的語言錯誤（Human-generated Verbal Errors）**，特別是日常對話中最常見的**口誤（Slips of the Tongue）**。

---

## 什麼是口誤（Slips of the Tongue）？
根據 Honig & Oron-Gilad（2018）的人為錯誤分類，人類錯誤可分為失誤（Mistakes）、**口誤／疏失（Slips）**、遺漏（Lapses）與蓄意違規（Intentional Violations）。其中 **Slips of the Tongue** 是指說話者在規劃與產出語句的瞬間發生短暫失誤，導致說出非本意的詞彙（例如 Kim, 2010 指出最常見的是「替換型錯誤 Substitution」）：
- **音韻替換（Phonological Substitution）**：誤說成發音相近的詞（如韓語的「冷氣 *naengbang*」說成「暖氣 *nanbang*」，或「奇異果 *kiwi*」說成「羽衣甘藍 *keil*」）。
- **語意替換（Semantic Substitution）**：誤說成意義相近或同類別的詞（如看著「藍椅子」卻說成「綠椅子」，或把「大蔥」說成「青蔥」）。

---

## LLM 時代的錯誤復原轉變
在過去規則式語音助理時代，系統遇到口誤往往只能照字面執行錯誤指令，或冷冰冰地回覆「找不到綠椅子」。進入大型語言模型（LLM）與多模態感測時代後，AI 系統有能力結合環境脈絡（如視覺確認現場只有藍椅子、IoT 確認暖氣正開啟中）推論使用者的真實意圖（Speech Act），並透過兩種關鍵機制完成復原：
1. **意圖推論與主動澄清**：不盲從錯誤字面，而是利用環境線索禮貌確認。
2. **社交層面的「保全面子」與關係維繫**：如 [Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md) 的質性結果所示，當機器人用自然且不傷人自尊的「趨同（Convergence）」語氣糾正口誤時，使用者不會覺得被指責，反而會感受到被關心（類似「熟識的朋友」），進而提升信任感與協同體驗。

---

## 常見迷思（Misconceptions）
- **迷思：「只要系統語音辨識（ASR）準確率夠高，就不會有溝通錯誤。」**
  - **釐清**：即使 ASR 一字不漏地聽對了使用者說出的字，如果使用者自己「說錯詞（口誤）」，系統仍會面臨字面與意圖不符的挑戰。這正是現代對話式 AI 必須結合上下文語意與社交溝通策略的原因。

---

## 參考文獻與關聯頁面
- 來源論文：[Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md)
- 語言策略：[溝通調適理論（Communication Accommodation Theory, CAT）](./communication-accommodation-theory.md)
- 任務脈絡：[McGrath 群體任務環狀模型](./mcgrath-task-circumplex.md)
