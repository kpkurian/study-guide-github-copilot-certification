# GitHub Copilot Chat

> Learning Objective: Identify high-value use cases for Copilot Chat, apply techniques to improve response quality, recognise Chat's limitations, use code suggestions effectively, master slash commands, and follow best practices including how to share feedback.

[Home](../../README.md) | [Domain Index](./README.md) | [Previous](./copilot-enterprise.md) | [Next](./copilot-cli.md)

## Exam Relevance

- Domain weight: 31%
- Why it matters: Copilot Chat is the conversational surface that developers interact with daily, and the exam tests detailed knowledge of its capabilities, slash commands, and limitations. Scenarios often describe a task and ask which Chat approach or command is most appropriate, making this a high-frequency question area.

## Key Concepts

- **Copilot Chat** is the conversational AI interface embedded in IDEs (VS Code, JetBrains, Visual Studio, Eclipse, Xcode), on GitHub.com (Enterprise), and in the GitHub mobile app.
- **Three Chat modes in VS Code:** Ask mode (Q&A and code suggestions), Plan mode (detailed implementation plans before any code changes), and Agent mode (autonomous multi-step task execution with file edits and terminal commands).
- **Slash commands** are shorthand directives prefixed with `/` that instruct Chat to perform a specific category of task without needing a full natural-language prompt.
- **Chat context** determines response quality: attaching relevant files (`#file:`), mentioning variables (`#variable:`), specifying the active editor, or selecting a code block before asking dramatically improves relevance.
- **Limitations:** Copilot Chat may produce confidently-stated but incorrect answers (hallucinations), has a finite context window, may not be aware of recent library updates, and cannot access the internet (unless using a web-search-enabled model or tool).
- **Code suggestion options:** Copilot Chat can return code inline in the response; from there, developers can (1) copy it manually, (2) use the "Insert at cursor" button, (3) create a new file from the suggestion, or (4) insert it into the terminal.
- **Feedback:** Developers can use 👍/👎 rating buttons on individual responses, the `/feedback` command (in some interfaces), or the **Help → Report Issue** path in VS Code to report problems.

## Visual Model

```mermaid
flowchart TD
    subgraph ChatModes["Copilot Chat — Three Modes (VS Code)"]
        A[Ask Mode\nAnswer questions\nGet code snippets\nExplain concepts] 
        B[Plan Mode\nCreate detailed implementation plan\nNo code changes until approved]
        C[Agent Mode\nAutonomously edits files\nRuns terminal commands\nIterates until task complete]
    end

    subgraph SlashCommands["Key Slash Commands"]
        D[/explain — Explain selected code]
        E[/fix — Suggest a bug fix]
        F[/tests — Generate unit tests]
        G[/doc — Add documentation comments]
        H[/simplify — Simplify selected code]
        I[/feedback — Submit feedback]
    end

    subgraph ContextAttachments["Context Attachment Options"]
        J["#file: — Attach a specific file"]
        K["#selection — Use highlighted code"]
        L["#codebase — Search entire codebase"]
        M["@workspace — Reference whole workspace"]
    end

    subgraph CodeSuggestionOptions["Code Suggestion Actions"]
        N[Copy to clipboard]
        O[Insert at cursor]
        P[Create new file]
        Q[Insert into terminal]
    end
```

Notes:
- Ask mode is the default and covers most day-to-day Q&A tasks.
- Plan mode is designed for large tasks: it researches requirements, drafts a plan, and waits for approval before writing any code.
- Agent mode is the most autonomous — it may run commands and modify multiple files; always review actions before approving.
- Slash commands work in the Chat panel, inline Chat, and (where supported) GitHub.com Chat.

## Practical Examples and Scenarios

### Example 1: Using `/explain` on a complex algorithm

- Context: A developer inherits a 100-line sorting algorithm with no comments. They want to understand the logic before modifying it.
- Action: They highlight the entire function in VS Code, open the Chat panel, and type `/explain`.
- Outcome: Copilot provides a step-by-step natural language explanation of the algorithm, identifies the design pattern used, and points out the time complexity — all without the developer needing to reverse-engineer the logic manually.

### Example 2: Improving Chat performance by providing context

- Context: A developer asks "How should I handle errors here?" and gets a generic error-handling example that doesn't match their stack.
- Action: They refine the prompt by: (1) selecting the specific function first, (2) attaching the config file with `#file:config.ts`, and (3) specifying the framework: "How should I handle errors here for an Express.js route that returns JSON responses?"
- Outcome: Copilot returns a pattern specifically tailored to Express.js JSON APIs, including status codes and error-response structure — dramatically more useful than the generic initial answer.

### Example 3: Generating unit tests with `/tests`

- Context: A developer has just written a utility function for currency formatting and wants to create a test suite quickly.
- Action: They highlight the function, open Chat, and type `/tests`. They also specify "use Jest and cover edge cases like null, zero, and negative values."
- Outcome: Copilot generates a Jest test file with describe/it blocks covering the specified edge cases, ready to be dropped into the test directory.

### Example 4: Handling a Chat limitation — outdated library knowledge

