# 🚀 AI Agile Quickstart

The **BMAD-METHOD** is an AI framework that works like an always‑on agile team — **Analyst, PM, Architect, Scrum Master, Developer, QA, Product Owner, and UX Expert** — working for you 24/7.

This quick start guide is designed to help you set up **Gemini CLI + BMAD** in minutes, without needing to dig through the full documentation.

💡 **Best part:** Anyone can use this to *vibe code* — **100% free**.

## 📦 Setup

1. **Create a project folder**  
   - Example: `C:\projects\project_abc`

2. **Install Node.js & Git**  
   - Download [Node.js](https://nodejs.org/) and [Git](https://git-scm.com/)
   - Direct link for Windows x64: [node-v22.19.0-x64.msi](https://nodejs.org/dist/v22.19.0/node-v22.19.0-x64.msi) and [Git-2.51.0-64-bit.exe](https://github.com/git-for-windows/git/releases/download/v2.51.0.windows.1/Git-2.51.0-64-bit.exe)

3. **Install Gemini CLI, markdown-tree-parser & configure Git username for automatic checkpoints**  
   ```bash
   npm install -g @google/gemini-cli @kayvan/markdown-tree-parser
   
   # Replace YourName with your Git username
   git config --global user.name "YourName"
   ```

4. **Install BMAD Method**  
   ```bash
   npx bmad-method install
   ```
   - When asked to **"Enter the full path to your project directory where BMad should be installed"**, provide your project folder created in **Step 1**.
   - When asked **"Which IDE(s) do you want to configure?"**, select `Gemini CLI`.
   - For all other prompts, simply press Enter to accept the default values.

5. **Run Gemini CLI & enable automatic checkpoints**  
   ```bash
   gemini --checkpointing
   ```

6. **Login to Gemini CLI**  
   - Select **"Login with Google"** and sign in with your Google account.

7. **Change response language**  
   - To make Gemini respond in a different language
      ```bash
      /memory add Always respond in <language>.
      ```
   - To undo this, edit or delete the Gemini CLI memory file
      ```bash
      %userprofile%\.gemini\GEMINI.md
      ```

## 🛠 Usage

1. Start by talking to the **BMAD Orchestrator** — it guides you through the entire BMAD process step‑by‑step  
   - Activate the **BMAD Orchestrator**
      ```bash
      *bmad-orchestrator
      ```

   - This is your BMAD teacher — you can ask  
      ```bash
      Teach me to use BMAD, I want to build a XXX app.
      ```

2. At any time, you can view a list of available commands  
   ```bash
   *help
   ```

3. Whenever you’re unsure what to do next, ask the **BMAD Orchestrator**, it will guide you step‑by‑step in building your project.

## 📋 Useful Commands & Keyboard Shortcuts for Gemini CLI

### **Commands**
| Command | Description |
|---------|-------------|
| `/init` | Analyzes the current directory and generates a tailored context file. |
| `/chat` | Save a chat session for later (e.g., after reboot). |
| `/memory` | Save important facts (e.g., preferred language). |
| `/restore` | Roll back project to a checkpoint (requires `gemini --checkpointing`). |
| `/copy` | Copy the last response. |
| `/help` | Display help information about Gemini CLI. |
| `/settings` | Open Gemini CLI settings. |
| `/stats` | Show statistics for the current session. |
| `/corgi` | Toggle doggo. ▼(´ᴥ`)▼ |

### **Keyboard Shortcuts**
| Shortcut | Action |
|----------|--------|
| `Ctrl+O` | Toggle debug console. |
| `Ctrl+S` | Print long responses without truncation. |
| `Ctrl+T` | Toggle tool descriptions. |
| `Ctrl+Y` | Toggle auto‑approval (YOLO mode). |
| `Ctrl+X` | Open current input in Notepad. |
| `!` | Toggle shell mode (when input is empty). |
| `\` + `Enter` | Insert a newline. |

---

**Repository:** [`ai-agile-quickstart`](https://github.com/TheJYU/ai-agile-quickstart)
