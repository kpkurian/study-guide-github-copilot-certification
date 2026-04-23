# GitHub Copilot Certification Study Guide

> **Exam:** GitHub Copilot · Exam Code: `COPILOT` · Microsoft Learn ID: `GH-300`

A structured, original study guide for the GitHub Copilot certification exam. Content is organized by exam domain — each domain has its own folder with subtopic pages built from a consistent template.

---

## Exam at a Glance

| Detail | Value |
|--------|-------|
| Level | Intermediate |
| Duration | 100 minutes |
| Cost | USD 99 |
| Validity | 730 days |
| Audience | Developer, DevOps Engineer, App Maker, Technology Manager |
| Certification page | [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/github-copilot/) |
| Practice assessment | [Take practice test](https://learn.microsoft.com/en-us/credentials/certifications/github-copilot/practice/assessment?assessment-type=practice&assessmentId=218035372&practice-assessment-type=certification) |

---

## Domain Weights

```mermaid
pie title GitHub Copilot Exam — Domain Weights
    "Domain 2: Plans and Features" : 31
    "Domain 3: How Copilot Works" : 15
    "Domain 7: Privacy and Exclusions" : 15
    "Domain 5: Developer Use Cases" : 14
    "Domain 4: Prompt Engineering" : 9
    "Domain 6: Testing" : 9
    "Domain 1: Responsible AI" : 7
```

---

## Domains

| # | Domain | Weight | Folder |
|---|--------|--------|--------|
| 1 | Responsible AI | 7% | [domain-1-responsible-ai](./domains/domain-1-responsible-ai/) |
| 2 | GitHub Copilot Plans and Features | 31% | [domain-2-plans-and-features](./domains/domain-2-plans-and-features/) |
| 3 | How GitHub Copilot Works and Handles Data | 15% | [domain-3-how-copilot-works](./domains/domain-3-how-copilot-works/) |
| 4 | Prompt Crafting and Prompt Engineering | 9% | [domain-4-prompt-engineering](./domains/domain-4-prompt-engineering/) |
| 5 | Developer Use Cases for AI | 14% | [domain-5-developer-use-cases](./domains/domain-5-developer-use-cases/) |
| 6 | Testing with GitHub Copilot | 9% | [domain-6-testing](./domains/domain-6-testing/) |
| 7 | Privacy Fundamentals and Context Exclusions | 15% | [domain-7-privacy-and-exclusions](./domains/domain-7-privacy-and-exclusions/) |

---

## Recommended Study Sequence

Study high-weight domains first to maximize exam readiness early.

```mermaid
flowchart LR
    subgraph Phase1["Phase 1 — High Weight (61%)"]
        D2["Domain 2\nPlans & Features\n31%"]
        D3["Domain 3\nHow Copilot Works\n15%"]
        D7["Domain 7\nPrivacy & Exclusions\n15%"]
    end
    subgraph Phase2["Phase 2 — Practical Skills (23%)"]
        D5["Domain 5\nDeveloper Use Cases\n14%"]
        D4["Domain 4\nPrompt Engineering\n9%"]
    end
    subgraph Phase3["Phase 3 — Reinforce (16%)"]
        D6["Domain 6\nTesting\n9%"]
        D1["Domain 1\nResponsible AI\n7%"]
    end
    subgraph Validate["Validate"]
        PA["Practice\nAssessment"]
        TR["Targeted\nReview"]
    end

    Phase1 --> Phase2 --> Phase3 --> Validate
```

