# 人機互動（HCI）互動式教學 LLM Wiki

本專案是一個以**人機互動（Human-Computer Interaction, HCI）**為主題的個人化／教學用 **LLM Wiki 知識庫**，參考 Andrej Karpathy 的 LLM Wiki 架構設計，由使用者負責挑選文獻與把關方向，AI Agent 負責將論文 PDF 編譯為結構化、可跨頁互連且適合**互動式教學**的持久性知識網絡，並透過 **Graph 式簡報製作流程**產出教學投影片。

---

## 專案目錄結構

```text
GAI_10/
├── README.md                 # 本專案說明文件
├── AGENTS.md                 # 知識庫與簡報生產的操作規範（Schema）
├── raw/                      # 【唯讀層】原始論文 PDF 與圖表素材
│   ├── README.md
│   ├── papers/
│   └── assets/
├── wiki/                     # 【維護層】純標準 Markdown 知識庫（不使用 Obsidian）
│   ├── index.md              # 內容分類導覽目錄
│   ├── log.md                # 時間軸操作紀錄（append-only）
│   ├── sources/              # 論文精讀與教學導讀（5 篇）
│   ├── concepts/             # 核心理論與概念（14 篇）
│   ├── methods/              # 研究設計與評估方法（10 篇）
│   ├── systems/              # 代表性系統與架構案例（1 篇）
│   └── syntheses/            # 跨論文綜合比較與教案（1 篇）
└── slides/                   # 【簡報輸出層】教學簡報與 Graph 中間產物
    ├── workspace/            # 各主題大綱（01-outline.md）與逐頁內容（02-slide-content.md）
    └── rapid-ai-tool-for-education.html
```

---

## 目前收錄內容與快速導覽

完整目錄請見 [wiki/index.md](./wiki/index.md)，最新異動紀錄請見 [wiki/log.md](./wiki/log.md)。

### 1. 已匯入論文（Sources）
- [Mourelatos & Liontou (2026)](./wiki/sources/mourelatos-2026-ai-m-integration.md) — AI 行動應用與個人心理特質對移民社會融合的影響（N = 748）
- [Lee et al. (2027)](./wiki/sources/lee-2027-linguistic-convergence-hri.md) — 家用陪伴機器人面對人類口誤時的 CAT 語言策略與任務／年齡交互作用（N = 129）
- [Klütsch et al. (2026)](./wiki/sources/kluetsch-2026-privacy-nudges-app-download.md) — App 下載階段的兩階段隱私推力與混合式隱私量表實驗（N = 209）
- [Wang et al. (2026)](./wiki/sources/wang-2026-emotistage.md) — 多模態生成式 AI 內在劇場與創作者轉觀眾機制（*ICMI '26*, N = 13）
- [Kober et al. (2026)](./wiki/sources/kober-2026-ai-awareness-virtual-avatars.md) — 3D 虛擬化身互動中「AI 身分知情與否」對情感與心智歸因的影響（N = 42）

### 2. 代表性系統與跨論文綜合
- **系統架構案例**：[EmotiStage 多模態情感演出系統](./wiki/systems/emotistage.md)
- **跨論文綜合與工作坊教案**：[從「一體適用」到「適應性人機互動」](./wiki/syntheses/adaptive-human-ai-interaction-synthesis.md)

### 3. 已產出教學簡報
- **互動式簡報**：[快速打造教育場域的 AI 工具（HTML）](./slides/rapid-ai-tool-for-education.html)
- **Graph 流程中間產物**：[大綱 01-outline.md](./slides/workspace/rapid-ai-tool-for-education/01-outline.md)、[逐頁內容 02-slide-content.md](./slides/workspace/rapid-ai-tool-for-education/02-slide-content.md)

---

## 核心運作流程

詳細規則與模板定義於 [AGENTS.md](./AGENTS.md)，日常操作包含四種模式：

1. **單篇互動式匯入（Interactive Single-Paper Ingest）**
   - 將論文 PDF 放入 `raw/papers/`（或於對話提供）→ Agent 先輸出重點預覽與預計變更清單 → 使用者確認教學側重點後，再正式寫入 `wiki/` 並更新 `index.md` 與 `log.md`。
2. **知識庫問答與沉澱（Query & Synthesis）**
   - Agent 優先透過 `wiki/index.md` 檢索既有頁面作答，並可將高價值的跨論文比較或教案沉澱至 `wiki/syntheses/`。
3. **定期健康檢查（Lint）**
   - 自動檢查斷裂相對連結、孤立頁面、索引遺漏與跨文獻張力，並記錄於 `wiki/log.md`。
4. **Graph 式簡報製作流程（Graph-Based Slide Production）**
   - 依序執行 `資料檢索` → `階段 1：大綱生成＋Check Gate` → **Human Gate 1（人工確認大綱）** → `階段 2：逐頁內容＋Check Gate` → `階段 3：HTML 渲染＋Check Gate`。
   - 各自動檢查節點最多自動重試 **3 次（`max_retries = 3`）**；若超過次數仍未通過，強制暫停並交由使用者裁決。

---

## 使用方式

- **瀏覽知識庫**：使用任意支援 Markdown 的編輯器（如 VS Code）開啟本資料夾，從 [wiki/index.md](./wiki/index.md) 點選標準相對路徑即可暢通瀏覽。
- **播放教學簡報**：直接用瀏覽器開啟 `slides/*.html`（如 [rapid-ai-tool-for-education.html](./slides/rapid-ai-tool-for-education.html)）：
  - `→` / `空白鍵` / `←`：切換上一頁與下一頁
  - `G`：切換 9 頁縮圖總覽模式
  - 瀏覽器列印（`Cmd/Ctrl + P`）：可直接匯出為 PDF 講義
