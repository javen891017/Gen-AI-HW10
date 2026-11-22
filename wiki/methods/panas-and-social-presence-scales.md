---
title: "PANAS 正負向情感與社會臨場感／心智歸因量表（PANAS, Social Presence & Mind Attribution）"
type: method
tags: [hci, evaluation-method, panas, social-presence, mind-perception, reysen-liking, psychometric-scale]
updated: 2026-11-20
sources: ["Kober et al. (2026)"]
---

# PANAS 正負向情感與社會臨場感／心智歸因量表

## 方法定位與適用階段
在評估對話式 AI 或虛擬化身（Virtual Avatars）的互動體驗時，常需要同時捕捉「使用者自身的情緒變化」、「互動當下的臨場共處感」以及「使用者是否覺得對方有心智」。[Kober et al. (2026)](../sources/kober-2026-ai-awareness-virtual-avatars.md) 整合了以下四套心理計量工具，適合用於受控實驗的前後測與條件比較：

---

## 四大核心量表結構
1. **正負向情感量表（Positive and Negative Affect Schedule, PANAS）**
   - **架構**：20 題 5 點李克特量表，分為 **正向情感（PA, 10 題，如熱情、自豪）** 與 **負向情感（NA, 10 題，如痛苦、恐懼）**。
   - **計算方式**：於每次對話前後施測，計算「互動後分數減去互動前分數」的差值，用來衡量該次人機對話究竟讓使用者心情變好還是變差。
2. **社會臨場感量表（Social Presence Scale）**
   - **出處與調整**：改編自 K. M. Lee 等人（2006）原本用於機器狗 Aibo 的 8 題 10 點量表（0–10 分），測量使用者在對話中感受到「與另一位智慧體共處、連結與互動投入」的程度。
3. **心智／自我概念歸因量表（Perceived Self-Concept / Mind Attribution）**
   - **出處與構面**：採用 Kozak 等人（2006）的三因子架構（7 點李克特量表），測量使用者將人類心智狀態投射到虛擬化身上的程度：
     - **情感（Emotion, 4 題）**：例如「這個對象有能力感受情緒」。
     - **意圖（Intention, 3 題）**：例如「這個對象有能力做出有意圖的行為」。
     - **認知（Cognition, 3 題）**：例如「這個對象具有高度自我覺察」。
4. **喜愛度與信任量表**
   - **修正版 Reysen 喜愛度量表（Modified Reysen-Liking Scale, 11 題, 7 點）**：測量友善度、有趣度與親和力。
   - **AI 信任量表（Trust in AI, Jian et al., 2000）**：選取 3 題測量對自動化／AI 系統的一般性信任。

---

## 課堂小活動建議（15 分鐘）
- **「拆解情感、意圖與認知」**：讓學生用 Kozak 等人（2006）的三個維度（Emotion / Intention / Cognition）去評估自己最常用的 LLM（例如 ChatGPT 或 Claude），討論「為什麼現代人很容易對 AI 歸因高認知（Cognition），卻對情感（Emotion）與自主意圖（Intention）持保留態度？」

---

## 參考文獻與關聯頁面
- 來源論文：[Kober et al. (2026)](../sources/kober-2026-ai-awareness-virtual-avatars.md)
- 理論背景：[擬人化、恐怖谷效應與心智知覺](../concepts/anthropomorphism-and-uncanny-valley.md)
- 相關量表：[RoSAS 機器人社交屬性量表](./rosas-scale.md)、[SUS 與 PETS 量表](./sus-and-pets-evaluation.md)
