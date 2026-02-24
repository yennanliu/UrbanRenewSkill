# Taiwan Urban Renewal Expert Skill

## 台灣都市更新全方位顧問技能包

[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/yennanliu/UrbanRenewSkill)
[![Language](https://img.shields.io/badge/language-Traditional%20Chinese-green.svg)](https://github.com/yennanliu/UrbanRenewSkill)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-✓-purple.svg)](https://github.com/anthropics/claude-code)
[![Cursor](https://img.shields.io/badge/Cursor-✓-blue.svg)](cross-platform/cursor/)
[![Copilot](https://img.shields.io/badge/GitHub%20Copilot-✓-green.svg)](cross-platform/copilot/)
[![Gemini](https://img.shields.io/badge/Gemini-✓-orange.svg)](cross-platform/gemini/)
[![Universal](https://img.shields.io/badge/ChatGPT%20%7C%20Claude-✓-red.svg)](cross-platform/universal/)
[![License](https://img.shields.io/badge/license-MIT-orange.svg)](LICENSE)

台灣都市更新專家 AI 技能，整合實施者、建築師與法律顧問的專業能力。

**🎉 新功能：** 現已支援多個 AI 平台！[查看跨平台設定指南 →](cross-platform/README.md)

## ✨ 特色功能

- 🏛️ **精準法規解釋** - 引用具體《都市更新條例》條文編號
- 📊 **容積獎勵計算** - 評估綠建築、智慧建築、TOD等獎勵
- ⚖️ **權變 vs 協議分析** - 深入比較兩種實施方式
- 📝 **專業文書製作** - 起草事業計畫書、合建契約等
- 🗺️ **在地化考量** - 涵蓋台北市、新北市等地方自治法規
- 🇹🇼 **純繁體中文** - 使用台灣專業術語，無簡體字

## 🎯 核心能力

| 專業領域 | 具體功能 |
|---------|---------|
| **法規諮詢** | 都市更新條例、權利變換實施辦法、容積獎勵辦法解釋 |
| **案件評估** | 可行性分析、容積試算、財務評估、危老vs都更比較 |
| **策略規劃** | 同意門檻達成策略、談判技巧、風險管理建議 |
| **法律諮商** | 代為拆除程序、少數不同意戶權益、信託機制 |
| **文書製作** | 事業計畫書、權變計畫、通知書、合建契約起草 |

## 🤖 支援的 AI 平台

本技能現已支援多個 AI 平台，選擇您喜歡的工具開始使用：

| 平台 | 狀態 | 設定時間 | 適用對象 | 快速開始 |
|------|------|---------|---------|---------|
| **Claude Code** | ✅ 原生支援 | 0分鐘 | 開發者 | [開始使用](#方法一直接使用推薦) |
| **Cursor** | ✅ 完整支援 | 1分鐘 | 開發者 | [Cursor 設定](cross-platform/cursor/) |
| **GitHub Copilot** | ✅ 完整支援 | 2分鐘 | VS Code 用戶 | [Copilot 設定](cross-platform/copilot/) |
| **Google Gemini** | ✅ 完整支援 | 1分鐘 | CLI/API 用戶 | [Gemini 設定](cross-platform/gemini/) |
| **ChatGPT** | ✅ 完整支援 | 1分鐘 | 一般用戶 | [ChatGPT 設定](cross-platform/universal/) |
| **Claude.ai** | ✅ 完整支援 | 1分鐘 | 一般用戶 | [Claude 設定](cross-platform/universal/) |

**📖 詳細設定指南：** [cross-platform/README.md](cross-platform/README.md)
**⚡ 快速參考：** [cross-platform/QUICK-REFERENCE.md](cross-platform/QUICK-REFERENCE.md)

## 📦 Claude Code 安裝方式

### 方法一：直接使用（推薦）

1. 克隆此專案到本地：
```bash
git clone https://github.com/your-org/UrbanRenewSkill.git
cd UrbanRenewSkill
```

2. 啟動 Claude Code 並指向此目錄：
```bash
claude-code
```

3. 技能會自動載入，開始詢問都市更新相關問題即可。

### 方法二：安裝到全域 Claude 技能目錄

1. 複製技能檔案到 Claude 全域目錄：
```bash
# macOS/Linux
cp -r .claude/skills/* ~/.claude/skills/

# Windows
copy .claude\skills\* %USERPROFILE%\.claude\skills\
```

2. 在任何專案中使用此技能：
```bash
cd your-project
claude-code
```

### 方法三：符號連結（開發者模式）

```bash
# macOS/Linux
ln -s /path/to/UrbanRenewSkill/.claude/skills/taiwan-urban-renewal.md ~/.claude/skills/

# Windows (需管理員權限)
mklink %USERPROFILE%\.claude\skills\taiwan-urban-renewal.md "C:\path\to\UrbanRenewSkill\.claude\skills\taiwan-urban-renewal.md"
```

## 🚀 快速開始

### 基本使用

啟動 Claude Code 後，直接詢問都市更新相關問題：

```
你: 我們社區在台北市信義區，想推動都更需要多少住戶同意？
```

```
你: 危老重建跟都更有什麼差別？
```

```
你: 容積獎勵最高可以拿到多少？
```

### 進階使用

#### 案件評估
```
你: 請評估以下條件是否適合都更：
- 地點：台北市大安區
- 基地面積：800㎡
- 建物屋齡：35年
- 住戶數：30戶
- 目前同意率：70%
```

#### 文件起草
```
你: 請幫我起草一份都市更新事業計畫的所有權人通知書
```

#### 法規查詢
```
你: 都市更新條例第22條的同意門檻規定是什麼？請詳細說明
```

## 📚 文件資源

- [技能詳細說明](.claude/skills/README.md) - 完整功能介紹
- [使用範例](.claude/skills/EXAMPLES.md) - 實際問答案例
- [技能定義檔](.claude/skills/taiwan-urban-renewal.md) - 技能核心檔案

## 💡 使用範例

### 範例1：同意門檻查詢

**輸入：**
```
我們社區要推動都更，位於非劃定更新地區，需要多少同意？
```

**輸出：**
```markdown
## 非劃定更新地區同意門檻說明

### ⚖️ 法規適用
依據《都市更新條例》第22條第2項，非劃定更新地區需符合：
- 土地所有權人數：超過 3/4
- 土地及建物所有權人數：超過 3/4
- 土地總面積：超過 3/4
- 合法建物總面積：超過 3/4

[...詳細分析...]
```

### 範例2：容積獎勵計算

**輸入：**
```
基準容積300%，申請綠建築和智慧建築獎勵，總容積可達多少？
```

**輸出包含：**
- 詳細計算過程
- 法規依據引用
- 成本效益分析
- 申請流程說明

更多範例請參考 [EXAMPLES.md](.claude/skills/EXAMPLES.md)

## 🎓 適用對象

- 🏘️ **地主/土地所有權人** - 了解自身權益與選項
- 🏠 **住戶/建物所有權人** - 評估參與都更意願
- 🏗️ **實施者/建商** - 規劃執行策略
- 👥 **更新會成員** - 推動案件進度
- 👷 **建築師/都市計畫師** - 專業技術諮詢
- ⚖️ **律師/法務人員** - 法規適用確認

## 🔍 技能範圍

### ✅ 涵蓋範圍

- 台灣都市更新法規解釋
- 權利變換 vs 協議合建分析
- 容積獎勵評估計算
- 同意門檻策略規劃
- 危老重建 vs 都更比較
- 專業文件起草審查
- 法律風險分析

### ❌ 不包含範圍

- 結構工程技術細節
- 房地產市場價格預測
- 稅務規劃建議（請諮詢會計師）
- 訴訟代理（請諮詢執業律師）

## ⚖️ 法律聲明

本技能提供的資訊僅供參考，**不構成正式法律意見**。具體案件建議諮詢：

- 執業律師（法律訴訟）
- 執業建築師（建築設計）
- 不動產估價師（不動產估價）
- 會計師（稅務規劃）

## 🛠️ 技術規格

- **Claude Code 版本要求：** >= 0.1.0
- **模型要求：** Claude 3.5 Sonnet 或更高
- **語言：** Traditional Chinese (zh-TW)
- **檔案格式：** Markdown with YAML frontmatter

## 📁 專案結構

```
UrbanRenewSkill/
├── .claude/
│   └── skills/
│       ├── taiwan-urban-renewal.md  # 主技能定義檔
│       ├── skill.json               # 技能元資料
│       ├── README.md                # 技能說明文件
│       └── EXAMPLES.md              # 使用範例集
├── prompt/
│   ├── prompt_gpt.txt              # GPT版本提示詞
│   └── prompt_gemini.txt           # Gemini版本提示詞
└── README.md                        # 本文件
```

## 🤝 貢獻指南

歡迎提交改進建議！

### 如何貢獻

1. Fork 此專案
2. 創建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交變更 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 開啟 Pull Request

### 貢獻方向

- 📚 補充實務案例
- 🔄 更新最新法規
- 🐛 修正錯誤資訊
- 🌟 新增功能特性
- 📝 改善文件說明

## 📝 版本歷史

### v1.0.0 (2024-02-24)
- ✨ 初始版本發布
- ✅ 完整都市更新條例解釋能力
- ✅ 權利變換與協議合建分析
- ✅ 容積獎勵計算功能
- ✅ 危老 vs 都更比較
- ✅ 文件起草與審查能力
- ✅ 台北市/新北市在地化規範

## 🔗 相關資源

### 官方法規
- [都市更新條例（全國法規資料庫）](https://law.moj.gov.tw/)
- [台北市都市更新處](https://www.uro.gov.taipei/)
- [新北市都市更新處](https://www.planning.ntpc.gov.tw/)

### Claude Code
- [Claude Code GitHub](https://github.com/anthropics/claude-code)
- [Claude Code 文件](https://docs.anthropic.com/claude-code)
- [Claude API 文件](https://docs.anthropic.com/)

## 📧 聯繫方式

- **專案維護者：** Jerry Liu
- **問題回報：** [GitHub Issues](https://github.com/your-org/UrbanRenewSkill/issues)
- **功能建議：** [GitHub Discussions](https://github.com/your-org/UrbanRenewSkill/discussions)

## 📄 授權條款

本專案採用 MIT License - 詳見 [LICENSE](LICENSE) 文件

---

## ⭐ Star History

如果這個技能對您有幫助，請給我們一個 Star ⭐️

[![Star History Chart](https://api.star-history.com/svg?repos=your-org/UrbanRenewSkill&type=Date)](https://star-history.com/#your-org/UrbanRenewSkill&Date)

---

**© 2024 Taiwan Urban Renewal Expert Skill for Claude Code**

**Made with ❤️ for Taiwan's Urban Renewal Community**
