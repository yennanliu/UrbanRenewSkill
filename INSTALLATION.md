# 安裝與測試指南

## 快速安裝

### 選項 1：直接在此專案使用（最簡單）

技能檔案已經在 `.claude/skills/` 目錄中，Claude Code 會自動載入。

```bash
# 確認您在專案目錄
cd /Users/jerryliu/UrbanRenewSkill

# 啟動 Claude Code
claude-code

# 技能已自動載入！開始提問即可
```

### 選項 2：安裝到全域 Claude 目錄

將技能安裝到全域，在任何專案都能使用：

```bash
# 建立全域技能目錄（如果不存在）
mkdir -p ~/.claude/skills

# 複製技能檔案
cp -r .claude/skills/* ~/.claude/skills/

# 驗證安裝
ls ~/.claude/skills/taiwan-urban-renewal.md
```

完成後，在任何專案目錄執行 `claude-code` 都能使用此技能。

### 選項 3：符號連結（開發者模式）

適合需要頻繁修改技能檔案的開發者：

```bash
# 建立符號連結
ln -s /Users/jerryliu/UrbanRenewSkill/.claude/skills/taiwan-urban-renewal.md ~/.claude/skills/

# 驗證連結
ls -la ~/.claude/skills/taiwan-urban-renewal.md
```

修改原始檔案會立即生效，無需重新複製。

## 測試技能

### 基礎測試

啟動 Claude Code 後，嘗試以下問題：

#### 測試 1：同意門檻查詢
```
問：我們社區在台北市，想推動都更需要多少住戶同意？
```

**預期回應：**
- 應引用《都市更新條例第22條》
- 區分「劃定」與「非劃定」更新地區
- 列出四項同意門檻（人數、面積）
- 使用結構化格式（📋📊⚖️💡等標記）

#### 測試 2：容積獎勵計算
```
問：申請綠建築和智慧建築獎勵，最多可以拿到多少容積？
```

**預期回應：**
- 應有詳細計算表格
- 引用台北市自治條例
- 說明總上限（基準容積50%）
- 提供成本效益分析

#### 測試 3：比較分析
```
問：危老重建跟都更有什麼差別？
```

**預期回應：**
- 應有比較表格
- 列出至少10項比較項目
- 提供選擇建議
- 包含財務試算範例

### 進階測試

#### 測試 4：案件評估
```
問：請評估以下條件是否適合都更：
- 地點：台北市大安區
- 基地面積：800㎡
- 建物屋齡：35年
- 住戶數：30戶
- 目前同意率：70%
```

**預期回應：**
- 完整現況分析
- 法規適用判斷
- 具體建議（危老或都更）
- 後續步驟說明

#### 測試 5：文件起草
```
問：請幫我起草一份都市更新的所有權人通知書範本
```

**預期回應：**
- 正式公文格式
- 包含必要法定資訊
- 繁體中文專業用語
- 符合台灣公文慣例

## 驗證技能載入

### 方法 1：直接測試
啟動 Claude Code 後，輸入：
```
你是誰？你有什麼專業能力？
```

如果技能正確載入，應該回應：
```
我是都市更新全方位顧問，整合了實施者、建築師與法律顧問的專業視角...
```

### 方法 2：檢查檔案
確認技能檔案存在：
```bash
# 檢查本地技能
ls -lah .claude/skills/

# 或檢查全域技能
ls -lah ~/.claude/skills/
```

應該看到：
- `taiwan-urban-renewal.md` (約 10KB)
- `skill.json` (約 3KB)
- `README.md` (約 4KB)
- `EXAMPLES.md` (約 15KB)

## 常見問題排解

### Q1: 技能沒有載入
**解決方法：**
1. 確認檔案在正確位置：
   ```bash
   ls .claude/skills/taiwan-urban-renewal.md
   ```
2. 檢查檔案權限：
   ```bash
   chmod 644 .claude/skills/*.md
   ```
3. 重新啟動 Claude Code

### Q2: 回應不是繁體中文
**可能原因：**
- 技能檔案未正確載入
- 使用的模型不支援繁體中文

**解決方法：**
- 確認使用 Claude 3.5 Sonnet 或更高版本
- 明確要求：「請用繁體中文回答」

### Q3: 法規引用不精確
**可能原因：**
- 技能定義檔案版本過舊
- 台灣法規已更新

**解決方法：**
- 檢查 CHANGELOG.md 確認版本
- 查看是否有更新版本
- 向維護者回報法規更新

### Q4: 技能在其他專案無法使用
**解決方法：**
- 使用選項2（全域安裝）：
  ```bash
  cp -r .claude/skills/* ~/.claude/skills/
  ```

## 更新技能

### 更新本地版本
```bash
cd /Users/jerryliu/UrbanRenewSkill
git pull origin main
```

### 更新全域安裝
```bash
cd /Users/jerryliu/UrbanRenewSkill
git pull origin main
cp -r .claude/skills/* ~/.claude/skills/
```

## 效能優化

### 減少載入時間
如果技能載入較慢，可以：

1. **只安裝核心檔案：**
   ```bash
   cp .claude/skills/taiwan-urban-renewal.md ~/.claude/skills/
   cp .claude/skills/skill.json ~/.claude/skills/
   ```

2. **使用符號連結：**
   ```bash
   ln -s $(pwd)/.claude/skills/taiwan-urban-renewal.md ~/.claude/skills/
   ```

## 驗證檢查清單

安裝完成後，請確認：

- [ ] 檔案存在於 `.claude/skills/` 或 `~/.claude/skills/`
- [ ] 啟動 Claude Code 無錯誤訊息
- [ ] 提問都更相關問題，收到繁體中文回應
- [ ] 回應中包含具體法條引用（如「都市更新條例第22條」）
- [ ] 回應使用結構化格式（📋📊⚖️💡⚠️📝等標記）
- [ ] 回應包含專業術語（權利變換、協議合建、容積獎勵等）

## 技術支援

如果遇到問題：

1. **查看範例：** 閱讀 `.claude/skills/EXAMPLES.md`
2. **檢查版本：** 查看 `CHANGELOG.md`
3. **提交問題：** 到 GitHub Issues 回報
4. **聯繫維護者：** jerry@example.com

---

## 快速參考卡

```bash
# 安裝
cp -r .claude/skills/* ~/.claude/skills/

# 啟動
claude-code

# 測試
問：我們社區要推動都更，需要多少同意？

# 更新
git pull && cp -r .claude/skills/* ~/.claude/skills/

# 檢查
ls -lah ~/.claude/skills/taiwan-urban-renewal.md
```

---

**安裝完成後，享受專業的都市更新諮詢服務！** 🏗️✨
