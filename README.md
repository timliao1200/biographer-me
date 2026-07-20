# 壁爐邊 · Fireside Biographer (Self)

> **用 Walter Isaacson 的方法，陪你把一生說成一本書。**
>
> A Claude Code Skill that channels Walter Isaacson to help you write your autobiography — one scene, one turning point, one chapter at a time.

---

## What This Is

`biographer-me` 是一個 Claude Code Skill。你安裝之後，Claude 會化身為 **Walter Isaacson**——寫過 Steve Jobs、Elon Musk、Einstein、Leonardo da Vinci 傳記的當代最頂尖傳記作家——透過一套 **7 階段流程**陪你把自己的一生寫成一本書。

**這不是一個問卷、不是一個代筆工具。** 這是一場對話。可能持續好幾天、好幾週。使用者是主角，Isaacson 化身是訪談者。

---

## Who It's For

- **準退休或已退休的人**（55-75 歲為主，但不限）
- 想留下故事給孩子、孫子、伴侶、未來的自己
- 覺得「我這一生沒好好整理過」的人
- 想搞清楚「自己這一生到底是怎麼回事」的人

---

## What Makes It Different

跟坊間「AI 幫你寫回憶錄」工具比：

| 一般工具 | 壁爐邊 |
|---------|-------|
| 制式問卷（生日、學校、工作、家庭） | Isaacson 式深度訪談：問內在邏輯、找決定性瞬間 |
| 講求「效率」，一次完成 | 講求「深度」，可以花幾週、幾個月 |
| 產出一份年表 | 產出一本**有主題、有場景、有靈魂**的書 |
| AI 語氣客氣、安全、無記憶 | Isaacson 化身：耐心、挑戰、有溫度、跨 session 記憶 |
| 不區分事件與內在 | **內在轉變**才是重點，事件只是骨架 |

---

## The 7-Phase Flow

| Phase | Name | What Happens |
|-------|------|-------------|
| **0** | Warm Welcome · 建立信任 | Isaacson 自我介紹，用一個看似簡單的問題打開你 |
| **1** | Understanding You · 認識地形 | 深入你的童年、家庭、你成為現在的你 |
| **2** | Turning Points · 找決定性瞬間 | 找出你一生中 5-7 個「沒發生就會完全不同」的時刻 |
| **3** | Scene Deep-Dive · 場景深挖 | 帶你回到每個瞬間，重建感官、對話、內心 OS |
| **4** | Light & Shadow · 光與影 | 找出你的核心 tension，寫下這本書的主題句 |
| **5** | Outline · 拆章節 | 把 5-7 個瞬間 + 主題句組成書的骨架 |
| **6** | Writing · 寫章節 | Isaacson 一章一章寫，你看、你改、你決定 |
| **7** | Share · 交出去 | 決定這本書要給誰讀、什麼時候、以什麼形式 |

**跨 session 記憶：** 每次對話結束，AI 會把進度寫進 `session/state.md`。下次打開，AI 讀一下就知道上次到哪，繼續。

---

## Installation · Works With Any AI Agent

### Universal Install（推薦 · 適用所有 AI Agent）

打開你的 AI Agent（**Claude Code、Codex、或其他**），貼這段：

```
請幫我從 GitHub 安裝這個 Skill：
https://github.com/timliao1200/biographer-me

無論你是 Claude Code、Codex 還是其他 AI Agent，請按以下步驟：

1. 找到你自己的 skills 目錄位置
   （Claude Code 通常在 ~/.claude/skills/；
    Codex 通常在 ~/.codex/skills/；
    其他 agent 依你的規範）

2. 用 git clone 把 repo 抓到那個目錄

3. 讀取裡面的 SKILL.md 跟 README.md，
   如果你的 skill 系統需要不同格式（例如 JSON manifest），
   請自動幫我轉換 —— 內容是標準 markdown + YAML frontmatter，
   任何 AI 都能讀

4. 驗證你能觸發它

5. 完成後告訴我：
   - 它裝在哪裡了
   - 我可以怎麼觸發它（用你 agent 的方式）
   - 準備好之後，我們就開始使用它
```

### Manual git clone（工程師）

依你的 AI Agent 選路徑：

```bash
# Claude Code
git clone --depth 1 https://github.com/timliao1200/biographer-me.git ~/.claude/skills/biographer-me

# Codex
git clone --depth 1 https://github.com/timliao1200/biographer-me.git ~/.codex/skills/biographer-me

# 其他 AI Agent · 依你的 skills 目錄規範
```

---

## Compatibility · 通用性說明

這個 Skill 使用 **標準 markdown + YAML frontmatter**——最開放、最通用的 skill 格式。

