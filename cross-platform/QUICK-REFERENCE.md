# Quick Reference Card - 快速參考卡

> 一頁搞定所有 AI 平台設定

---

## 🎯 60 秒設定指南

### Cursor
```bash
cp cross-platform/cursor/.cursorrules .cursorrules
```
✅ 完成！開啟 Cursor，按 Cmd+K 開始使用

---

### GitHub Copilot
```bash
mkdir -p .github
cp cross-platform/copilot/copilot-instructions.md .github/
```
✅ 完成！在 Copilot Chat 輸入 `@workspace` 開始使用

---

### Gemini CLI
```bash
alias urban='gemini chat --system-instruction="$(cat cross-platform/gemini/gemini-system-instruction.txt)"'
urban
```
✅ 完成！

---

### ChatGPT
1. 開啟 [ChatGPT](https://chat.openai.com)
2. Settings → Custom Instructions
3. 貼上 `cross-platform/universal/system-prompt.md` 中的系統提示詞
✅ 完成！

---

### Claude.ai
1. 開啟 [Claude.ai](https://claude.ai)
2. Projects → New Project
3. 上傳 `cross-platform/universal/system-prompt.md`
✅ 完成！

---

## 📋 測試檢查清單

複製以下問題測試：

```
✓ 我們社區在台北市，想推動都更需要多少住戶同意？
✓ 容積獎勵最高可以拿到多少？
✓ 請用表格比較危老重建和都更的差異
```

預期回應特徵：
- ✅ 繁體中文
- ✅ 包含 📋📊⚖️💡⚠️📝 標記
- ✅ 引用具體法條編號
- ✅ 結構化格式

---

## 🔧 檔案位置速查

| 平台 | 配置檔案 | 位置 |
|------|---------|------|
| Claude Code | `taiwan-urban-renewal.md` | `.claude/skills/` |
| Cursor | `.cursorrules` | 專案根目錄 |
| Copilot | `copilot-instructions.md` | `.github/` |
| Gemini | `gemini-system-instruction.txt` | `cross-platform/gemini/` |
| 通用 | `system-prompt.md` | `cross-platform/universal/` |

---

## ⚡ 一鍵命令

### 設定所有平台
```bash
# Cursor
cp cross-platform/cursor/.cursorrules .cursorrules

# Copilot
mkdir -p .github && cp cross-platform/copilot/copilot-instructions.md .github/

# Gemini alias
echo 'alias urban-renewal="gemini chat --system-instruction=\"\$(cat ~/UrbanRenewSkill/cross-platform/gemini/gemini-system-instruction.txt)\""' >> ~/.zshrc
source ~/.zshrc
```

---

## 🆘 快速除錯

| 問題 | 解決方案 |
|------|---------|
| 簡體字 | 在問題開頭加上「請用繁體中文回答」 |
| 沒法條 | 加上「請引用具體法條編號」 |
| 太簡短 | 加上「請詳細說明」 |
| 太冗長 | 加上「請簡潔回答，每項3點內」 |
| 格式錯 | 加上「請用標準格式（📋📊⚖️💡⚠️📝）」 |

---

## 📞 需要幫助？

- 📖 完整文件：[README.md](README.md)
- 💡 使用範例：[EXAMPLES.md](../.claude/skills/EXAMPLES.md)
- 🐛 回報問題：[GitHub Issues](https://github.com/yennanliu/UrbanRenewSkill/issues)

---

**保存此頁面以便快速參考！** 🔖
