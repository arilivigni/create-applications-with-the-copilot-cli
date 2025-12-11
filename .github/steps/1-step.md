## Step 1: Install Copilot CLI and Use the Issue Template

Duck is getting ready to manage development for the Node.js calculator app and wants to install the standalone Copilot CLI and use the existing issue template to create a new issue.

### 📖 Theory: GitHub Copilot CLI - A Standalone Terminal Application

**What is GitHub Copilot CLI?**

GitHub Copilot CLI is a **standalone terminal application** that brings the power of GitHub Copilot directly to your command line. It is installed via npm and provides a rich interactive experience for developers.

Key capabilities include:
- Providing intelligent command suggestions powered by the latest AI models from OpenAI and Google
- Generating code snippets and scripts directly in your terminal
- Assisting with Git operations and GitHub interactions
- Supporting image inputs via paste and drag-and-drop for visual context
- Using the `/share` command to save chat sessions as Markdown files or GitHub gists
- Creating **custom agents** to encode specialized prompts and workflows
- Delegating tasks to **Copilot coding agent** using the `/delegate` command

**Installation Requirements**

To install Copilot CLI, you need:
- Node.js version 22 or later
- npm version 10 or later
- An active GitHub Copilot subscription (Pro, Pro+, Business, or Enterprise)

**Issue Templates**

Issue templates help maintain consistency when team members create issues. This repository already has a `feature_request.md` template that you'll use to create your calculator app issue. Templates ensure:
- All necessary information is captured upfront
- Issues follow a standard format
- The team can triage and respond to issues more efficiently

**References:**
- [Installing GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/set-up/install-copilot-cli)
- [Using GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli)
- [GitHub Copilot CLI 101](https://github.blog/ai-and-ml/github-copilot-cli-101-how-to-use-github-copilot-from-the-command-line/)

### ⌨️ Activity 1: Install the Standalone Copilot CLI

1. Open your Codespace (if not already open)
1. Install the standalone GitHub Copilot CLI by running:
   ```bash
   npm install -g @github/copilot
   ```
1. Verify the installation by running:
   ```bash
   copilot --version
   ```
1. Start Copilot CLI and authenticate with your GitHub account:
   ```bash
   copilot
   ```
   Follow the prompts to complete authentication if this is your first time.

> [!TIP]
> After installation, you can use the `copilot` command anywhere in your terminal to start an interactive session!

### ⌨️ Activity 2: Create an Issue Using Copilot CLI

1. Start an interactive Copilot CLI session:
   ```bash
   copilot
   ```

1. Ask Copilot CLI to help you create a feature request issue for the calculator app:
   ```
   Help me create a GitHub issue for a Node.js calculator app. I want to request a feature for basic arithmetic operations including addition, subtraction, multiplication, and division. The calculator should be implemented in calculator.js.
   ```

1. Copilot CLI will help you draft and create the issue. Follow the prompts to:
   - **Feature description**: Create a basic Node.js calculator with addition, subtraction, multiplication, and division operations
   - **Use case**: Learning to use Copilot CLI for code generation and development
   - **Additional context**: The calculator should be implemented in calculator.js

1. You can also use the `/delegate` command to have Copilot create the issue for you:
   ```
   /delegate Create a GitHub issue titled "Initial Node.js Calculator App" requesting basic arithmetic operations (add, subtract, multiply, divide) to be implemented in calculator.js
   ```

> [!NOTE]
> When you create the issue, the workflow will automatically verify your work and prepare the next step!

<details>
<summary>Having trouble? 🤷</summary><br/>

- Make sure you have Node.js 22+ installed: `node --version`
- If npm install fails, try: `sudo npm install -g @github/copilot`
- Make sure you have GitHub Copilot access enabled for your account
- If authentication fails, run `copilot` and follow the login prompts
- You can also create the issue through the GitHub UI if needed

</details>
