# 知識庫操作日誌（Log）

> 本檔案為只增不減（append-only）的時間軸紀錄，記錄每次 `ingest`、`query`（若沉澱為頁面）與 `lint` 的變更摘要。
> 格式範例：`## [YYYY-MM-DD] ingest | <Paper Title>`

## [2026-11-19] init | 初始化人機互動（HCI）LLM Wiki
- 建立 `AGENTS.md`（互動式教學導向、論文 PDF 來源、純標準 Markdown 相對路徑、台灣繁體中文＋中英並列術語、單篇互動式 Ingest）。
- 建立 `raw/` 與 `wiki/` 初始目錄結構、`wiki/index.md` 與本 `wiki/log.md`。

## [2026-11-20] ingest | AI-powered smartphone tools and immigrant social integration. The role of personality and psychological factors
- 新建論文導讀頁：`wiki/sources/mourelatos-2026-ai-m-integration.md`（Mourelatos & Liontou, 2026, *Computers in Human Behavior*）。
- 新建核心概念頁：`wiki/concepts/m-integration.md`、`wiki/concepts/capability-approach.md`、`wiki/concepts/self-determination-theory.md`、`wiki/concepts/psychological-factors-in-ai-adoption.md`。
- 新建研究方法頁：`wiki/methods/ethnosizer-index.md`、`wiki/methods/heckman-selection-model.md`。
- 更新 `wiki/index.md` 索引目錄，所有頁面皆採標準 Markdown 相對路徑互連。

## [2026-11-20] ingest | "Can talking like you make it work?": The role of linguistic convergence and maintenance in human–robot interaction
- 新建論文導讀頁：`wiki/sources/lee-2027-linguistic-convergence-hri.md`（Lee et al., 2027, *Computers in Human Behavior*）。
- 新建核心概念頁：`wiki/concepts/communication-accommodation-theory.md`、`wiki/concepts/mcgrath-task-circumplex.md`、`wiki/concepts/human-error-recovery-in-hri.md`。
- 新建研究方法頁：`wiki/methods/rosas-scale.md`、`wiki/methods/video-based-hri-simulation.md`。
- 更新 `wiki/index.md` 索引目錄，補齊雙向相對路徑連結。

## [2026-11-20] ingest | Choose to think: Nudging towards privacy informed decisions at the app download stage
- 新建論文導讀頁：`wiki/sources/kluetsch-2026-privacy-nudges-app-download.md`（Klütsch et al., 2026, *Computers in Human Behavior*）。
- 新建核心概念頁：`wiki/concepts/digital-nudging-and-dark-patterns.md`、`wiki/concepts/privacy-paradox-and-cognitive-biases.md`、`wiki/concepts/personalized-privacy-assistant.md`。
- 新建研究方法頁：`wiki/methods/experimental-vignette-and-click-dummy.md`、`wiki/methods/bayesian-logistic-regression-separation.md`。
- 更新 `wiki/index.md` 索引目錄與跨文獻連結。

## [2026-11-20] ingest | EmotiStage: Designing an Emotion-Driven Performance System with Multi-modal Generative AI to Support Emotional Awareness
- 新建論文導讀頁：`wiki/sources/wang-2026-emotistage.md`（Wang et al., 2026, *ICMI '26*）。
- 新建知識庫首篇系統頁：`wiki/systems/emotistage.md`。
- 新建核心概念頁：`wiki/concepts/emotional-awareness-and-self-distancing.md`、`wiki/concepts/form-grounded-multimodal-integration.md`。
- 新建研究方法頁：`wiki/methods/sus-and-pets-evaluation.md`、`wiki/methods/s-ders-and-emotion-free-listing.md`。
- 更新 `wiki/index.md` 索引目錄，補齊系統與概念雙向連結。

## [2026-11-20] ingest | AI or human? Exploring the effects of user awareness in conversational dynamics with virtual avatars
- 新建論文導讀頁：`wiki/sources/kober-2026-ai-awareness-virtual-avatars.md`（Kober et al., 2026, *Computers in Human Behavior*）。
- 新建核心概念頁：`wiki/concepts/anthropomorphism-and-uncanny-valley.md`、`wiki/concepts/llm-sycophancy-and-identity-transparency.md`。
- 新建研究方法頁：`wiki/methods/panas-and-social-presence-scales.md`、`wiki/methods/vader-sentiment-analysis.md`。
- 更新 `wiki/index.md` 索引目錄與跨文獻連結。

## [2026-11-20] lint | 健康檢查摘要（32 份檔案）
- **結構與連結檢查**：全數 30 篇內容頁皆已登錄於 `wiki/index.md`，無斷裂相對路徑、無違規 `[[Wikilinks]]`、無孤立頁面。
- **連結強化與缺漏建議**：`bayesian-logistic-regression-separation.md` 與 `experimental-vignette-and-click-dummy.md` 僅有 1 個連入；多篇論文共同提及「AI 信任（Trust in AI）」與「非一體適用（No One-Size-Fits-All）」，建議後續可建立 `concepts/trust-in-ai.md` 與 `syntheses/` 綜合比較頁。
- **原始檔案提醒**：`raw/papers/` 目前尚無 PDF 複本，建議補存 5 篇原文以維持唯讀層完整。

## [2026-11-20] synthesis | 從「一體適用」到「適應性人機互動」
- 整合全部 5 篇論文，建立跨論文綜合與課堂工作坊教案：`wiki/syntheses/adaptive-human-ai-interaction-synthesis.md`。
- 同步更新 `wiki/index.md` 登錄該綜合筆記。

## [2026-11-21] query | 產出「快速打造教育場域 AI 工具」教學簡報
- 依據 `wiki/` 內容（5 篇論文、系統案例與評估工具箱）產出獨立互動式簡報 HTML：`slides/rapid-ai-tool-for-education.html`（共 9 頁，支援鍵盤翻頁、總覽模式與列印成 PDF）。

## [2026-11-22] query | 以 Graph 流程重新產出「快速打造教育場域 AI 工具」簡報
- 依 `AGENTS.md` 第 4.4 節 Graph 流程執行，保存中間產物於 `slides/workspace/rapid-ai-tool-for-education/`（`01-outline.md` 與 `02-slide-content.md`），並於 Human Gate 1 確認後完成 Check Gate 2 與 Check Gate 3（均於第 1/3 次通過）。
- 輸出最終商務淺色微漸層簡報：`slides/rapid-ai-tool-for-education.html`（9 頁，底色 `#f7f8fc`、純白卡片 `#ffffff`、六色章節輪替）。
