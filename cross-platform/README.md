# Cross-Platform Setup Guide
# 跨平台設定指南

> 讓台灣都市更新專家技能在多個 AI 平台上運作

[![Claude Code](https://img.shields.io/badge/Claude%20Code-✓-purple)](../README.md)
[![Cursor](https://img.shields.io/badge/Cursor-✓-blue)](cursor/)
[![GitHub Copilot](https://img.shields.io/badge/GitHub%20Copilot-✓-green)](copilot/)
[![Gemini](https://img.shields.io/badge/Gemini-✓-orange)](gemini/)
[![Universal](https://img.shields.io/badge/ChatGPT%20%7C%20Claude%20%7C%20Others-✓-red)](universal/)

---

## 📦 目錄結構

```
cross-platform/
├── README.md                           # 本文件
├── cursor/
│   └── .cursorrules                    # Cursor IDE 配置檔
├── copilot/
│   └── copilot-instructions.md         # GitHub Copilot 指示檔
├── gemini/
│   └── gemini-system-instruction.txt   # Gemini CLI 系統指示
└── universal/
    └── system-prompt.md                # 通用系統提示詞（ChatGPT, Claude等）
```

---

## 🚀 快速開始

選擇您使用的平台：

| 平台 | 點擊查看詳細說明 | 設定時間 |
|------|----------------|---------|
| 🔵 **Cursor** | [→ Cursor 設定指南](#cursor-ide) | 1 分鐘 |
| 🟢 **GitHub Copilot** | [→ Copilot 設定指南](#github-copilot) | 2 分鐘 |
| 🟠 **Gemini CLI** | [→ Gemini 設定指南](#google-gemini) | 1 分鐘 |
| 🔴 **ChatGPT** | [→ ChatGPT 設定指南](#chatgpt) | 1 分鐘 |
| 🟣 **Claude** | [→ Claude 設定指南](#claude) | 1 分鐘 |
| ⚫ **其他 AI** | [→ 通用設定指南](#universal-setup) | 依平台而定 |

---

## 平台別設定說明

### Cursor IDE

**適用於：** Cursor IDE 用戶

#### 方法一：自動設定（推薦）
```bash
# 複製 .cursorrules 到專案根目錄
cp cross-platform/cursor/.cursorrules .cursorrules

# Cursor 會自動載入
```

#### 方法二：全域設定
```bash
# 複製到 Cursor 全域配置目錄
cp cross-platform/cursor/.cursorrules ~/.cursor/.cursorrules
```

#### 測試
1. 開啟 Cursor
2. 按 `Cmd+K` (Mac) 或 `Ctrl+K` (Windows)
3. 輸入：`我們社區要推動都更，需要多少同意？`
4. 應收到繁體中文、結構化的回應

#### 優點
- ✅ 自動載入，無需手動配置
- ✅ 整合在編輯器中
- ✅ 支援程式碼註解觸發
- ✅ 團隊共享配置（透過 Git）

---

### GitHub Copilot

**適用於：** VS Code + GitHub Copilot 用戶

#### 方法一：專案配置
```bash
# 建立 .github 目錄（如果不存在）
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
      "text": "當討論台灣都市更新議題時，請扮演都市更新全方位顧問..."
    }
  ],
  "github.copilot.chat.localeOverride": "zh-TW"
}
```

#### 使用方式
```
# 在 Copilot Chat 中
@workspace 請用都市更新專家角色說明同意門檻

# 在程式碼註解中
// 請用都市更新專家角色計算容積獎勵

# Inline Chat
Ctrl+I: 請比較危老重建和都更
```

#### 優點
- ✅ 整合在開發流程中
- ✅ 支援多種觸發方式
- ✅ 團隊可共享配置
- ✅ 版本控制友善

#### 完整文件
查看 [`copilot/copilot-instructions.md`](copilot/copilot-instructions.md) 獲取詳細說明

---

### Google Gemini

**適用於：** Gemini CLI 或 API 用戶

#### Gemini CLI 使用
```bash
# 使用系統指示檔
gemini chat --system-instruction="$(cat cross-platform/gemini/gemini-system-instruction.txt)"

# 或建立別名
alias gemini-urban-renewal='gemini chat --system-instruction="$(cat ~/UrbanRenewSkill/cross-platform/gemini/gemini-system-instruction.txt)"'

# 使用
gemini-urban-renewal
```

#### Gemini API 使用
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

#### 完整文件
查看 [`gemini/gemini-system-instruction.txt`](gemini/gemini-system-instruction.txt)

---

### ChatGPT

**適用於：** ChatGPT (OpenAI) 用戶

#### 網頁版設定
1. 登入 [ChatGPT](https://chat.openai.com)
2. 點選左下角個人資料
3. Settings → Personalization → **Custom Instructions**
4. 在 "How would you like ChatGPT to respond?" 貼上：

```
從 cross-platform/universal/system-prompt.md
複製「SYSTEM PROMPT」區塊內容
```

5. 儲存並開始使用

#### API 使用
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
```

#### 優點
- ✅ 設定簡單
- ✅ 所有對話都套用
- ✅ 支援網頁和 API
- ✅ 持久化配置

---

### Claude

**適用於：** Claude.ai 或 API 用戶

#### Claude.ai 設定
1. 登入 [Claude.ai](https://claude.ai)
2. 點選左上角 **Projects**
3. 建立新專案：「Taiwan Urban Renewal Expert」
4. 在 **Project Knowledge** 中，新增檔案：
   ```
   上傳：cross-platform/universal/system-prompt.md
   ```
5. 或直接貼上系統提示詞到 Custom Instructions

#### Claude API 使用
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
```

#### 優點
- ✅ 支援 Project Knowledge
- ✅ 長上下文能力強
- ✅ 適合複雜文件分析

---

### Universal Setup

**適用於：** 其他支援自訂指示的 AI 工具

大多數 AI 工具都支援某種形式的自訂指示。查找以下關鍵字：
- "Custom Instructions"
- "System Prompt"
- "Personality Settings"
- "Behavior Configuration"

#### 通用步驟
1. 開啟 [`universal/system-prompt.md`](universal/system-prompt.md)
2. 複製 **SYSTEM PROMPT** 區塊內容
3. 在您的 AI 工具中找到自訂指示設定
4. 貼上並儲存
5. 測試是否正常運作

---

## 🧪 測試清單

設定完成後，使用以下問題測試：

### ✅ 測試 1：語言與格式
```
我們社區在台北市信義區，想推動都更需要多少住戶同意？
```

**預期結果：**
- [ ] 回應使用繁體中文（台灣）
- [ ] 包含結構化格式（📋📊⚖️💡⚠️📝）
- [ ] 引用具體法條（都市更新條例第22條）
- [ ] 區分劃定與非劃定地區

### ✅ 測試 2：計算能力
```
基準容積300%，申請綠建築和智慧建築獎勵，總容積可達多少？請詳細計算
```

**預期結果：**
- [ ] 引用都市更新條例第65條
- [ ] 列出各項獎勵百分比
- [ ] 顯示計算過程
- [ ] 說明50%上限
- [ ] 提供成本效益分析

### ✅ 測試 3：比較分析
```
請用表格比較危老重建和都更的差異
```

**預期結果：**
- [ ] 使用表格格式
- [ ] 至少10項比較項目
- [ ] 包含同意門檻、容積獎勵、時程等
- [ ] 提供選擇建議
- [ ] 包含財務試算範例

### ✅ 測試 4：文件起草
```
請幫我起草一份都市更新的所有權人通知書範本
```

**預期結果：**
- [ ] 正式公文格式
- [ ] 繁體中文專業用語
- [ ] 包含必要法定資訊
- [ ] 結構完整清晰

---

## 📊 平台比較

| 特性 | Claude Code | Cursor | Copilot | Gemini | ChatGPT | Claude.ai |
|------|-------------|--------|---------|--------|---------|-----------|
| **設定難度** | ⭐ | ⭐ | ⭐⭐ | ⭐⭐ | ⭐ | ⭐ |
| **自動載入** | ✅ | ✅ | ⚠️ | ❌ | ❌ | ❌ |
| **程式碼整合** | ✅ | ✅ | ✅ | ⚠️ | ❌ | ❌ |
| **團隊共享** | ✅ | ✅ | ✅ | ⚠️ | ❌ | ⚠️ |
| **版本控制** | ✅ | ✅ | ✅ | ⚠️ | ❌ | ❌ |
| **API支援** | ✅ | ❌ | ❌ | ✅ | ✅ | ✅ |
| **CLI支援** | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ |
| **網頁版** | ❌ | ❌ | ❌ | ✅ | ✅ | ✅ |

**圖例：**
- ✅ 完整支援
- ⚠️ 部分支援
- ❌ 不支援
- ⭐ 簡單（1-2分鐘）
- ⭐⭐ 中等（3-5分鐘）

---

## 💡 使用建議

### 開發者工作流程
```
推薦組合：Cursor + GitHub Copilot
- Cursor：日常開發與諮詢
- Copilot：程式碼註解與文件撰寫
```

### 非開發者使用
```
推薦組合：ChatGPT 或 Claude.ai
- 網頁介面友善
- 設定簡單
- 功能完整
```

### 自動化腳本
```
推薦組合：Gemini API 或 Claude API
- CLI 支援
- API 整合容易
- 適合批次處理
```

### 團隊協作
```
推薦組合：Cursor + Git
- .cursorrules 納入版本控制
- 團隊成員自動同步配置
- 一致的回應品質
```

---

## 🔧 進階配置

### 多語言支援

雖然此技能專注於繁體中文，您可以修改提示詞支援雙語：

```
在系統提示詞最後加入：

當使用者明確要求英文回應時，可以提供英文翻譯，但主要回應仍使用繁體中文。
```

### 特定城市版本

針對特定城市建立專用版本：

```bash
# 台北市專用版
cp cross-platform/cursor/.cursorrules .cursorrules.taipei
# 編輯加入：特別注重台北市都市更新自治條例

# 新北市專用版
cp cross-platform/cursor/.cursorrules .cursorrules.newtaipei
# 編輯加入：特別注重新北市都市更新推動辦法
```

### 角色強化

強調特定專業角色：

```
# 強化法律顧問角色
在系統提示詞加入：
特別強調法律顧問角色，每次回應必須包含法律風險分析和合規檢查。

# 強化建築師角色
特別強調建築師角色，著重技術可行性和設計規範。

# 強化實施者角色
特別強調實施者角色，著重財務規劃和執行策略。
```

---

## 🐛 常見問題

### Q1: AI 回應簡體字
**A:** 在提示詞最前面加上：
```
‼️ 重要：必須使用繁體中文（台灣），嚴禁使用簡體字。每個字都必須是繁體。
```

### Q2: 沒有引用法條
**A:** 在問題中明確要求：
```
請引用具體法條編號回答我的問題
```

### Q3: 回應格式不正確
**A:** 提醒 AI：
```
請使用標準格式回答（包含📋現況分析、⚖️法規適用等章節）
```

### Q4: 回應太簡短
**A:** 要求更詳細：
```
請提供詳細完整的分析，包含所有相關法條和實務案例
```

### Q5: 回應太冗長
**A:** 要求精簡：
```
請簡潔回答，每個章節不超過3個要點
```

---

## 📝 貢獻與回饋

### 發現問題？
在 [GitHub Issues](https://github.com/yennanliu/UrbanRenewSkill/issues) 回報

### 想貢獻新平台支援？
1. Fork 專案
2. 在 `cross-platform/` 建立新平台目錄
3. 建立適配檔案和說明文件
4. 提交 Pull Request

### 建議改進？
在 [GitHub Discussions](https://github.com/yennanliu/UrbanRenewSkill/discussions) 討論

---

## 📄 授權

MIT License - 可自由使用與修改

---

## 🔗 相關連結

- **主專案：** [README.md](../README.md)
- **Claude Code 版本：** [.claude/skills/](../.claude/skills/)
- **使用範例：** [EXAMPLES.md](../.claude/skills/EXAMPLES.md)
- **安裝指南：** [INSTALLATION.md](../INSTALLATION.md)

---

**Version:** 1.0.0
**Last Updated:** 2024-02-24
**Maintained by:** Jerry Liu

**讓台灣都市更新專業知識在各個 AI 平台上都能發揮價值！** ✨
