## Step 3: Expand Calculator Functionality

Duck wants to expand the calculator with additional operations by creating a new issue and working with Copilot CLI to implement the enhancements.

### 📖 Theory: Iterative Development with Copilot CLI

**Iterative Development and Agile Practices**

Modern software development follows iterative approaches where features are built incrementally:
- Start with a minimal viable product (MVP)
- Add features in small, manageable chunks
- Test and validate each addition
- Continuously improve based on feedback

**Maintaining Momentum with Copilot CLI**

The standalone Copilot CLI helps maintain development momentum by:
- Quickly generating code for new features using the latest AI models
- Suggesting best practices and patterns
- Helping debug and test new functionality
- Reducing context switching by keeping you in the terminal
- Handling long-running shell commands more efficiently
- Supporting improved automation with the headless `-p` mode

**Delegating Larger Tasks**

For more complex tasks, you can use the `/delegate` command:
```bash
copilot
> /delegate Add modulo, exponentiation, and square root functions to calculator.js with proper error handling
```

Copilot coding agent will:
1. Create a new branch automatically
2. Open a draft pull request
3. Work on the task autonomously
4. Stream output to your terminal
5. Request your review when complete

**Testing and Improvement Workflows**

As you add features, Copilot CLI can help you:
- Generate test cases for new operations
- Suggest edge cases to consider
- Create documentation
- Refactor code for better maintainability
- Save and share your development sessions using `/share`

### ⌨️ Activity: Add More Operations to the Calculator

1. Create a new issue for additional calculator operations:
   ```bash
   gh issue create --title "Add More Operations to Calculator" --template feature_request.md
   ```
   
   Fill in the template with details about adding modulo, exponentiation, and square root operations.

1. Work with Copilot CLI to implement the new operations:
   ```bash
   copilot -p "Add modulo, exponentiation (power), and square root functions to a Node.js calculator module. Include proper error handling for edge cases like negative square roots."
   ```

1. Or use an interactive session for more detailed guidance:
   ```bash
   copilot
   ```
   Then ask:
   ```
   Help me add these functions to my calculator.js:
   1. modulo(a, b) - returns the remainder of a divided by b
   2. power(base, exponent) - returns base raised to the exponent
   3. squareRoot(n) - returns the square root of n with error handling for negative numbers
   ```

1. Update your `calculator.js` file with the new functions

1. Test your new functions:
   ```bash
   node -e "const calc = require('./calculator'); console.log('5 % 2 =', calc.modulo(5, 2)); console.log('2 ^ 3 =', calc.power(2, 3)); console.log('√16 =', calc.squareRoot(16));"
   ```

1. Commit your changes:
   ```bash
   git add calculator.js
   git commit -m "Add modulo, power, and square root operations"
   git push
   ```

> [!TIP]
> Use `/share` in your Copilot CLI session to save your conversation as a Markdown file or GitHub gist for future reference!

> [!NOTE]
> Creating this second issue will complete the exercise and trigger the review workflow!

<details>
<summary>Having trouble? 🤷</summary><br/>

- Make sure your issue title includes "Calculator" or "Operations"
- The calculator.js file should export functions that can be required/imported
- You can test operations manually using Node.js REPL: `node` then type your code
- For square root of negative numbers, consider returning `NaN` or throwing an error
- Remember to commit and push any code changes you make
- Use `copilot --help` to see all available command options

</details>
