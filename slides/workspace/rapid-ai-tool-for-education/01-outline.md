---
topic: "快速打造教育場域的 AI 工具"
topic_slug: "rapid-ai-tool-for-education"
total_slides: 9
style_spec: "商務淺色微漸層（#f7f8fc 投影片底色 / #ffffff 純白卡片 / 6 色章節輪替）"
check_gate_status: "PASSED (Attempt 1/3)"
updated: 2026-11-22
---

# 階段 1：簡報大綱（Outline）

## 整體敘事弧線
從「為何給了工具卻沒效（起）」→「如何用 Multi-Agent 與控制權切分快速落地（承）」→「對話語氣、外觀透明度與隱私推力的實戰細節（轉）」→「寫程式前後的輕量驗證箱與 5 步檢核清單（合）」。

---

## 逐頁大綱規劃

| 頁碼 | 投影片標題 | 章節主色 | 核心論點 | 建議版型 | 對應 Wiki 來源 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **01** | 快速打造教育場域的 AI 工具 | `cover` (`#01b0ff → #9a6fff`) | 破題點出「從 HCI 實證出發，快速組裝、適應學生、輕量驗證」三大核心目標。 | 封面主標題 + 三欄導覽卡 | `syntheses/adaptive-human-ai-interaction-synthesis.md` |
| **02** | 開發前先想清楚：給了 AI 工具，學生就會用嗎？ | `blue` (`#01b0ff`) | 工具可用不等於能力擴展；心理韌性、自尊、決策風格與年齡造成隱形門檻，必須放棄一體適用。 | 雙欄對照卡 + 底部原則 Callout | `sources/mourelatos-2026-ai-m-integration.md`, `concepts/capability-approach.md`, `concepts/self-determination-theory.md`, `concepts/psychological-factors-in-ai-adoption.md` |
| **03** | 不用從頭訓練模型：Multi-Agent 快速組裝管線 | `purple` (`#9a6fff`) | 借鏡 EmotiStage：以 JSON 中繼表徵串接「每輪一問引導 → 結構化分析 → 多模態並行生成 → 輕量前端合成」。 | 四步驟水平流程管線 + 教育改裝範例 Callout | `systems/emotistage.md`, `sources/wang-2026-emotistage.md` |
| **04** | 多模態整合與「把什麼控制權留給學生」 | `purple` (`#9a6fff`) | 先選定學生熟悉的文化形式（Form-Grounded），再把「意義參數微調」留給學生、「技術渲染」交給 AI 促成自我抽離。 | 雙欄對照卡（左：整合原則 / 右：委派邊界） | `concepts/form-grounded-multimodal-integration.md`, `concepts/emotional-awareness-and-self-distancing.md` |
| **05** | 依教學任務切換 AI 語氣，並溫柔接住學生的口誤 | `teal` (`#4bc0c0`) | 依據 CAT × McGrath 模型：發想／選擇用趨同（Convergence），執行／協商用維持（Maintenance），並結合脈絡保全面子地澄清口誤。 | 四列比較表 + 口誤處理 Callout | `sources/lee-2027-linguistic-convergence-hri.md`, `concepts/communication-accommodation-theory.md`, `concepts/mcgrath-task-circumplex.md`, `concepts/human-error-recovery-in-hri.md` |
| **06** | 虛擬助教的外觀、阿諛奉承與「AI 身分揭露」 | `coral` (`#ff6484`) | 用風格化外觀避開恐怖谷；抑制過度奉承但留意語氣別過冷；明確揭露 AI 身分並以同理引導彌補知情後的心理距離。 | 三欄重點卡 | `sources/kober-2026-ai-awareness-virtual-avatars.md`, `concepts/anthropomorphism-and-uncanny-valley.md`, `concepts/llm-sycophancy-and-identity-transparency.md` |
| **07** | 讓學生真正看懂 AI 隱私風險：兩階段知情推力 | `orange` (`#ff9f3f`) | 拒絕暗黑模式；Stage 1 把隱私按鈕放第一層引發曝光與登門檻效應，Stage 2 用紅綠燈號＋白話說明（Hybrid Nudge）促成知情決策。 | 雙欄階段對照卡（Stage 1 vs. Stage 2） | `sources/kluetsch-2026-privacy-nudges-app-download.md`, `concepts/digital-nudging-and-dark-patterns.md`, `concepts/privacy-paradox-and-cognitive-biases.md`, `concepts/personalized-privacy-assistant.md` |
| **08** | 如何「快速且嚴謹」地驗證你的教育 AI 工具？ | `yellow` (`#ffcd56`) | 寫程式前用 Click-Dummy／影片＋GPT-4o 預檢；上線後結合 SUS、PETS/RoSAS、S-DERS/Free-Listing 與 VADER/統計修正。 | 四階段評估工具箱表格 | `methods/experimental-vignette-and-click-dummy.md`, `methods/video-based-hri-simulation.md`, `methods/sus-and-pets-evaluation.md`, `methods/s-ders-and-emotion-free-listing.md`, `methods/vader-sentiment-analysis.md`, `methods/heckman-selection-model.md` |
| **09** | 打造教育 AI 工具的 5 步快速檢核清單 | `teal` (`#4bc0c0`) | 收斂為 5 步設計檢核與本週即可執行的 3 個最小可行驗證行動。 | 雙欄檢核與行動卡 + 核心心法 Callout | `syntheses/adaptive-human-ai-interaction-synthesis.md` |

---

## Check Gate 1 自動檢查紀錄
- [x] **敘事邏輯連貫性**：起（問題）→ 承（架構與控制權）→ 轉（對話、外觀、隱私）→ 合（驗證與行動清單），結構完整。
- [x] **頁數與節奏**：共 9 頁，單頁只聚焦 1 個核心主題，無過載頁。
- [x] **來源覆蓋度**：完整涵蓋 `wiki/` 內全部 5 篇論文導讀、1 篇系統案例與對應之概念／方法頁。
- **狀態**：通過自動檢查，進入 **Human Gate 1** 等待使用者確認。
