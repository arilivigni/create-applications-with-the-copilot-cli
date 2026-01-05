## Step 2: Work on the Calculator Issue with Copilot CLI

With the issue created, Duck works with the standalone Copilot CLI interactively to start building the calculator application.

### 📖 Theory: Collaborative Development with Copilot CLI

#### Interactive Development with Copilot CLI

The standalone Copilot CLI (`copilot` command) provides a rich interactive experience for development:

- Start a session by simply running `copilot` in your terminal
- Have natural conversations about your code and get intelligent suggestions
- Generate boilerplate code based on your requirements
- Use the latest AI models for cutting-edge responses
- Share your session using the `/share` command to save as Markdown or a gist

#### Custom Agents

Copilot CLI supports custom agents that you can define in your repository:

- Create agent profiles in `.github/agents/` directory
- Encode specialized prompts, tool selections, and workflows
- Invoke agents using `/agent <name>` command
- Great for documentation, infrastructure, security, or domain-specific tasks

#### Delegating Tasks

When you have larger tasks, you can delegate them to Copilot coding agent:

- Use `/delegate TASK-DESCRIPTION` to assign work
- Copilot creates a new branch and draft pull request
- The coding agent works autonomously in the background
- Review the changes when complete

> [!TIP]
> Use the `/share` command to save your Copilot CLI chat sessions as Markdown files or GitHub gists for future reference!

> [!NOTE]
> References:
>
> - [Using GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli)
> - [Custom agents in Copilot CLI](https://github.blog/changelog/2025-10-28-github-copilot-cli-use-custom-agents-and-delegate-to-copilot-coding-agent/)
> - [About custom agents](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-custom-agents)

### ⌨️ Activity: Create a New Branch for the Calculator App

1. Create and push a new branch called `create-calc-app`:

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > copilot -p "Create and push a new branch called 'create-calc-app'"
   > ```

> [!TIP]
> Use the `!` command in Copilot CLI to execute shell commands directly from your chat session!

### ⌨️ Activity: Generate Calculator Code with Copilot CLI

1. Save this image locally as `node-js-calculator.png` to use as a visual reference for the calculator interface:

   > [!TIP]
   > Right-click the image below and select "Save image as..." to save it locally as `node-js-calculator.png`:

   <img alt="Node.js calculator CLI interface showing the command prompt and available operations" src="https://github.com/user-attachments/assets/330a5086-e74e-4c54-bead-91c7a9d93997" width="400">

1. Start an interactive Copilot CLI session:

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > copilot
   > ```

1. Ask Copilot CLI to help you create the calculator functions:

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > @node-js-calculator.png help me create a Node.js calculator app based on
   > this image and all the math operations shown.
   > Make sure to create the "src" directory and put all the app code there.
   > ```

1. Alternatively, use the headless mode with a prompt:

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > copilot -p "@node-js-calculator.png help me create
   > a Node.js calculator app based on this image
   > and all the math operations shown.
   > Make sure to create the 'src' directory and put all the app code there."
   > ```

1. Update your `calculator.js` file with the generated code. You can also ask Copilot for explanations:

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > copilot -p "Explain how module.exports works in Node.js"
   > ```

1. Test your calculator functions:

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > node -e "const calc = require('./calculator'); console.log('2 + 3 =', calc.add(2, 3)); console.log('10 - 4 =', calc.subtract(10, 4));"
   > ```

1. Commit your changes:

   > ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)
   >
   > ```prompt
   > git add calculator.js
   > git commit -m "Implement basic calculator operations"
   > git push
   > ```

> [!TIP]
> You can paste or drag-and-drop images into Copilot CLI to provide visual context for your questions!

> [!NOTE]
> Pushing your changes will trigger the workflow to verify your work and prepare the next step!

<details>
<summary>Having trouble? 🤷</summary><br/>

- Make sure you're in the repository directory when running commands
- The `copilot` command requires Node.js 22+ to be installed
- If authentication fails, run `copilot` and follow the login prompts
- You can also edit the calculator.js file manually based on Copilot's suggestions
- Remember to export your functions using `module.exports`

</details>
