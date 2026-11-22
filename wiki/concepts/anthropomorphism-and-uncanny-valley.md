---
title: "擬人化、恐怖谷效應與心智知覺（Anthropomorphism, Uncanny Valley & Mind Perception）"
type: concept
tags: [hci, virtual-avatars, anthropomorphism, uncanny-valley, mind-perception, social-presence]
updated: 2026-11-20
sources: ["Kober et al. (2026)"]
---

# 擬人化、恐怖谷效應與心智知覺

## 定義與核心概念
1. **擬人化（Anthropomorphism）**：在人機互動中賦予非人類系統（如聊天機器人、虛擬化身或機器人）人類的外觀特徵、姓名、語音或行為線索，以促進親切感與互動投入（J. Lee & Lee, 2023）。
2. **恐怖谷效應（Uncanny Valley Effect）**：由森政弘（Mori et al., 2012）提出，指當機器人或虛擬角色的外觀與行為「極度接近真人、卻又存在細微破綻」時，會引發使用者強烈的怪異感（Eeriness）與負面情緒。
3. **心智知覺／自我概念歸因（Mind Perception / Self-Concept Attribution）**：使用者將人類才有的心理狀態——包含**情感體驗（Emotion）**、**自主意圖（Intention）**與**高階認知／自我覺察（Cognition）**——投射到人工代理上的程度（Kozak et al., 2006）。
4. **社會臨場感（Social Presence）**：在科技中介環境中，感覺自己「正與另一個有智慧的個體真實共處與交流」的心理感受（Skarbez et al., 2018）。

---

## 來自 Kober et al. (2026) 的設計與理論洞見

### 1. 身分知情會「覆蓋」表面擬人化線索
[Kober et al. (2026)](../sources/kober-2026-ai-awareness-virtual-avatars.md) 發現，即使系統配備了高度擬人化的 3D 動畫化身、唇形同步與自然語音，只要使用者**明確知道對方是 AI**，他們就會意識到「這具人類外殼背後缺乏真實的心智與情感能力」，進而顯著降低對化身的情感歸因、意圖歸因與社會臨場感。換言之，**「外顯的身分標籤」會調節甚至覆蓋視覺擬人化帶來的正面效果**。

### 2. 如何設計出「親切但不恐怖」的 3D 虛擬化身？
為了在擬人化與恐怖谷之間取得平衡，該研究採取了四項具體介面策略，成功讓受試者在互動後負向情緒（Negative Affect）不升反降：
- 採用略帶**卡通／風格化（Comic-like）**的 3D 模型（Ready Player Me），保留可辨識的人工感，不追求照片級逼真。
- 加入微幅**眨眼（Eye-blinking）**與**呼吸起伏（Subtle breathing）**動畫，避免死板僵硬。
- 臉部表情整體保持**中性（Largely neutral）**，僅有極少量的表情模仿，防止出現不自然的誇張扭曲。

---

## 常見迷思（Misconceptions）
- **迷思：「只要把虛擬化身做得越像真人，使用者就越會把它當成有情感的夥伴。」**
  - **釐清**：除了視覺恐怖谷風險之外，Stein & Ohler（2017）指出「心智的恐怖谷（Uncanny Valley of Mind）」——當使用者感覺一個人工代理彷彿擁有獨立意圖與自我意識時，反而可能感到不安；而一旦知道背後是 AI，過於逼真的外觀更容易凸顯「真實感與真實能力的落差」。

---

## 參考文獻與關聯頁面
- 來源論文：[Kober et al. (2026)](../sources/kober-2026-ai-awareness-virtual-avatars.md)
- 相關概念：[LLM 阿諛奉承與身分透明度](./llm-sycophancy-and-identity-transparency.md)
- 相關系統：[EmotiStage 多模態情感演出系統](../systems/emotistage.md)（採風格化情緒化身，而非寫實真人）
- 評估工具：[PANAS 與社會臨場感／心智歸因量表](../methods/panas-and-social-presence-scales.md)
