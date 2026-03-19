# Copilot in the IDE: Suggestions, Chat, Inline Chat, and Edits

GitHub Copilot is most powerful when used directly inside the IDE. This is where developers spend most of their time, and where Copilot integrates deeply into the coding workflow.

Inside the IDE, Copilot provides multiple interaction models. These are not just different features, but different ways of working with AI, each suited for specific types of tasks.

Understanding how these modes differ is critical for both real usage and exam scenarios.

## This Document Will Cover

- Copilot in the IDE Overview  
- Inline Suggestions (Ghost Text)  
- Multiple Suggestions and Navigation  
- Next Edit Suggestions  
- Copilot Chat in the IDE  
- Inline Chat (Scoped Editing)  
- Chat Modes (Ask, Edit, Agent, Plan)  
- Chat Participants and Context Scoping  
- Slash Commands and Their Purpose  
- Copilot Edits (Cross-File Changes)  
- Agent Mode in the IDE  
- Subagents and Task Delegation  
- Practical Usage Patterns  
- Core Limitations in the IDE  
- Summary  

## Copilot in the IDE Overview

In the IDE, Copilot operates as a real-time assistant embedded in the coding environment.

It continuously analyzes:

- The file being edited  
- Nearby code  
- Open files  
- Comments and structure  

This allows Copilot to provide:

- Immediate code completions  
- Context-aware suggestions  
- Conversational assistance  
- Multi-step task execution  

The IDE is where Copilot shifts from a simple autocomplete tool into a workflow assistant.

## Inline Suggestions (Ghost Text)

Inline suggestions are the most frequently used Copilot feature.

They appear as ghost text while typing and represent predicted code completions.

- **Context-Based Generation:**  
  Suggestions are generated using the surrounding code, comments, naming patterns, and structure already present in the file  

- **Adaptive Behavior:**  
  Copilot adapts to naming conventions, formatting style, and repeated patterns in the project  

- **Granular Acceptance:**  
  Developers can accept full suggestions, accept partial suggestions, or ignore them entirely  

- **Low Friction Workflow:**  
  Inline suggestions require no explicit prompt, allowing developers to stay in flow without interrupting their work  

Inline suggestions are best for fast, repetitive, and local coding tasks rather than complex reasoning.

## Multiple Suggestions and Navigation

Copilot often generates more than one possible solution.

- **Alternative Suggestions:**  
  Developers can cycle through multiple suggestions to explore different implementations for the same task  

- **Decision Flexibility:**  
  This allows selecting the most appropriate approach without rewriting prompts or manually restructuring code  

- **Exploration Without Context Switching:**  
  Multiple options are available directly inside the editor, keeping developers in the coding flow  

This is particularly useful when there are multiple valid implementations or when comparing different patterns.

## Next Edit Suggestions

Next edit suggestions extend beyond simple completion.

- **Predictive Editing:**  
  Copilot predicts where the next change should occur, not just what to type  

- **Multi-Line Awareness:**  
  Suggestions may span multiple lines or affect broader sections of the file  

- **Workflow Acceleration:**  
  Helps developers move quickly across logical changes instead of manually navigating and editing  

This feature reflects Copilot’s ability to assist with editing intent, not just typing.

## Copilot Chat in the IDE

Copilot Chat introduces a conversational interface directly inside the IDE.

- **Natural Language Interaction:**  
  Developers describe goals or problems instead of writing code step by step  

- **Contextual Understanding:**  
  Chat uses open files, selected code, and workspace context to generate relevant responses  

- **Multi-Step Tasks:**  
  Supports complex operations such as debugging, planning, and structured refactoring  

Common use cases include explaining code, generating implementations, debugging issues, and writing tests.

Copilot Chat is designed for reasoning and problem-solving tasks rather than simple code completion.

## Inline Chat (Scoped Editing)

Inline Chat allows interaction directly within the code editor.

- **Local Context Focus:**  
  Operates only on the selected code or the current file  

- **Minimal Context Switching:**  
  Developers remain inside the editor while interacting with Copilot  

