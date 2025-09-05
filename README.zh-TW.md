# 🚀 AI 敏捷開發快速入門指南

🌐 [English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md)

**[BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD)** 是一個 AI 開發框架，就像一個 24/7 全天候在線的敏捷團隊——**分析師、專案經理、架構師、Scrum Master、開發人員、QA、產品負責人和使用者體驗專家**——隨時為你工作。

本快速入門指南旨在幫助你在幾分鐘內完成 **Gemini CLI + BMAD** 的設定，而無需翻閱大量文件。

💡 **最好的一點：完全免費**——任何人都可以用它來 *vibe code*。

## 📦 安裝步驟

1. **建立專案資料夾**  
   - 範例：`C:\projects\project_abc`

2. **安裝 Node.js 和 Git**  
   - 下載 [Node.js](https://nodejs.org/) 和 [Git](https://git-scm.com/)
   - Windows x64 直接下載連結：[node-v22.19.0-x64.msi](https://nodejs.org/dist/v22.19.0/node-v22.19.0-x64.msi) 和 [Git-2.51.0-64-bit.exe](https://github.com/git-for-windows/git/releases/download/v2.51.0.windows.1/Git-2.51.0-64-bit.exe)

3. **安裝 Gemini CLI、markdown-tree-parser 並設定 Git 使用者名稱以啟用自動存檔點**  
   ```bash
   npm install -g @google/gemini-cli @kayvan/markdown-tree-parser
   
   # 將 YourName 替換為你的名字
   git config --global user.name "YourName"
   ```

4. **安裝 BMAD-Method**  
   ```bash
   npx bmad-method install
   ```
   - 當提示 **"Enter the full path to your project directory where BMad should be installed"** 時，輸入你在 **步驟 1** 建立的專案資料夾路徑。
   - 當提示 **"Which IDE(s) do you want to configure?"** 時，選擇 `Gemini CLI`。
   - 其他提示直接按 Enter 使用預設值。

5. **執行 Gemini CLI 並啟用自動存檔點**  
   ```bash
   gemini --checkpointing
   ```

6. **登入 Gemini CLI**  
   - 選擇 **"Login with Google"** 並使用你的 Google 帳號登入。

7. **更改回覆語言**  
   - 讓 Gemini 使用中文回覆
      ```bash
      /memory add Always respond in Traditional Chinese.
      ```
   - 如要撤銷此設定，可以編輯或刪除 Gemini CLI 的記憶檔案
      ```bash
      %userprofile%\.gemini\GEMINI.md
      ```

## 🛠 使用方法

1. 先與 **BMAD Orchestrator** 對話——它會一步步引導你完成整個 BMAD 流程  
   - 啟動 **BMAD Orchestrator**
      ```bash
      *bmad-orchestrator
      ```

   - 它是你的 BMAD 導師——你可以這樣問  
      ```bash
      教我如何使用 BMAD，我想開發一個 XXX 應用。
      ```

2. 隨時查看可用指令清單  
   ```bash
   *help
   ```

3. 當你不確定下一步該做什麼時，找 **BMAD Orchestrator** 問問

## 📋 Gemini CLI 常用指令與快捷鍵

### **指令**
| 指令 | 描述 |
|------|------|
| `/init` | 分析當前目錄並生成目錄説明檔案 |
| `/chat` | 儲存聊天會話以便稍後恢復（例如重啟後） |
| `/memory` | 儲存重要資訊（例如更改語言） |
| `/restore` | 將專案回滾到某個存檔點（需要 `gemini --checkpointing`） |
| `/copy` | 複製上一個回覆 |
| `/help` | 顯示 Gemini CLI 的説明資訊 |
| `/settings` | 開啟 Gemini CLI 設定 |
| `/stats` | 顯示當前會話的統計資訊 |
| `/corgi` | 切換狗狗模式 ▼(´ᴥ`)▼ |

### **快捷鍵**
| 快捷鍵 | 操作 |
|--------|------|
| `Ctrl+O` | 切換除錯主控台 |
| `Ctrl+S` | 切換長回覆完整顯示 |
| `Ctrl+T` | 切換工具描述顯示 |
| `Ctrl+Y` | 切換自動批准（YOLO 模式） |
| `Ctrl+X` | 在記事本中開啟當前輸入 |
| `!` | 切換到 Shell 模式（當輸入為空時） |
| `\` + `Enter` | 插入新行 |

---

**GitHub 倉庫：** [`ai-agile-quickstart`](https://github.com/TheJYU/ai-agile-quickstart)  
