---
title: "溝通調適理論（Communication Accommodation Theory, CAT）"
type: concept
tags: [hci, hri, theoretical-framework, communication-accommodation-theory, linguistic-alignment]
updated: 2026-11-20
sources: ["Lee et al. (2027)"]
---

# 溝通調適理論（Communication Accommodation Theory, CAT）

## 定義與直覺比喻
**溝通調適理論（Communication Accommodation Theory, CAT）**由 Howard Giles 等人提出，原本用於解釋人際面對面溝通中，說話者如何根據互動對象的關係、身分與情境，動態調整自己的語言與非語言行為。近年已廣泛延伸至電腦中介溝通（CMC）與人機互動（HRI）領域。

CAT 定義了三種核心調適策略：
1. **趨同（Convergence）**：主動調整自己的詞彙、句法、語速或停頓節奏，向對話夥伴靠攏，以拉近心理距離並建立親和感（Rapport）。
2. **維持（Maintenance）**：保持自己既有的正式或中立溝通風格，不刻意模仿或迎合對方的說話方式。
3. **背離（Divergence）**：刻意強調彼此的語言差異，用來凸顯個人身分或拉開社交距離（多見於衝突或區隔情境）。

- **教學直覺比喻**：就像你在跟長輩聊天時會自動放慢語速、少用網路流行語（趨同），而在擔任客服或播報新聞時會維持標準專業口吻（維持）。

---

## 在人機互動與 LLM 對話設計中的應用
在 [Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md) 的實驗中，作者將 CAT 操作化為機器人回應「人類口誤」的三項具體語言規則：
1. **詞彙與句法對齊（Lexical & Syntactic Alignment）**：趨同組會重複使用使用者的關鍵用詞與句型（如「嗯⋯⋯讓我幫你想想看」）；維持組則使用標準系統模板（「啟動室內風格分析⋯⋯」）。
2. **對話節奏同步（Conversational Pacing）**：趨同組會匹配使用者的猶豫標記與停頓長度（例如 2 秒停頓後再接話）；維持組則保持固定一致的節奏。
3. **錯誤調適方式（Error Accommodation）**：面對口誤（如把「藍椅子」說成「綠椅子」），趨同組會先溫和複述使用者的原話再順勢修正（「你說的綠椅子，是指那張藍色的嗎？」）；維持組則直接以正確資訊澄清（「你是指藍色的椅子嗎？」）。

---

## 代表性正反案例與使用邊界
- **適宜使用趨同（Convergence）的情境**：創意發想（Generate）、個人偏好選擇（Choose）、需要建立陪伴感與降低焦慮的日常對話。實證顯示這能顯著提升溫暖度（Warmth）、勝任感（Competence）與信任感（Trust）。
- **適宜使用維持（Maintenance）的情境**：步驟明確的執行任務（Execute）或利益權衡的協商任務（Negotiate）。在此類結果導向的情境中，過度模仿使用者語氣或猶豫停頓可能顯得不夠專業，反而維持簡潔、精準與中立更有幫助。

---

## 常見迷思（Misconceptions）
- **迷思：「AI 越像人類、越會模仿使用者說話，使用者體驗就一定越好。」**
  - **釐清**：過度的語言趨同（Over-accommodation）或用錯任務情境，反而可能讓使用者覺得 AI 囉唆、不專業甚至刻意討好。理想的 LLM 互動應具備「情境敏感度（Context Sensitivity）」，在感性陪伴與理性效率之間切換策略。

---

## 參考文獻與關聯頁面
- 來源論文：[Lee et al. (2027)](../sources/lee-2027-linguistic-convergence-hri.md)
- 任務分類框架：[McGrath 群體任務環狀模型（McGrath's Group Task Circumplex Model）](./mcgrath-task-circumplex.md)
- 應用情境：[人機互動中的錯誤復原與口誤處理](./human-error-recovery-in-hri.md)