- **Precise Changes:**  
  Ideal for small fixes, targeted refactoring, and localized improvements  

Inline Chat is best suited for controlled, scoped changes.

## Chat Modes

Copilot Chat provides multiple modes, each designed for a specific workflow.

- **Ask Mode:**  
  Used for explanations, questions, and general assistance without modifying files  

- **Edit Mode:**  
  Used to make controlled changes across selected files, allowing review before applying updates  

- **Agent Mode:**  
  Enables autonomous multi-step task execution, including proposing commands and iterating until completion  

- **Plan Mode:**  
  Generates structured plans before making changes, useful for complex or multi-step implementations  

Each mode represents a different balance between control and automation.

## Chat Participants and Context Scoping

Participants help scope requests to specific domains or contexts.

- **@workspace:**  
  Uses the full project context to answer questions or generate code  

- **@terminal:**  
  Focuses on command-line operations and terminal-related workflows  

- **@vscode:**  
  Handles IDE-specific configuration and usage questions  

- **@github:**  
  Uses repository context such as issues, pull requests, and workflows  

Participants improve accuracy by narrowing the scope of the request.

## Slash Commands

Slash commands simplify common development tasks.

- **/fix:**  
  Suggests fixes for errors or problematic code  

- **/tests:**  
  Generates unit tests based on selected code  

- **/doc:**  
  Adds documentation or comments  

- **/explain:**  
  Explains the behavior and logic of code  

- **/new:**  
  Creates new files or scaffolds project structures  

Slash commands reduce prompt complexity and guide Copilot toward specific outcomes.

## Copilot Edits (Cross-File Changes)

Copilot Edits enable changes across multiple files.

- **Multi-File Awareness:**  
  Copilot can modify several files in a single operation  

- **Controlled Execution:**  
  Developers review and approve suggested changes before applying them  

- **Workflow Integration:**  
  Useful for refactoring, feature updates, and structural changes across a codebase  

This capability bridges the gap between simple suggestions and larger transformations.

## Agent Mode in the IDE

Agent Mode enables autonomous workflows inside the IDE.

- **Task Execution:**  
  Copilot can plan, execute, and iterate on development tasks  

- **Tool Integration:**  
  May suggest terminal commands or interact with available tools  

- **Iterative Improvement:**  
  Continues refining output until the task is complete  

Agent Mode represents a shift from assistant behavior to collaborative workflow automation.

## Subagents and Task Delegation

Subagents allow delegation of complex tasks.

- **Independent Context:**  
  Subagents operate with their own context window separate from the main chat  

- **Specialized Tasks:**  
  Useful for focused tasks such as testing, refactoring, or analysis  

- **Result Aggregation:**  
  Outputs are returned to the main session after completion  

This supports more advanced, multi-step workflows.

## Practical Usage Patterns

Different Copilot features are suited for different tasks.

- **Inline Suggestions:**  
  Best for fast, repetitive coding and small code completions  

- **Inline Chat:**  
  Best for small, localized fixes and targeted improvements  

- **Chat (Ask Mode):**  
  Best for understanding code and getting explanations  

- **Edit Mode:**  
  Best for controlled multi-file changes  

- **Agent Mode:**  
  Best for complex, multi-step workflows and automation  

Choosing the correct interaction model improves both speed and output quality.

## Core Limitations in the IDE

Copilot in the IDE has limitations.

- **Context Limitations:**  
  Only visible files and available context are used, which may result in incomplete understanding  

- **Non-Deterministic Output:**  
  The same input may produce different outputs across attempts  

- **Over-Reliance Risk:**  
  Developers may accept suggestions without sufficient validation  

- **Incomplete Understanding:**  
  Copilot does not fully understand architecture or business intent  

These limitations reinforce the need for validation, testing, and human oversight.

## Summary

You should now be able to:

- Understand how Copilot operates inside the IDE  
- Distinguish between Inline Suggestions, Chat, and Inline Chat  
- Identify different Chat Modes and their use cases  
- Use participants and slash commands effectively  
- Understand Agent Mode and Edits workflows  
- Choose the correct interaction model for each task  
- Recognize limitations and apply validation