- Context: A developer asks Copilot Chat for the correct syntax for a method that changed in a major version upgrade released last month. Copilot provides the old syntax.
- Action: The developer recognises that Chat's training data has a knowledge cutoff and cross-checks the answer with the official library changelog.
- Outcome: The developer finds the correct new syntax, corrects the suggestion, and updates their custom instructions to include a note about the library version they're using — preventing the same issue in future sessions.

## Hands-on Practice Checklist

- [ ] Select a complex function in your codebase, open Copilot Chat, and run `/explain` — review the quality of the explanation.
- [ ] Introduce a deliberate bug in a small function, then use `/fix` and observe whether Copilot identifies the issue.
- [ ] Use `/tests` on a utility function and specify a testing framework (e.g., "use Pytest with parametrize").
- [ ] Use `/doc` on a function that lacks docstrings and review the generated documentation.
- [ ] Try attaching a file with `#file:` to a prompt and compare the response quality to a prompt without that context.
- [ ] Click the 👍 or 👎 button on a Copilot Chat response and note where the feedback UI is located.
- [ ] Switch between Ask, Plan, and Agent modes in VS Code's Chat panel using the mode selector at the bottom.

## Common Mistakes and Troubleshooting

- Mistake: Trusting Copilot Chat output without validation, especially for security-sensitive code.
  Fix: Always review and test generated code. Chat can produce confident but incorrect or insecure output. Human review is mandatory for production code.

- Mistake: Sending vague prompts like "fix this" without context.
  Fix: Provide specific context — select the relevant code, attach related files, and describe the expected behaviour. The more specific the prompt, the more useful the response.

- Mistake: Expecting Chat to know about libraries or APIs released after its training cutoff.
  Fix: For recent updates, paste in the relevant documentation section directly into the prompt or cross-reference with official docs. Custom instructions can also note the library version.

- Mistake: Using Agent mode for simple, quick tasks.
  Fix: Agent mode is powerful but consumes premium requests and executes multiple autonomous actions. For quick code edits or explanations, Ask mode is faster and more efficient.

- Mistake: Ignoring the "Used N references" indicator at the top of Chat responses.
  Fix: Click the indicator to see exactly which files Copilot used as context. If the wrong files are being referenced, use explicit `#file:` attachments to guide it.

## Quick Recap

- Copilot Chat has three modes: Ask (Q&A), Plan (design-first, no code until approved), Agent (autonomous multi-step execution).
- Slash commands accelerate common tasks: `/explain`, `/fix`, `/tests`, `/doc`, `/simplify`, `/feedback`.
- Context quality drives response quality — use `#file:`, `#selection`, `#codebase`, and `@workspace` to anchor answers.
- Code suggestions can be: copied, inserted at cursor, saved to a new file, or inserted into the terminal.
- Key limitations: training data cutoff (no real-time knowledge), finite context window, potential for hallucinations, no internet access by default.
- Feedback can be given via 👍/👎 on individual responses or through in-IDE reporting tools.

## Practice Questions

1. A developer wants to understand a complex regular expression they found in a legacy codebase. Which Copilot Chat slash command is most appropriate?
   - Answer: `/explain`
   - Rationale: The `/explain` command instructs Copilot to provide a natural-language breakdown of selected code, making it ideal for decoding complex or unfamiliar logic like regular expressions.

2. Which Chat mode should a developer use when they want Copilot to create a detailed plan for a large feature implementation and review it before any code changes are made?
   - Answer: Plan mode.
   - Rationale: Plan mode is designed specifically for this workflow — Copilot researches the task, drafts a structured plan, and waits for developer approval before executing any code changes.

3. A developer receives a code block from Copilot Chat and wants to run it directly as a shell command without leaving the Chat panel. Which action should they choose?
   - Answer: "Insert into terminal" (the terminal insert action on the code block).
   - Rationale: Chat code blocks provide multiple insertion actions; "Insert into terminal" sends the code directly to the integrated terminal, ideal for shell commands or CLI instructions.

4. A developer asks Copilot Chat "what is the correct import syntax for Pydantic v2?" and receives an answer that refers to Pydantic v1 syntax. What is the most likely cause?
   - Answer: Copilot's training data has a knowledge cutoff and may not include information about the version change in Pydantic v2.
   - Rationale: Large language models are trained on data up to a specific date. If a library released a breaking change after the training cutoff, Copilot may not know about it. The developer should consult official documentation to verify.

## Originality Declaration

- This page was written as original instructional content.
- No protected source text was copied verbatim.

## Sources Consulted

- https://docs.github.com/en/copilot/get-started/features
- https://docs.github.com/en/copilot/using-github-copilot/asking-github-copilot-questions-in-your-ide
- https://docs.github.com/en/copilot/using-github-copilot/asking-github-copilot-questions-in-github

## Potential Similarity Risk

- Risk level: Low
- Notes: Slash command names (`/explain`, `/fix`, `/tests`, `/doc`) are product feature names that must be reproduced accurately. Mode names (Ask, Plan, Agent) are product terms. All descriptions, examples, and scenarios are independently written.

## References

- Facts referenced; explanations are original.
- https://docs.github.com/en/copilot/using-github-copilot/asking-github-copilot-questions-in-your-ide
- https://docs.github.com/en/copilot/get-started/features

[Home](../../README.md) | [Domain Index](./README.md) | [Previous](./copilot-enterprise.md) | [Next](./copilot-cli.md)
