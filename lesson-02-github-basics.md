# 第二課：GitHub 基本操作

**日期**：2026-06-09  
**狀態**：✅ 完成

---

## 核心概念

**Repository（Repo）** — 一個專案的資料夾，存在 GitHub 雲端上

**Clone** — 把雲端的 Repo 下載到你的電腦

**Commit** — 儲存一個「版本快照」（像 Word 的存檔）

**Push** — 把本地改動上傳回雲端

---

## 安裝工具

### Homebrew（Mac 套件管理器）
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### GitHub CLI
```bash
brew install gh
```

### 登入 GitHub
```bash
gh auth login
# 選擇：GitHub.com → HTTPS → Login with a web browser
```

---

## 基本操作流程

### Clone（下載 Repo 到電腦）
```bash
git clone https://github.com/用戶名/repo名稱.git
```

### 修改檔案後儲存版本
```bash
git add .                          # 把所有改動加入暫存區
git commit -m "說明這次改了什麼"    # 建立版本快照
git push                           # 上傳到 GitHub
```

### 從 GitHub 拉取最新版本
```bash
git pull
```

---

## 今日完成事項

- 建立 `ai-learning-journal` Repository
- Clone 到本地電腦（`~/Desktop/ai-learning-journal`）
- 新增 README.md 和第一課內容
- 成功 Push 到 GitHub
- 開啟 GitHub Pages，課程網站正式上線

**課程網站**：[https://harryho3308336-cpu.github.io/ai-learning-journal/](https://harryho3308336-cpu.github.io/ai-learning-journal/)

---

## 金融類比

| Git 概念 | 金融類比 |
|---------|---------|
| Repository | 一個基金的所有文件夾 |
| Commit | 每日 NAV 存檔記錄 |
| Branch | 投資策略的不同情境測試 |
| Push | 把報告提交給上級 |
| Pull | 從共享伺服器同步最新版本 |
