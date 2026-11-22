---
title: "\"Can talking like you make it work?\": The role of linguistic convergence and maintenance in human–robot interaction"
type: source
tags: [hci, hri, companion-robots, communication-accommodation-theory, error-recovery, mixed-methods, rosas]
updated: 2026-11-20
sources: ["1-s2.0-S0747563226002487-main.pdf (Lee et al., 2027)"]
---

# "Can talking like you make it work?": The role of linguistic convergence and maintenance in human–robot interaction

## 書目資訊
- **論文標題**："Can talking like you make it work?": The role of linguistic convergence and maintenance in human–robot interaction
- **作者**：Jeongmin Lee, Sukyung Yoon, Hyorim Shin, Junho Choi（延世大學，Yonsei University）
- **發表期刊與年份**：*Computers in Human Behavior*, Vol. 187 (2027), Article 109151（2026 年 8 月線上發表）
- **DOI**：`10.1016/j.chb.2026.109151`
- **原始檔案**：待補存於 `raw/papers/`（目前來源為對話上傳之 `1-s2.0-S0747563226002487-main.pdf`）

---

## 一句話教學摘要
這篇研究透過 2 × 4 × 2 混合設計情境影片實驗（N = 129），探討家用陪伴機器人在面對**人類口誤（Slips of the Tongue）**時，採用「語言趨同（Convergence）」或「語言維持（Maintenance）」策略如何隨任務類型與使用者年齡影響信任感與社交評價，並提出陪伴機器人的三大質性特質：協同效應（Synergy）、愉悅感（Enjoyment）與主動性（Proactivity）。

---

