# GitHub Copilot Plans Overview

> Learning Objective: Distinguish between all GitHub Copilot plan tiers, identify which audiences each targets, and describe the full range of ways a developer can invoke Copilot assistance.

[Home](../../README.md) | [Domain Index](./README.md) | [Previous](./README.md) | [Next](./copilot-individual.md)

## Exam Relevance

- Domain weight: 31%
- Why it matters: Domain 2 is the highest-weighted section of the GH-300 exam at 31%. A solid grasp of the plan landscape is the prerequisite for every other feature question: you must know which tier unlocks which capability before answering scenario questions about specific features. Exam items frequently require you to select the right plan for a described scenario or identify which trigger mode a developer is using.

## Key Concepts

- **Six plan tiers:** GitHub Copilot is available as Free, Student, Pro, Pro+, Business, and Enterprise — each offering a progressively larger feature set and designed for a different buyer.
- **Individual plans** (Free, Student, Pro, Pro+) are self-managed on a personal GitHub account; no organisation admin involvement is needed.
- **Organisational plans** (Business and Enterprise) are managed by an organisation or enterprise owner who assigns seats to members.
- **Copilot in the IDE** is the editor extension installed in VS Code, JetBrains IDEs, Visual Studio, Neovim, Eclipse, Xcode, or Azure Data Studio. It delivers both ghost-text inline completions and the embedded Chat panel.
- **Copilot Chat in the IDE** is the conversational AI sidebar inside the editor — distinct from passive ghost-text completions — where developers ask questions in natural language and receive code, explanations, or command suggestions.
- **Trigger modes** are the distinct ways a developer can invoke Copilot: inline suggestions (ghost text), inline Chat, the Chat panel, GitHub.com Chat (Enterprise), the CLI extension, and via the GitHub mobile app.
- **Copilot for non-GitHub customers** — developers on platforms that are not GitHub.com can access AI completions through the VS Code GitHub Copilot extension authenticated with a GitHub account, but organisation-level governance requires GitHub.com.
- **Premium requests** are a metered resource (used for advanced models and agentic features); each plan tier provides a different monthly allowance.

## Visual Model

```mermaid
flowchart TD
    A[Developer needs AI assistance] --> B{Account type?}
    B -->|Personal| C{Usage level?}
    B -->|Team / Org| D{Enterprise Cloud?}

    C -->|Occasional / free| E[Copilot Free\nLimited completions & chat]
    C -->|Verified student| F[Copilot Student\nUnlimited completions + premium models]
    C -->|Professional paid| G[Copilot Pro\nUnlimited completions + cloud agent]
    C -->|Power user| H[Copilot Pro+\nHighest premium request allowance\nAll models]

    D -->|No - GitHub Free or Team| I[Copilot Business\nOrg policy + audit logs + file exclusions]
    D -->|Yes - GitHub Enterprise Cloud| J[Copilot Enterprise\nAll Business features +\nGitHub.com Chat, PR summaries,\nKnowledge Bases, custom models]

    E & F & G & H --> K[IDE completions\nCopilot Chat IDE\nCLI\nMobile]
    I --> K
    I --> L[Org-wide policy\nAudit logs]
    J --> K
    J --> L
    J --> M[GitHub.com Chat\nPR Summaries\nKnowledge Bases]
```

Notes:
- The left branch (Free → Pro+) covers individual developers; billing is on a personal account.
- The right branch (Business / Enterprise) requires an organisation owner to assign seats and configure policies.
- Enterprise is only purchasable alongside GitHub Enterprise Cloud (GHEC); Business can be purchased independently.
- Every paid plan includes IDE completions and the CLI extension; GitHub.com Chat is exclusive to Enterprise.

## Quick Recap

- Six plan tiers exist: Free, Student, Pro, Pro+, Business, Enterprise — moving from self-serve individual to enterprise-grade with governance tools.
- Individual plans are account-managed; Business and Enterprise are org/enterprise-managed with seat assignment.
- Copilot Enterprise is exclusively for GitHub Enterprise Cloud organisations and adds GitHub.com Chat, PR summaries, and Knowledge Bases on top of all Business features.
- Developers can trigger Copilot through: ghost-text inline suggestions, inline Chat (`Ctrl+I`), the Chat panel, GitHub.com Chat (Enterprise only), the CLI extension, and mobile.
- Copilot Free includes limited completions; Student, Pro, and Pro+ include unlimited completions with increasing premium-request allowances.

## Sources Consulted

- https://docs.github.com/en/copilot/get-started/plans
- https://docs.github.com/en/copilot/get-started/features
- https://docs.github.com/en/copilot/using-github-copilot/getting-code-suggestions-in-your-ide-with-github-copilot
- https://docs.github.com/en/copilot/github-copilot-in-the-cli/about-github-copilot-in-the-cli

## References

- Facts referenced; explanations are original.
- https://docs.github.com/en/copilot/get-started/plans
- https://docs.github.com/en/copilot/get-started/features

[Home](../../README.md) | [Domain Index](./README.md) | [Previous](./README.md) | [Next](./copilot-individual.md)
