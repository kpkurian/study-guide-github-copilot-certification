# GitHub Copilot Enterprise

> Learning Objective: Explain the exclusive capabilities of Copilot Enterprise — including Copilot Chat on GitHub.com, PR summaries, Knowledge Bases, repository indexing, and custom models — and describe how each is configured and used.

[Home](../../README.md) | [Domain Index](./README.md) | [Previous](./copilot-business.md) | [Next](./copilot-chat.md)

## Exam Relevance

- Domain weight: 31%
- Why it matters: Copilot Enterprise is the most feature-rich plan and the one most likely to appear in exam scenario questions requiring you to identify which capability requires Enterprise (vs Business). Understanding Knowledge Bases, PR summaries, GitHub.com Chat, and custom models is essential for the highest-difficulty questions in Domain 2.

## Key Concepts

- **Copilot Enterprise** requires GitHub Enterprise Cloud (GHEC). It includes all Business features plus a set of platform-native capabilities that go beyond the IDE.
- **Copilot Chat on GitHub.com** — a conversational AI interface available directly on the GitHub website (not just in IDEs), allowing developers to ask questions in the context of repositories, pull requests, issues, and commits without leaving their browser.
- **Pull request summaries** — Copilot can auto-generate a structured description of a PR's changes (what was changed, which files are affected, what reviewers should focus on) to accelerate code review.
- **Repository indexing** — Copilot creates a semantic code search index for repositories to deliver context-enriched answers. Initial indexing can take up to 60 seconds for large repositories; subsequent updates are near-instant when a new conversation starts.
- **Knowledge Bases (Copilot Spaces)** — the mechanism for organising and centralising relevant content (repositories, documentation, specs, code examples) into a curated context that Copilot can draw from when answering questions. This improves response quality, consistency, and efficiency.
- **Knowledge types in a Knowledge Base:** source code snippets, best-practice documentation, design patterns, architecture decision records (ADRs), API specifications, internal style guides, and plain-text notes.
- **Custom models** — Enterprise allows organisations to fine-tune or configure Copilot to use models trained or adjusted on their own codebase, style, and conventions, improving relevance of completions in specialised domains.
- **Enterprise-level policy control** — Enterprise owners can set policies that cascade down to all organisations in the enterprise and cannot be overridden at the organisation level.

## Visual Model

```mermaid
flowchart TD
    subgraph EnterpriseExclusive["Copilot Enterprise — Exclusive Features"]
        A[Copilot Chat on GitHub.com\nRepository / PR / issue context\nNo IDE required]
        B[PR Summaries\nAuto-generated description\nChanges + reviewer focus areas]
        C[Knowledge Bases / Copilot Spaces\nCurated context repositories\nDocs, code, specs, patterns]
        D[Repository Indexing\nSemantic code search\nUp-to-date within seconds]
        E[Custom Models\nFine-tuned on org codebase\nImproves specialised completions]
    end

    subgraph KBTypes["Knowledge Base Content Types"]
        F[Code Snippets\nReusable patterns]
        G[Best Practices\nCoding standards]
        H[Design Patterns\nArchitecture templates]
        I[API Specs\nOpenAPI / internal contracts]
        J[ADRs\nArchitecture decisions]
        K[Style Guides\nNaming, structure conventions]
    end

    subgraph IndexFlow["Repository Indexing Lifecycle"]
        L[New conversation started] --> M[Semantic index check]
        M -->|Index missing or stale| N[Background indexing\nup to 60s first time]
        M -->|Index current| O[Context-enriched response]
        N --> O
    end

    C --> KBTypes
    D --> IndexFlow
```

Notes:
- All Enterprise features sit on top of Business features — there is nothing in Business that Enterprise lacks.
- The GitHub.com Chat interface is the key differentiator most likely to appear in exam questions distinguishing Business from Enterprise.
- PR summaries are generated on demand — Copilot does not automatically post them; the author triggers generation from the PR description editor.
- Repository indexing happens automatically; no admin configuration is required. Content exclusion policies apply to indexed data before it is shared with Copilot.

## Quick Recap

- Copilot Enterprise = all Business features + GitHub.com Chat + PR summaries + Knowledge Bases (Spaces) + repository indexing + custom models.
- Copilot Chat on GitHub.com lets developers query repositories directly in the browser without an IDE, using the semantic index for context-enriched answers.
- PR summaries are triggered on-demand in the PR description editor; they summarise changes, affected files, and reviewer focus areas.
- Knowledge Bases (Spaces) curate content types: source code, best practices, design patterns, API specs, ADRs, and style guides; they ground Chat in org-specific knowledge.
- Repository indexing (semantic code search) is automatic; initial indexing takes up to 60 seconds; content exclusions apply to indexed data.
- Custom models allow fine-tuning on an organisation's own codebase, improving completion relevance for specialised or proprietary code.

## Sources Consulted

- https://docs.github.com/en/copilot/get-started/plans
- https://docs.github.com/en/copilot/get-started/features
- https://docs.github.com/en/copilot/using-github-copilot/creating-a-pull-request-summary-with-github-copilot
- https://docs.github.com/en/copilot/concepts/context/repository-indexing
- https://docs.github.com/en/copilot/using-github-copilot/asking-github-copilot-questions-in-github

## References

- Facts referenced; explanations are original.
- https://docs.github.com/en/copilot/concepts/context/repository-indexing
- https://docs.github.com/en/copilot/using-github-copilot/creating-a-pull-request-summary-with-github-copilot
- https://docs.github.com/en/copilot/using-github-copilot/asking-github-copilot-questions-in-github

[Home](../../README.md) | [Domain Index](./README.md) | [Previous](./copilot-business.md) | [Next](./copilot-chat.md)
