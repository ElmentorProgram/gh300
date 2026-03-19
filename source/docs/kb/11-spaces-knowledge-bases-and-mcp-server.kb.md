# Spaces, Knowledge Bases, and MCP Server

GitHub Copilot introduces multiple ways to extend context beyond a single file or chat session. These include:

- Copilot Spaces for task-focused, curated context  
- Knowledge Bases for large-scale organizational documentation  
- MCP Server for connecting Copilot to external tools and systems  

These features are critical for GH-300 because they define:

- How Copilot accesses and uses context  
- Differences between scoped vs large context  
- How Copilot integrates with tools and workflows  

Understanding these distinctions is key to both real-world usage and exam scenarios.

## This Document Will Cover

- Context Expansion in Copilot  
- Copilot Spaces (Concept and Usage)  
- Spaces vs Knowledge Bases  
- Creating and Structuring Spaces  
- Collaboration and Sharing in Spaces  
- Best Practices for Spaces  
- Knowledge Bases (Enterprise Context)  
- MCP Server (Concept and Architecture)  
- MCP in Developer Workflows  
- Agent Mode and MCP Integration  
- Limitations and Boundaries  
- Summary  

## Context Expansion in Copilot

By default, Copilot operates on limited context.

- **Local Context:**  
  Includes the current file, nearby code, and open files, which form the primary input for suggestions  

- **Session Context:**  
  Includes chat history and recent interactions, helping Copilot maintain conversational continuity  

- **Limitations:**  
  Copilot cannot see full repositories or external systems unless additional context is explicitly provided  

To overcome these limitations, Copilot introduces structured context mechanisms such as Spaces, Knowledge Bases, and MCP.

## Copilot Spaces (Concept and Usage)

Copilot Spaces provide a curated, task-specific context designed to improve accuracy and consistency.

- **Focused Context:**  
  Spaces allow developers to define exactly what Copilot should use as context, improving relevance  

- **Supported Inputs:**  
  Can include repositories, files, pull requests, issues, text notes, images, and uploaded documents  

- **Task-Oriented Design:**  
  Optimized for specific workflows such as onboarding, feature development, or system understanding  

- **Reusable Context:**  
  Spaces persist beyond a single chat session and can be reused across multiple interactions  

Spaces improve response quality by narrowing context to only what matters.

## Spaces vs Knowledge Bases

Spaces and Knowledge Bases serve different purposes.

- **Spaces:**  
  Designed for focused, task-specific context with limited size and higher response accuracy  

- **Knowledge Bases:**  
  Designed for large-scale documentation and organization-wide context  

- **Accuracy vs Breadth:**  
  Spaces prioritize accuracy through curated, smaller context  
  Knowledge Bases prioritize breadth by covering large documentation sets  

- **Creation Scope:**  
  Spaces can be created by individual users  
  Knowledge Bases are typically managed at the organization level  

Understanding this distinction is critical for exam scenarios.

## Creating and Structuring Spaces

Spaces are created and configured using context and instructions.

- **Instructions:**  
  Define what Copilot should focus on, what tasks it should perform, and what it should avoid  

- **Sources:**  
  Add repositories, files, issues, pull requests, and uploaded content to ground responses  

- **Selective Context:**  
  Including only relevant sources improves output quality and reduces noise  

- **Dynamic Updates:**  
  GitHub-based sources automatically reflect updates from the default branch  

The structure and quality of context directly affect Copilot performance.

## Collaboration and Sharing in Spaces

Spaces support collaboration across teams.

- **Ownership:**  
  Spaces can belong to individual users or organizations  

- **Sharing:**  
  Organization-owned spaces can be shared with teams or specific users  

- **Roles:**  
  Viewers can ask questions, editors can modify content, and admins can manage settings and permissions  

- **Use Cases:**  
  Common scenarios include onboarding, documentation sharing, and system knowledge management  

Spaces enable shared understanding and reduce repeated explanations.

## Best Practices for Spaces

To improve results when using Spaces:

- **Keep Context Focused:**  
  Avoid adding unnecessary or unrelated sources  

- **Use Clear Instructions:**  
  Clearly define goals, tasks, and expected outputs  

- **Provide Examples:**  
  Include sample outputs to guide Copilot responses  

- **Maintain Context:**  
  Keep sources updated and relevant to the task  

- **Avoid Overloading:**  
  Too much context reduces accuracy and response quality  

Well-designed spaces produce more consistent and reliable results.

## Knowledge Bases (Enterprise Context)

Knowledge Bases provide organization-wide context for Copilot.

- **Centralized Documentation:**  
  Store large collections of documentation for use across teams  

- **Enterprise Feature:**  
  Typically available in enterprise environments with advanced governance  

- **Markdown-Based:**  
  Content is usually structured as markdown files stored in repositories  

- **Broad Context:**  
  Supports large-scale knowledge sharing across projects  

- **Lower Precision:**  
  Large context may reduce response accuracy compared to focused Spaces  

Knowledge Bases are useful for scale, but less precise than Spaces.

## MCP Server (Concept and Architecture)

The Model Context Protocol (MCP) enables Copilot to connect to external tools and data.

- **Standardized Integration:**  
  Provides a consistent interface for connecting AI models to tools and services  

- **Client-Server Model:**  
  Copilot acts as a client interacting with MCP servers  

- **Local and Remote Options:**  
  MCP servers can run locally or remotely depending on the setup  

- **Tool Access:**  
  Enables actions such as creating issues, editing files, or retrieving external data  

MCP extends Copilot capabilities beyond repositories.

## MCP in Developer Workflows

MCP enables advanced workflows across tools and systems.

- **Repository Interaction:**  
  Allows actions such as creating issues, managing pull requests, and updating files  

- **Automation:**  
  Automates repetitive development tasks  

- **Cross-Platform Integration:**  
  Works across IDEs, web interfaces, and command-line environments  

- **Real-Time Context Access:**  
  Retrieves and uses external data during development tasks  

MCP transforms Copilot into a workflow automation tool.

## Agent Mode and MCP Integration

Agent mode becomes more powerful when combined with MCP.

- **Autonomous Workflows:**  
  Copilot can perform multi-step tasks without constant user input  

- **Tool Selection:**  
  Selects appropriate MCP tools based on the task and context  

- **Iterative Execution:**  
  Executes tasks, evaluates results, and refines outputs  

- **Extended Context:**  
  Accesses data beyond the local environment and repository  

This enables advanced AI-driven development workflows.

## Limitations and Boundaries

These features have limitations.

- **Context Size Limits:**  
  Large context reduces response accuracy  

- **Security Constraints:**  
  Access is limited by permissions and organizational policies  

- **Tool Availability:**  
  MCP capabilities depend on configured servers and available tools  

- **Repository Scope:**  
  Spaces and Knowledge Bases only use accessible data  

- **Complexity:**  
  Setup and management may require additional effort and configuration  

Understanding these limitations prevents misuse and incorrect expectations.

## Summary

You should now be able to:

- Understand how Copilot expands context  
- Use Copilot Spaces effectively  
- Distinguish Spaces from Knowledge Bases  
- Structure and manage Spaces  
- Use Knowledge Bases for enterprise context  
- Understand MCP architecture and purpose  
- Apply MCP in developer workflows  
- Understand agent mode integration with MCP  
- Recognize limitations and boundaries