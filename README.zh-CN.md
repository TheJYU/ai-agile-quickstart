# 🚀 AI 敏捷开发快速入门指南

🌐 [English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md)

**[BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD)** 能将你的 LLM 打造成你专属的敏捷开发团队——**分析师、项目经理、架构师、Scrum Master、开发人员、QA、产品负责人和用户体验专家**——全天候为你效劳。

本快速入门指南旨在帮助你在几分钟内完成 **BMAD + Gemini CLI** 的设置，而无需翻阅大量文档。

💡 **最好的一点：完全免费**——任何人都可以用它来 *vibe code*。

## 📦 安装步骤

1. **创建项目文件夹**  
   - 示例：`C:\projects\project_abc`

2. **安装 Node.js 和 Git**  
   - 下载并安装 [Node.js](https://nodejs.org/) 和 [Git](https://git-scm.com/)
   - Windows x64 直接下载链接：[node-v22.19.0-x64.msi](https://nodejs.org/dist/v22.19.0/node-v22.19.0-x64.msi) 和 [Git-2.51.0-64-bit.exe](https://github.com/git-for-windows/git/releases/download/v2.51.0.windows.1/Git-2.51.0-64-bit.exe)

3. **安装 Gemini CLI、markdown-tree-parser 并配置 Git 用户名以启用[自动存档点](#命令)**  
   ```bash
   npm install -g @google/gemini-cli @kayvan/markdown-tree-parser
   
   # 将 YourName 替换为你的名字
   git config --global user.name "YourName"
   ```

4. **安装 BMAD-Method**  
   ```bash
   npx bmad-method install
   ```
   - 当提示 `Enter the full path to your project directory where BMad should be installed` 时，输入你在 **步骤 1** 创建的项目文件夹路径。
   - 当提示 `Which IDE(s) do you want to configure?` 时，按空格选择 `Gemini CLI` 后按回车。
   - 其他提示直接按回车使用默认值。

5. **运行 Gemini CLI 并启用自动存档点**  
   ```bash
   gemini --checkpointing
   ```

6. **登录 Gemini CLI**  
   - 选择 `Login with Google` 并使用你的 Google 账号登录。

7. **更改回复语言**  
   - 让 Gemini 使用中文回复
      ```bash
      /memory add Always respond in Chinese.
      ```
   - 如要撤销此设置，可以编辑或删除 Gemini CLI 的记忆文件 `%userprofile%\.gemini\GEMINI.md`

## 🛠 使用方法

1. 先与 **BMAD Orchestrator** 对话——它会一步步引导你完成整个 BMAD 流程  
   - 启动 **BMAD Orchestrator**
      ```bash
      *bmad-orchestrator
      ```

   - 它是你的 BMAD 导师——你可以这样问  
      ```bash
      教我如何使用 BMAD，我想开发一个 XXX 应用。
      ```

2. 你可以随时查看 BMAD 命令列表  
   ```bash
   *help
   ```

3. 当你不确定下一步该做什么时就找 **BMAD Orchestrator** 问问

## 📋 Gemini CLI 常用命令与快捷键

### **命令**
| 命令 | 描述 |
|------|------|
| `/init` | 分析当前目录并生成目录说明文件 |
| `/chat` | 保存聊天会话以便稍后恢复（例如重启后） |
| `/memory` | 保存重要信息（例如更改语言） |
| `/restore` | 将项目回滚到某个自动存档点（需要 `gemini --checkpointing`） |
| `/copy` | 复制上一个回复 |
| `/help` | 显示 Gemini CLI 帮助说明 |
| `/settings` | 打开 Gemini CLI 设置 |
| `/stats` | 显示当前会话的统计信息 |
| `/corgi` | 狗狗模式开关 ▼(´ᴥ`)▼ |

### **快捷键**
| 快捷键 | 操作 |
|--------|------|
| `Ctrl+O` | 调试控制台开关 |
| `Ctrl+S` | 长回复显示全部 |
| `Ctrl+T` | 工具描述开关 |
| `Ctrl+Y` | 自动批准开关（YOLO 模式） |
| `Ctrl+X` | 在记事本中打开当前输入 |
| `!` | 切换到 Shell 模式（当输入为空时） |
| `\` + `Enter` | 插入新行 |

---

**GitHub 仓库：** [`ai-agile-quickstart`](https://github.com/TheJYU/ai-agile-quickstart)  
