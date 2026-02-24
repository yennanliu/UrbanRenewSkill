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

---

## 📦 其他 AI 平台安裝方式

### 🔵 Cursor IDE

**適用於：** Cursor IDE 用戶

#### 快速安裝
```bash
# 方法一：複製到專案根目錄（推薦）
cp cross-platform/cursor/.cursorrules .cursorrules

# Cursor 會自動載入配置
```

#### 全域安裝
```bash
# 複製到 Cursor 全域配置目錄
cp cross-platform/cursor/.cursorrules ~/.cursor/.cursorrules
```

#### 使用方式
1. 開啟 Cursor IDE
2. 按 `Cmd+K` (Mac) 或 `Ctrl+K` (Windows)
3. 輸入都更相關問題，例如：
   ```
   我們社區要推動都更，需要多少住戶同意？
   ```

#### 優點
- ✅ 自動載入，無需手動配置
- ✅ 整合在編輯器中
- ✅ 支援程式碼註解觸發
- ✅ 團隊共享配置（透過 Git）

📖 **詳細文件：** [cross-platform/cursor/](cross-platform/cursor/)

---

### 🟢 GitHub Copilot

**適用於：** VS Code + GitHub Copilot 用戶

#### 方法一：專案配置（推薦）
```bash
# 建立 .github 目錄
mkdir -p .github

# 複製 Copilot 指示檔
cp cross-platform/copilot/copilot-instructions.md .github/copilot-instructions.md
```

#### 方法二：VS Code 設定
在專案根目錄建立或編輯 `.vscode/settings.json`：

```json
{
  "github.copilot.chat.codeGeneration.instructions": [
    {
      "text": "當討論台灣都市更新議題時，請扮演都市更新全方位顧問，整合實施者、建築師與法律顧問專業..."
    }
  ],
  "github.copilot.chat.localeOverride": "zh-TW"
}
```

#### 使用方式

**Copilot Chat:**
```
@workspace 請用都市更新專家角色說明同意門檻
```

**程式碼註解:**
```typescript
// 請用都市更新專家角色計算容積獎勵
```

**Inline Chat:**
```
Ctrl+I (或 Cmd+I): 請比較危老重建和都更
```

#### 優點
- ✅ 整合在開發流程中
- ✅ 支援多種觸發方式
- ✅ 團隊可共享配置
- ✅ 版本控制友善

📖 **詳細文件：** [cross-platform/copilot/copilot-instructions.md](cross-platform/copilot/copilot-instructions.md)

---

### 🟠 Google Gemini

**適用於：** Gemini CLI 或 API 用戶

#### Gemini CLI 使用

**一次性使用:**
```bash
gemini chat --system-instruction="$(cat cross-platform/gemini/gemini-system-instruction.txt)"
```

**建立別名（推薦）:**
```bash
# 加入到 ~/.zshrc 或 ~/.bashrc
echo 'alias urban-renewal="gemini chat --system-instruction=\"\$(cat ~/UrbanRenewSkill/cross-platform/gemini/gemini-system-instruction.txt)\""' >> ~/.zshrc

# 重新載入
source ~/.zshrc

# 使用
urban-renewal
```

#### Gemini API 使用

**Python 範例:**
```python
import google.generativeai as genai

# 讀取系統指示
with open('cross-platform/gemini/gemini-system-instruction.txt', 'r') as f:
    system_instruction = f.read()

# 配置模型
genai.configure(api_key='your-api-key')
model = genai.GenerativeModel(
    model_name='gemini-1.5-pro',
    system_instruction=system_instruction
)

# 使用
response = model.generate_content('我們社區要推動都更，需要多少同意？')
print(response.text)
```

#### 優點
- ✅ 支援 CLI 和 API
- ✅ 適合自動化腳本
- ✅ 可整合到工作流程
- ✅ Python、Node.js 等多語言支援

📖 **詳細文件：** [cross-platform/gemini/gemini-system-instruction.txt](cross-platform/gemini/gemini-system-instruction.txt)

---

### 🔴 ChatGPT (OpenAI)

**適用於：** ChatGPT 網頁版或 API 用戶

#### 網頁版設定

