---
title: "EmotiStage 多模態情感演出系統"
type: system
tags: [hci, system-architecture, multi-agent, multimodal-ai, affective-computing, vuejs, gpt-4o, dalle3]
updated: 2026-11-20
sources: ["Wang et al. (2026)"]
---

# EmotiStage 多模態情感演出系統

## 系統背景與設計目標
**EmotiStage** 是由 Wang 等人（2026）於 *ICMI '26* 發表的網頁端多模態生成式 AI 系統。它將使用者抽象、難以言喻的個人情緒敘事，轉化為一場包含原創歌詞音樂、視覺舞台背景與雙虛擬化身（Emotion Avatars）演出的「內在劇場（Inner Theater）」，幫助使用者在日常生活中培養更高層次的情緒覺察。

---

## 四大模組與多代理（Multi-Agent）架構

### 1. 引導式情緒探索（Guided Emotional Inquiry —「Control Room」介面）
- **Narrative Construction Agent（敘事建構代理，GPT-4o-2024-11-20）**：透過溫暖、非批判的 3–4 輪對話，依序引導使用者從「客觀事件與情境脈絡」→「身體感受（Somatic Sensations）」→「個人心理意義」。為避免對話疲乏，Prompt 嚴格限制**每輪只問一個問題（One-question-per-turn）**。
- **Emotion Analysis Agent（情緒分析代理）**：將完整對話整理為下游共用的結構化表示法：
  1. **敘事摘要（Narrative Summary）**：保留場景細節、角色與情緒動態。
  2. **雙層情緒標籤（Dual-layer Emotion Tags）**：依據論文提出的**敘事持續性（Narrative Sustainability）**概念，區分定調主軸的**主要情緒（Main Emotion）**（限於持續性情緒：Happiness, Sadness, Anger）與回應敘事衝突的**次要情緒（Secondary Emotion）**（可從 Ekman 六大基本情緒：Happiness, Sadness, Anger, Surprise, Disgust, Fear 中擇一）。

### 2. 情緒音樂創作（Emotional Music Creation —「Rehearsal Studio」介面）
- **Music Prompting Agent**：讀取敘事摘要與雙層情緒標籤，產出符合規範的 JSON 物件，包含貼合故事的**歌詞（Lyrics）**與四項預設聲學參數：**音色（Timbre）、節拍（BPM）、曲風（Genre）、樂器（Instrument）**。
- **使用者校準與 Music Generation Agent**：前端介面會預先填入上述參數，使用者可自由微調後點擊「Finish Rehearsal」，由下游的 **LeVo** 歌詞轉旋律（Lyrics-to-melody）模型生成最終人聲演唱音軌。

### 3. 舞台內容準備（Stage Content Preparation — 並行生成）
在使用者微調音樂的同時，系統背景並行準備三項舞台素材：
- **Backdrop Image Generation Agent**：將敘事摘要轉譯為提示詞，呼叫 **DALL-E 3 API** 生成具象徵氛圍的舞台背景圖。
- **Dialogue Script Generation Agent**：依據雙層情緒標籤生成 6 句、三幕劇結構（衝突 → 發展 → 解決）的 JSON 對話腳本。
- **Avatar Animation Orchestration（規則式動畫編排）**：基於 Ekman 六大基本情緒設計 6 個擬人化情緒化身（採色彩情緒映射，如紅色代表憤怒、藍色代表悲傷）。依據主要情緒選取對應化身與 5 段預先渲染的循環動作影片，並透過音訊播放器的 `timeupdate` 事件將 5 段動作均分同步至整首歌的總長度。

### 4. 內在劇場渲染（Inner Theater Rendering）
前端採用 **Vue.js** 結合 CSS 圖層合成與 **Web Audio API**，將演出分為兩階段：
1. **情緒獨唱舞台（Emotion Solo Stage）**：主情緒化身在 AI 生成的背景前隨音樂演唱並做出對應肢體動作（例如悲傷化身低頭嘆氣搖頭）。
2. **雙情緒對話（Dual-Emotion Dialogue）**：使用者點擊「Trigger Secondary Emotion」後，畫面垂直分割為雙欄，次要情緒化身從右側登場，與主情緒化身演繹一段具戲劇張力的對話，將「內在並存的衝突情緒」外顯為可觀察的舞台對質。

---

## 評估結果與限制
- **定量表現**（N = 13）：SUS 易用性 **81.35**、PETS 科技同理心 **78.37**；使用後 S-DERS 覺察／清晰度顯著提升（$d = 1.53$），自由列舉情緒詞數量顯著增加（$d = 2.90$）。
- **主要限制**：目前依賴預先渲染的 6 種情緒化身動畫與 Ekman 離散情緒分類，尚無法完全捕捉極度細微的情緒光譜；且單次互動尚未支援跨時間的長期情緒記憶與回放（Affective Memory）。

---

## 教學啟示
EmotiStage 是一個極佳的「**LLM 結構化輸出（JSON）＋多代理協作＋多模態前端合成**」教學範例：它展示了如何不用訓練單一端到端巨型模型，就能透過清晰的資料結構（敘事摘要＋雙層情緒標籤）把文字 LLM、音樂生成、圖像生成與預製動畫組裝成具備高度同理心與審美完整度的互動系統。

---

## 關聯頁面
- 來源論文：[Wang et al. (2026)](../sources/wang-2026-emotistage.md)
- 理論機制：[情緒覺察與自我抽離](../concepts/emotional-awareness-and-self-distancing.md)
- 設計原則：[基於形式的多模態整合與控制權委派](../concepts/form-grounded-multimodal-integration.md)
