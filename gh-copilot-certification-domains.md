# GitHub Copilot Certification Domains

Last updated from source: 2026-04-22
Source endpoint: https://learn.github.com/api/certifications/COPILOT
Certification: GitHub Copilot (Exam code: COPILOT, Microsoft Learn ID: GH-300)

## Exam at a Glance

- Level: Intermediate
- Duration: 100 minutes
- Cost: USD 99
- Validity: 730 days
- Audience: App Maker, Developer, DevOps Engineer, Technology Manager

## Domain Weights

- Domain 1: Responsible AI (7%)
- Domain 2: GitHub Copilot plans and features (31%)
- Domain 3: How GitHub Copilot works and handles data (15%)
- Domain 4: Prompt Crafting and Prompt Engineering (9%)
- Domain 5: Developer use cases for AI (14%)
- Domain 6: Testing with GitHub Copilot (9%)
- Domain 7: Privacy fundamentals and context exclusions (15%)

## Domain 1: Responsible AI (7%)

### Explain responsible usage of AI

- Describe the risks associated with using AI.
- Explain limitations of generative AI tools (source-data depth, bias in data, and similar constraints).
- Explain the need to validate AI tool output.
- Identify how to operate AI responsibly.
- Identify potential harms of generative AI (bias, secure code concerns, fairness, privacy, transparency).
- Explain how to mitigate potential harms.
- Explain ethical AI.

## Domain 2: GitHub Copilot Plans and Features (31%)

### Identify the different GitHub Copilot plans

- Understand differences between Copilot Individual, Copilot Business, Copilot Enterprise, and Copilot Business for non-GHE.
- Understand Copilot for non-GitHub customers.
- Define GitHub Copilot in the IDE.
- Define GitHub Copilot Chat in the IDE.
- Describe ways to trigger Copilot (chat, inline chat, suggestions, multiple suggestions, exception handling, CLI).

### Identify the main features with GitHub Copilot Individual

- Explain differences between Copilot Individual and Copilot Business (data exclusions, IP indemnity, billing, and more).
- Understand available IDE features in Copilot Individual.

### Identify the main features of GitHub Copilot Business

- Demonstrate excluding specific files from GitHub Copilot.
- Demonstrate organization-wide policy management.
- Describe the purpose of organization audit logs for Copilot Business.
- Explain searching audit log events for Copilot Business.
- Explain managing Copilot Business subscriptions via REST API.

### Identify the main features with GitHub Copilot Chat

- Identify use cases where Copilot Chat is most effective.
- Explain how to improve Copilot Chat performance.
- Identify Copilot Chat limitations.
- Identify options for using code suggestions from Copilot Chat.
- Explain how to share feedback about Copilot Chat.
- Identify common best practices for Copilot Chat.
- Identify available slash commands in Copilot Chat.

### Identify the main features with GitHub Copilot Enterprise

- Explain benefits of Copilot Chat on GitHub.com.
- Explain Copilot pull request summaries.
- Explain configuration and use of Knowledge Bases in Copilot Enterprise.
- Describe knowledge types in a Knowledge Base (code snippets, best practices, design patterns, and more).
- Explain benefits of Knowledge Bases for code completion and review (quality, consistency, efficiency).
- Describe creating, managing, and searching Knowledge Bases, including indexing and related configuration.
- Explain benefits of custom models.

### Using GitHub Copilot in the CLI

- Discuss steps to install GitHub Copilot in the CLI.
- Identify common commands when using Copilot in the CLI.
- Identify configurable settings for Copilot in the CLI.

## Domain 3: How GitHub Copilot Works and Handles Data (15%)

### Describe the data pipeline lifecycle of GitHub Copilot code suggestions in the IDE

- Visualize the lifecycle of a Copilot code suggestion.
- Explain how Copilot gathers context.
- Explain how Copilot builds a prompt.
- Describe the proxy service and prompt filters.
- Describe how the large language model produces a response.
- Explain post-processing of Copilot responses through the proxy server.
- Identify how Copilot identifies matching code.

### Describe how GitHub Copilot handles data

- Describe how data in Copilot Individual is used and shared.
- Explain the data flow for Copilot code completion.
- Explain the data flow for Copilot Chat.
- Describe input processing types for Copilot Chat (prompt types it is designed for).

### Describe the limitations of GitHub Copilot (and LLMs in general)

- Describe the effect of frequently seen examples in source data.
- Describe code suggestion age and relevance.
- Describe the nature of Copilot reasoning and contextual response versus exact calculations.
- Describe limited context windows.

## Domain 4: Prompt Crafting and Prompt Engineering (9%)

### Describe the fundamentals of prompt crafting

- Describe how prompt context is determined.
- Describe language options for prompting Copilot.
- Describe different parts of a prompt.
- Describe the role of prompting.
- Describe zero-shot versus few-shot prompting.
- Describe how chat history is used with Copilot.
- Identify prompt crafting best practices for Copilot.

### Describe the fundamentals of prompt engineering

- Explain prompt engineering principles, training methods, and best practices.
- Describe the prompt process flow.

## Domain 5: Developer Use Cases for AI (14%)

### Improve developer productivity

- Describe how AI improves common developer productivity use cases.
- Learning new programming languages and frameworks.
- Language translation.
- Context switching.
- Writing documentation.
- Personalized, context-aware responses.
- Generating sample data.
- Modernizing legacy applications.
- Debugging code.
- Data science workflows.
- Code refactoring.
- Discuss how Copilot helps with SDLC management.
- Describe limitations of using Copilot.
- Describe using the productivity API to measure Copilot impact.

## Domain 6: Testing with GitHub Copilot (9%)

### Describe options for generating tests for your code

- Describe how Copilot can help add unit tests, integration tests, and other test types.
- Explain how Copilot can assist with identifying edge cases and suggesting tests.

### Describe the different SKUs for GitHub Copilot

- Describe different SKUs and associated privacy considerations.
- Describe organization-level code suggestion configuration options.
- Describe the GitHub Copilot Editor config file.

## Domain 7: Privacy Fundamentals and Context Exclusions (15%)

### Enhance code quality through testing

- Describe how to improve effectiveness of existing tests with Copilot suggestions.
- Describe generating boilerplate code for test types with Copilot.
- Explain how Copilot can help write assertions for testing scenarios.

### Leverage GitHub Copilot for security and performance

- Describe how Copilot can learn from existing tests to suggest improvements and identify potential issues.
- Explain how Copilot Enterprise can support collaborative code reviews with security and performance considerations.
- Explain how Copilot can identify potential security vulnerabilities.
- Describe how Copilot can suggest performance optimizations.

### Identify content exclusions

- Describe configuring content exclusions at repository and organization levels.
- Explain effects of content exclusions.
- Explain limitations of content exclusions.
- Describe ownership of Copilot outputs.

### Safeguards

- Describe the duplication detector filter.
- Explain contractual protection.
- Explain configuring Copilot settings on GitHub.com.
- Enabling or disabling duplication detection.
- Enabling or disabling prompt and suggestion collection.
- Describe security checks and warnings.

### Troubleshooting

- Explain resolving missing code suggestions for specific files.
- Explain why context exclusions may not be applied.
- Explain how to trigger Copilot when suggestions are absent or not ideal.
- Explain context exclusion steps in code editors.

## Notes

- The source outline currently contains repeated entries for two Domain 2 sections (Individual and Business). This guide consolidates those duplicate sections to avoid redundancy.
- The exam metadata in the endpoint marks the exam object as not currently available to take. Verify current booking status in Microsoft Credentials before scheduling.