## 核心研究問題與貢獻
1. **研究視角翻轉**：過去 [人機互動中的錯誤復原（Error Recovery in HRI）](../concepts/human-error-recovery-in-hri.md) 研究多半處理「機器人自己犯錯」，本篇將焦點轉向「機器人如何以語言策略回應**人類發起的口誤**」。
2. **驗證語言調適策略的任務邊界**：依據 [溝通調適理論（Communication Accommodation Theory, CAT）](../concepts/communication-accommodation-theory.md) 設計「趨同」與「維持」兩種語言策略，並透過 [McGrath 群體任務環狀模型（McGrath's Group Task Circumplex Model）](../concepts/mcgrath-task-circumplex.md) 區分四類日常任務，證明「模仿使用者說話」並非在所有情境下都比較好。
3. **揭露年齡與任務脈絡的交互作用**：發現不同世代（20–30 歲 vs. 40–50 歲）對創意任務與執行任務的信任感與不適感截然不同，為多世代家庭的適應性對話設計提供實證依據。
4. **擴展陪伴機器人（Companion Robots）概念**：從 319 則開放式回饋中歸納出使用者期待家用機器人具備的三大特質——**協同效應（Synergy）、愉悅感（Enjoyment）與主動性（Proactivity）**。

---

## 研究方法與關鍵發現

### 實驗設計與刺激材料
- **實驗架構**：2（CAT 策略：Convergence vs. Maintenance，受試者內因子）× 4（任務類型：Generate, Choose, Execute, Negotiate，受試者間因子）× 2（年齡層：20s–30s vs. 40s–50s，受試者間因子）混合因子設計。
- **樣本規模**：最終有效樣本 **N = 129**（女性 70 人、男性 59 人，平均年齡 37.98 歲），其中 20–30 歲組 75 人、40–50 歲組 54 人。
- **刺激材料與操弄檢驗**：採用 [情境影片模擬實驗法（Video-Based HRI Simulation）](../methods/video-based-hri-simulation.md)，以 3D 渲染模擬類似 Samsung Ballie 的非人形家用機器人「Milo」，並運用 GPT-4o 進行預實驗腳本操弄檢驗（Pre-experimental Validation）。對話中刻意植入韓語常見的音韻或語意替換型口誤（如將「藍椅子」說成「綠椅子」、將「暖氣溫度」說成「冷氣溫度」）。
- **評估指標**：
  - **信任（Trust）**：2 題 5 點李克特量表（Cronbach's α = .784）。
  - **社交屬性評價**：採用 [機器人社交屬性量表（RoSAS）](../methods/rosas-scale.md)，測量溫暖度（Warmth, α = .878）、勝任感（Competence, α = .845）與不適感（Discomfort, α = .869）。
  - **質性內容分析**：針對實驗後開放式問答共 319 則回應進行歸納編碼。

### 主要實證發現
1. **CAT 策略的整體優勢與任務依賴性**：
   - **主效果**：整體而言，趨同策略（Convergence）在**信任**（M = 4.00 vs. 3.90, p = .046）、**溫暖度**（M = 3.39 vs. 2.95, p < .001）與**勝任感**（M = 4.07 vs. 3.87, p = .001）皆顯著高於維持策略（Maintenance）。
   - **策略 × 任務交互作用（Trust）**：趨同策略對信任的顯著提升**僅發生在 Generate（p = .046）與 Choose（p = .016）任務**；在講求效率、步驟精確或衝突解決的 **Execute 與 Negotiate** 任務中，維持中立正式語氣的 Maintenance 策略與趨同策略表現相當，甚至有受試者認為直接精準說明更值得信賴。
2. **年齡與任務類型的交互作用（Task × Age）**：
   - **創意發想（Generate）任務**：20–30 歲組的信任度顯著高於 40–50 歲組（M = 3.93 vs. 3.19, p = .007），而 40–50 歲組在此任務的不適感（Discomfort）顯著高於年輕組（M = 2.03 vs. 1.51, p = .032）。
   - **步驟執行（Execute）任務**：反而是 20–30 歲組的不適感顯著高於 40–50 歲組（M = 2.04 vs. 1.49, p = .021）。
   - **溫暖度（Warmth）的年齡差異**：兩個年齡層都認為趨同策略較溫暖，但年輕族群的差距幅度更為明顯（p < .001 vs. p = .0499）。
3. **研究限制**：採影片模擬而非實體機器人互動（生態效度受限）、僅限單一使用者與韓國文化樣本、未納入 60 歲以上高齡族群、且每類任務僅由單一情境代表。

---

## 教學切入點與課堂討論題
1. **「AI 講話像你，就一定比較好嗎？」**：請學生對照 Table 1（Generate 任務）與 Table 11–12（Execute / Negotiate 任務）的對話腳本，討論為什麼在「討論客廳裝潢」時學人語氣會增加信任，但在「廚房做果汁」或「協商省電」時，太像人類口吻反而可能顯得不夠專業？
2. **Prompt Engineering 實作練習**：讓學生為 LLM 驅動的語音助手撰寫兩版 System Prompt——一版執行「Convergence（複述口誤並順暢改寫、匹配停頓節奏）」，另一版執行「Maintenance（中性精準澄清）」，並設計觸發切換的任務判斷規則。
3. **跨論文連結討論**：結合 [Mourelatos & Liontou (2026)](./mourelatos-2026-ai-m-integration.md) 的發現，討論「使用者的心理特質（如高神經質或低自尊）」與「機器人的語言策略（Convergence vs. Maintenance）」之間可能存在什麼樣的交互影響？

---

## 關聯頁面
- [溝通調適理論（Communication Accommodation Theory, CAT）](../concepts/communication-accommodation-theory.md)
- [McGrath 群體任務環狀模型（McGrath's Group Task Circumplex Model）](../concepts/mcgrath-task-circumplex.md)
- [人機互動中的錯誤復原與口誤處理（Error Recovery & Slips of the Tongue）](../concepts/human-error-recovery-in-hri.md)
- [機器人社交屬性量表（Robotic Social Attributes Scale, RoSAS）](../methods/rosas-scale.md)
- [情境影片模擬實驗法（Video-Based HRI Simulation）](../methods/video-based-hri-simulation.md)
