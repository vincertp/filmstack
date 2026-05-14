# filmstack

> 「開發是把錢變成劇本的過程，製作是把劇本變成電影的過程。」
> — William Goldman

**filmstack** 是一套開源的 AI 影視工作流程系統——以 [gstack](https://github.com/garrytan/gstack) 的設計哲學為基礎，專為電影與電視產業重新打造。

它把 Claude Code（或任何支援 SKILL.md 標準的 AI 代理）變成一個虛擬製作團隊：一位找出你情節破綻的故事編輯、一位用真實好萊塢標準評估劇本的讀稿人、一位壓力測試預算的製片主任、一位掃描法律風險的版權顧問，以及一位把你的完片導向正確市場的院線策略師。

**23 個技能。7 個製作階段。從概念到發行的完整流程。**

---

## 製作流程

filmstack 遵循好萊塢實際的七階段製作流程：

```
開發 → 前製 → 拍攝 → 後製 → 行銷 → 發行 → 映演
```

每個技能的輸出都會成為下一個技能的輸入。`/pitch-room` 寫出的創作提案由 `/coverage` 讀取；`/breakdown` 產出的場景清單由 `/budget-review` 使用；`/picture-lock` 生成的交片清單由 `/rights-clearance` 驗證。

| 階段 | 技能 | 角色 | 功能說明 |
|---|---|---|---|
| **開發** | `/logline` | 故事顧問 | Logline 工作坊——迭代精煉，直到找到那句能賣出電影的句子 |
| **開發** | `/pitch-room` | 故事監製 | 六個強迫提問，在你動筆前挑戰你的概念 |
| **開發** | `/series-bible` | 電視編劇／監製人 | 影集聖經結構——前提、人物、季弧、集數概念、持續潛力 |
| **開發** | `/coverage` | 劇本讀稿人 | 好萊塢標準讀稿報告：Logline、故事摘要、評語、Pass/Consider/Recommend |
| **開發** | `/script-doctor` | 故事編輯 | 找出情節漏洞、人物弧線斷裂、節奏問題與缺乏動機的選擇 |
| **開發** | `/market-comp` | 開發主管 | 參考片分析——「A meets B」定位框架、票房數據、串流基準值 |
| **開發** | `/pitch-deck` | 包裝專員 | 投資人與發行商提案簡報——9 張投影片結構與七項測試 |
| **前製** | `/breakdown` | 第一副導演 | 逐場分解：場景、演員、特技、道具、VFX、特殊需求 |
| **前製** | `/casting-breakdown` | 選角導演 | 以 Breakdown Express 格式輸出角色資料，可直接提交 |
| **前製** | `/budget-review` | 製片主任 | 預算可行性評估、拍攝風險、每日成本估算、紅旗警示 |
| **前製** | `/co-production` | 國際合拍顧問 | 雙邊條約資格、積分測試、財務結構、各地區優惠 |
| **前製** | `/wga-check` | 勞動合規顧問 | WGA/SAG-AFTRA 合規掃描——最低工資標準、殘片費、署名仲裁觸發條件 |
| **前製** | `/rights-clearance` | 娛樂法律顧問 | E&O 保險前置審查——音樂授權、人物肖像權、商標風險 |
| **前製** | `/taiwan-production` | 台灣製作顧問 | 文化部輔導金、TAICCA、金馬影展策略、OTT 平台景觀、合拍資格 |
| **後製** | `/adr-session` | 後製聲音監督 | ADR 對白補錄準備——提示表、演員排程、錄音室清單 |
| **後製** | `/picture-lock` | 後製監督 | 畫面鎖定清單——交付規格、VFX 拉出清單、聲音對位、M&E 需求 |
| **後製** | `/dcp-delivery` | 數位院線交付專員 | DCP 製作、加密、KDM 管理、院線交付完整清單 |
| **發行** | `/music-licensing` | 音樂授權監督 | 雙授權規則、同步版權 vs. 母帶版權清除、PRO 登記、音樂提示表需求 |
| **發行** | `/distribution-deal` | 版權代理／娛樂律師 | 發行合約審查——MG、P&A 承諾、映演窗口、淨利潤瀑布式分配 |
| **發行** | `/festival-strategy` | 版權代理 | 依內容類型、預算與目標（獎項 vs. 發行）規劃影展路線 |
| **發行** | `/press-kit` | 宣傳統籌 | EPK 電子新聞資料包——簡介、導演自述、製作紀錄、素材清單 |
| **發行** | `/korea-production` | 韓國製作顧問 | KOFIC 補助、釜山影展策略、韓國 OTT 生態、台韓合拍框架 |
| **進階工具** | `/retro` | 製片人 | 製作回顧——預算差異分析、拍攝進度偏移、下次改進方向 |

---

## 快速開始

1. 安裝 filmstack（見下方說明）
2. 執行 `/pitch-room`——描述你正在開發的項目
3. 對劇本草稿執行 `/coverage`
4. 執行 `/script-doctor` 找出結構問題
5. 停在這裡。你自然會知道這套工具適不適合你。

## 安裝——30 秒搞定

**需求：** [Claude Code](https://docs.anthropic.com/en/docs/claude-code)、[Git](https://git-scm.com/)

### 全域安裝（適用所有專案）

開啟 Claude Code，貼上以下指令：

> 安裝 filmstack：執行 `git clone https://github.com/vincertp/filmstack.git ~/.claude/skills/filmstack`，然後在 CLAUDE.md 中新增「filmstack」區塊，列出所有可用技能：/pitch-room、/coverage、/script-doctor、/market-comp、/breakdown、/casting-breakdown、/budget-review、/picture-lock、/festival-strategy、/rights-clearance、/wga-check、/retro。

### 加入特定專案

```bash
cp -Rf ~/.claude/skills/filmstack .claude/skills/filmstack
rm -rf .claude/skills/filmstack/.git
```

然後在專案的 `CLAUDE.md` 中加入：

```
## filmstack
可用技能：/pitch-room、/coverage、/script-doctor、/market-comp、/logline、/series-bible、
/pitch-deck、/breakdown、/casting-breakdown、/budget-review、/picture-lock、
/festival-strategy、/rights-clearance、/wga-check、/retro。
```


### 作為 Cowork Plugin 安裝

filmstack 已封裝為 Claude Cowork plugin。在 Cowork 中，透過 Plugin 選單，輸入以下 repo URL 安裝：



安裝後 23 個技能立即以斜線指令形式可用。

### 其他 AI 代理（Codex、Gemini CLI、Cursor）

filmstack 適用於任何支援 [SKILL.md 標準](https://github.com/anthropics/claude-code)的代理。將技能目錄複製到 `.agents/skills/filmstack/` 即可。

---

## 實際運作範例

```
你：    我想拍一部關於台灣科技富豪假裝死亡的電影。
你：    /pitch-room

Claude: 在你動筆之前，六個問題：
        1. 傷口是什麼？不是情節——是這個角色無法逃脫的傷口。
        2. 當富豪既是反派又是受害者，觀眾該認同誰？
        3. 類型契約是什麼？驚悚片承諾有解答，劇情片不承諾。
        4. 什麼樣的台灣特殊性讓這個故事不只是「另一個富豪故事」？
        5. 他消失之後誰是輸家——我們對那個人的感情比對他更深嗎？
        6. 「假裝死亡」讓他付出了什麼金錢買不回來的代價？

        [你回答。Claude 整合成創作提案。]
        [提案儲存至 .filmstack/creative-brief.md]

你：    /coverage 劇本初稿v2.pdf

Claude: 片名：[你的片名]
        編劇：[你]
        類型：驚悚 / 劇情
        頁數：112
        LOGLINE：一位台灣科技富豪為逃避弊案調查而偽造死亡，
                 卻發現他一直在逃避的那個身份，
                 是唯一值得活下去的身份。

        故事摘要：[完整一頁含劇透摘要]

        評語：
        概念：8/10——題材具商業性。台灣背景在此類型中尚未被充分開發……
        結構：6/10——第二幕在第67頁前後崩潰……
        人物：7/10——主角動機清晰，但反派厚度不足……
        對白：7/10——對抗場景有力，鋪陳場景說教感重……
        市場性：8/10——有對應的串流參考片……

        建議：CONSIDER（值得考慮）
        [具體理由]

你：    /script-doctor

Claude: 鐵律：先診斷，再開藥。
        [追溯第二幕崩潰的根源——三個導致結構斷裂的場景]
        [找出反派問題——第43頁缺少一場關鍵戲]
        [發現第89頁一個缺乏動機的戲劇逆轉]
        建議修改：[具體、最小介入、不傷害現有結構]
```

---

## 文件

| 文件 | 內容 |
|---|---|
| [技能深度解析](docs/skills.md) | 每個技能的設計哲學與工作流程（英文） |
| [系統架構](ARCHITECTURE.md) | 設計決策與流程邏輯（英文） |
| [貢獻指南](CONTRIBUTING.md) | 如何新增技能或改善現有技能（英文） |

## 重要說明

**這是創意分析工具，不是法律工具。** `/rights-clearance` 與 `/wga-check` 產出的是初步清單——無法取代合格的娛樂律師或勞動法顧問。正式製作前請務必諮詢專業人士。

**本工具的好萊塢術語**以美國產業標準為基礎。國際合拍案將涉及不同的工會協議、版權授權規範與發行慣例，請依所在地區調整。

**台灣製作環境說明：** `/taiwan-production` 涵蓋文化部輔導金、TAICCA 投資、國片認定標準、金馬影展策略與 OTT 平台景觀。`/korea-production` 提供台韓合拍框架，包含 KOFIC-TAICCA MOU（2023）雙重補助申請路徑。

## 授權

MIT。永久免費。

---

[English README](README.md)