1. 登入 [ChatGPT](https://chat.openai.com)
2. 點選左下角個人資料
3. **Settings** → **Personalization** → **Custom Instructions**
4. 在 "How would you like ChatGPT to respond?" 貼上：

```
從 cross-platform/universal/system-prompt.md 複製「SYSTEM PROMPT」區塊內容
```

5. 儲存並開始使用

#### OpenAI API 使用

**Python 範例:**
```python
import openai

# 讀取系統提示詞
with open('cross-platform/universal/system-prompt.md', 'r') as f:
    content = f.read()
    # 提取 SYSTEM PROMPT 區塊
    system_prompt = content.split('```')[1]

openai.api_key = 'your-api-key'
response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": "容積獎勵最高可以拿到多少？"}
    ]
)
print(response.choices[0].message.content)
```

#### 優點
- ✅ 設定簡單
- ✅ 所有對話都套用
- ✅ 支援網頁和 API
- ✅ 持久化配置

📖 **詳細文件：** [cross-platform/universal/system-prompt.md](cross-platform/universal/system-prompt.md)

---

### 🟣 Claude.ai (Anthropic)

**適用於：** Claude.ai 網頁版或 API 用戶

#### 網頁版設定

1. 登入 [Claude.ai](https://claude.ai)
2. 點選左上角 **Projects**
3. 建立新專案：「Taiwan Urban Renewal Expert」
4. 在 **Project Knowledge** 中：
   - 點選 **Add Content**
   - 上傳 `cross-platform/universal/system-prompt.md`
   - 或直接貼上系統提示詞到 Custom Instructions
5. 開始使用

#### Anthropic API 使用

**Python 範例:**
```python
import anthropic

# 讀取系統提示詞
with open('cross-platform/universal/system-prompt.md', 'r') as f:
    content = f.read()
    system_prompt = content.split('```')[1]

client = anthropic.Anthropic(api_key='your-api-key')
message = client.messages.create(
    model="claude-3-5-sonnet-20241022",
    max_tokens=4096,
    system=system_prompt,
    messages=[
        {"role": "user", "content": "危老重建跟都更有什麼差別？"}
    ]
)
print(message.content[0].text)
```

#### 優點
- ✅ 支援 Project Knowledge
- ✅ 長上下文能力強
- ✅ 適合複雜文件分析
- ✅ 網頁和 API 都支援

📖 **詳細文件：** [cross-platform/universal/system-prompt.md](cross-platform/universal/system-prompt.md)

---

### ⚫ 其他 AI 工具

**適用於：** 其他支援自訂指示的 AI 工具

大多數 AI 工具都支援某種形式的自訂指示。查找以下關鍵字：
- "Custom Instructions"
- "System Prompt"
- "Personality Settings"
- "Behavior Configuration"

#### 通用設定步驟

1. 開啟 [`cross-platform/universal/system-prompt.md`](cross-platform/universal/system-prompt.md)
2. 複製 **SYSTEM PROMPT** 區塊內容
3. 在您的 AI 工具中找到自訂指示設定
4. 貼上並儲存
5. 測試是否正常運作

📖 **詳細文件：** [cross-platform/README.md](cross-platform/README.md)

---

## 🧪 安裝測試

設定完成後，使用以下問題測試是否正常運作：

### ✅ 測試 1：語言與格式
```
我們社區在台北市信義區，想推動都更需要多少住戶同意？
```

**預期結果：**
- ✓ 回應使用繁體中文（台灣）
- ✓ 包含結構化格式（📋📊⚖️💡⚠️📝）
- ✓ 引用具體法條（都市更新條例第22條）
- ✓ 區分劃定與非劃定地區

### ✅ 測試 2：計算能力
```
基準容積300%，申請綠建築和智慧建築獎勵，總容積可達多少？
```

**預期結果：**
- ✓ 引用都市更新條例第65條
- ✓ 列出各項獎勵百分比
- ✓ 顯示計算過程
- ✓ 說明50%上限

### ✅ 測試 3：比較分析
```
請用表格比較危老重建和都更的差異
```

**預期結果：**
- ✓ 使用表格格式
- ✓ 至少10項比較項目
- ✓ 包含同意門檻、容積獎勵、時程等
- ✓ 提供選擇建議

---

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