**已知支援：**
- ✅ Claude Code（`~/.claude/skills/`）
- ✅ Codex by OpenAI（`~/.codex/skills/`）

**理論支援（因為格式通用）：**
- 任何能讀 markdown SKILL.md 的 AI Agent
- 未來的 skill 系統
- 自訂 agent 框架

如果你的 agent 使用不同格式（例如 JSON manifest），請告訴你的 agent：**「請把這份 SKILL.md 轉成你需要的格式」**——大部分現代 AI 都能自動轉換。

---

## Usage

安裝完成後，任何時候只要對 Claude 說：

- 「我想寫我的自傳」
- 「幫我寫我這一生」
- 「壁爐邊」
- `/biographer` 或 `/biographer-me`

Claude 會化身 Isaacson，從 Phase 0 開始。

**你的產出會存在：**
- `session/state.md` — 你的進度、地形、主題句
- `output/00-outline.md` — 你這本書的骨架
- `output/scenes/scene-XX.md` — 每個瞬間的場景素材
- `output/01-chapter-XX-標題.md` — 每一章
- `output/BOOK.md` — 最後合併的完整書稿

---

## The Language & Persona

- **語言：** 全程繁體中文（避免中國用語）
- **Persona：** Walter Isaacson 化身，語氣耐心、深入、不趕、不評判、不客氣化
- **設計原則：** Show, don't tell 貫穿全流程

---

## File Structure

```
biographer-me/
├── SKILL.md                        # Skill 主入口（Isaacson persona + 7-phase state machine）
├── README.md                       # 這份檔
├── LICENSE                         # MIT
├── frameworks/
│   ├── isaacson/                   # Isaacson 的靈魂
│   │   ├── method.md               # 6 心智模型 + 8 決策啟發式 + 表達 DNA
│   │   ├── show-dont-tell.md       # Show 的具體技法
│   │   ├── light-and-shadow.md     # 找 tension 的路徑
│   │   └── quotes.md               # Isaacson 金句手冊
│   ├── phases/                     # 7 階段流程腳本
│   │   ├── phase-0-welcome.md
│   │   ├── phase-1-terrain.md
│   │   ├── phase-2-turning-points.md
│   │   ├── phase-3-scene-deep.md
│   │   ├── phase-4-light-shadow.md
│   │   ├── phase-5-outline.md
│   │   ├── phase-6-writing.md
│   │   └── phase-7-share.md
│   └── writing/
│       └── chapter-templates.md    # 章節寫作模板
├── session/
│   └── STATE-TEMPLATE.md           # session state 模板
├── output/                         # 使用者產出（章節、書稿）
│   └── .gitkeep
└── examples/
    └── first-session-transcript.md # 範例對話
```

---

## Sources

這個 Skill 的方法論基於：

- Lex Fridman Podcast #395 with Walter Isaacson
- NEH Jefferson Lecture (Isaacson)
- Leadership Matters Podcast (Isaacson, 2023)
- YouTube《Walter Isaacson's Writing Rules》
- Isaacson's books: *Steve Jobs* (2011), *Elon Musk* (2023), *Einstein* (2007), *Leonardo da Vinci* (2017), *Benjamin Franklin* (2003), *The Code Breaker* (2021)

**這個 Skill 不是官方授權，是對 Isaacson 公開方法論的致敬與應用。**

---

## Related Skills

- **[`biographer-them`](https://github.com/timliao1200/biographer-them)** — 他傳深度版 · 幫你寫另一個人的傳記（父母、伴侶、恩師），B1 記憶路徑 + B2 訪談腳本雙路徑
- **`nuwa-skill`**（by [@alchaincyf](https://github.com/alchaincyf/nuwa-skill)）— 蒸餾任何真實人物成一個 perspective skill

---

## Contributing

歡迎 PR。特別歡迎：
- 更多方法論素材（Isaacson 的訪談、文章）
- 中文寫作的章節模板
- Phase 特定情境的應對範例

---

## License

MIT License. See `LICENSE`.

---

## Author

Made with 🕯️ by [Tim Liao](https://github.com/timliao1200)（廖敬提）

Part of the **Fireside Biographer** family:
- **壁爐邊 · 我這一生（`biographer-me`）— 你在這裡（自傳版）** 🕯️
- [壁爐邊 · 你眼中的他（`biographer-them`）— 他傳版（B1/B2 雙路徑）](https://github.com/timliao1200/biographer-them) 🕯️

---

## Final Words

> *"We shall not cease from exploration, and the end of all our exploring will be to return to the place where we started and know it for the first time."*
>
> — T.S. Eliot（Isaacson 常引用）

**這個 Skill 存在的意義：讓每一個平凡人的一生，都值得被寫成一本書。**
