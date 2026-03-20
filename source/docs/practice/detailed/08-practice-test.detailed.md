# Detailed Practice Test 08 - Answer Sheet & Explanation

**Question:** [211]  
What is a key difference between **Copilot Agent Mode** and standard Copilot Chat?

**Options:**  
A. Standard Chat can only answer questions, while Agent Mode is limited to viewing logs and cannot edit code or run commands  
B. **Agent Mode can autonomously perform multi-step tasks (edit files, run commands, open PRs) based on a high-level goal**  
C. Agent Mode is restricted to Q&A and cannot change files or execute any tools  
D. Agent Mode and standard Chat are identical in capability and differ only in UI  

**Correct Answer(s):** B  

**Explanation:**  
Standard Copilot Chat focuses on **conversational help** explaining code, answering questions, and suggesting snippets while **Agent Mode / the coding agent** can take a **high-level task** and autonomously plan and execute **multi-step workflows**. These workflows can include editing multiple files, running tools or commands, and preparing a **pull request** for you to review, all within your existing repository permissions and policies.

**Tips and Tricks:**  
Use standard Chat when you need explanations, quick examples, or small edits scoped to what is visible in the editor.  
Use Agent Mode when the task involves multiple coordinated steps across files and tools, such as updating APIs, tests, and build scripts together.  
Always review the agent’s changes and pull requests branch protections, required reviews, and CI checks still apply.

> [!IMPORTANT]  
> When you see “**multi-step, edit files, run commands, open a PR**” in a scenario, it is pointing to **Agent Mode / coding agent**, not basic Copilot Chat.

**Correct and Wrong:**  
The correct option is the only one that highlights **autonomous, multi-step execution** editing files, running commands, and opening PRs based on a high-level goal, which is exactly what Agent Mode adds. The other options either claim Agent Mode is only Q&A, give it incorrect limitations, or say there is no functional difference from Chat, all of which conflict with the documented behavior.

**Source:**  
[GitHub Copilot features – Agent mode](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[Build applications with GitHub Copilot agent mode](https://learn.microsoft.com/en-us/training/modules/github-copilot-agent-mode/) (Microsoft Learn)  
[Agent mode 101: All about GitHub Copilot’s powerful mode](https://github.blog/ai-and-ml/github-copilot/agent-mode-101-all-about-github-copilots-powerful-mode/) (GitHub Blog)  


**Question:** [212]  
Which is the **best prompt** to give Copilot Agent Mode when building a new feature?

**Options:**  
A. “Fix everything in this repository and change whatever you think is necessary across all services.”  
B. **“Implement a new /reports endpoint in this service that returns JSON summaries; update routing, handlers, and add tests. Keep existing APIs unchanged.”**  
C. “Write some code for me.”  
D. “Refactor something somewhere in the codebase to make it better.”  

**Correct Answer(s):** B  

**Explanation:**  
Agent Mode works best with a **high-signal, well-scoped prompt** that describes the feature, its scope, and any constraints. Asking for a `/reports` endpoint, specifying JSON summaries, naming the areas to update (routing, handlers, tests), and requiring that existing APIs remain unchanged gives the agent enough structure to plan a coherent set of edits. Vague prompts like “fix everything” or “write some code” are far more likely to produce noisy, hard-to-review changes.

**Tips and Tricks:**  
Include **goal, scope, and constraints** in your Agent Mode prompt: what to build, where to build it, and what must stay stable.  
Mention **tests explicitly** for example, “add or update tests” to make them part of the agent’s plan, not an afterthought.  
Avoid unbounded repo-wide prompts; smaller, well-defined tasks produce cleaner diffs and safer PRs.

> [!IMPORTANT]  
> Treat Agent Mode prompts like **ticket descriptions**: clear feature, clear scope, explicit constraints, and acceptance criteria including tests and PR output.

**Correct and Wrong:**  
The correct prompt clearly describes the feature, the affected areas, and the constraints, making it ideal for Agent Mode’s multi-step planning. The other prompts are vague (“write code,” “refactor something”) or dangerously broad (“fix everything”), which do not align with recommended practice or exam expectations for safe agent use.

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[GitHub Copilot features – Agent mode](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Build applications with GitHub Copilot agent mode](https://learn.microsoft.com/en-us/training/modules/github-copilot-agent-mode/) (Microsoft Learn)  


**Question:** [213]  
In a **TDD-style workflow** using Copilot Agent Mode, what is an appropriate sequence?

**Options:**  
A. Write implementation code first, let Agent Mode delete or skip any failing tests, then deploy if the build is green  
B. **Use Chat or Agent Mode to scaffold failing tests, then have Agent Mode implement the code to satisfy them, and finally review and refactor with tests passing**  
C. Ask Agent Mode to generate both code and tests in one pass and skip manual review as long as tests compile  
D. Turn tests off while Agent Mode works, then enable them again only in production  

**Correct Answer(s):** B  

**Explanation:**  
In a TDD-style workflow, you still follow **red–green–refactor**: write tests first (red), implement code to make them pass (green), then refactor with tests as your safety net. Copilot Chat or Agent Mode can help **scaffold tests** and **implement code**, but you remain in control of the sequence, run the tests yourself, and review the resulting changes before merging.

**Tips and Tricks:**  
Start by asking Copilot to generate or refine **tests that initially fail**, validating your understanding of the desired behavior.  
Have Agent Mode implement or adjust code until the tests pass, then refactor while keeping the suite green.  
Keep tasks small and focused so it is obvious which tests correspond to which changes, making reviews and debugging easier.

> [!IMPORTANT]  
> Copilot can **accelerate** TDD but never replaces it: tests still come first, and you still own review, refactoring, and final approval.

**Correct and Wrong:**  
The correct option is the only one that respects the **TDD loop** tests first, then implementation, then refactor while using Agent Mode as an accelerator. The distractors either demote tests (deleting or disabling them), encourage skipping review, or suggest turning tests off entirely, which conflicts with both TDD practice and responsible Copilot usage.

**Source:**  
[Develop unit tests using GitHub Copilot tools](https://learn.microsoft.com/en-us/training/modules/develop-unit-tests-github-copilot-tools/) (Microsoft Learn)  
[GitHub Copilot features – Agent mode](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  


**Question:** [214]  
Which scenario **best fits** using Copilot Agent Mode instead of a simple edit or inline suggestion?

**Options:**  
A. Renaming a single local variable inside one function in a single file  
B. Correcting a spelling mistake in a comment that appears in one file  
C. **Updating a feature that spans multiple files (API contract, data model, and tests), and adjusting a CI script to run new tests as part of the same change**  
D. Writing a short, one-line SQL query for a quick check in a scratch file  

**Correct Answer(s):** C  

**Explanation:**  
Agent Mode is designed for **cross-cutting, multi-step tasks** that touch several parts of your system such as updating an API contract, corresponding data models, related tests, and the CI configuration needed to run those tests together. For small localized edits like a variable rename, typo fix, or one-line query, inline suggestions or simple edits are faster, safer, and more appropriate.

**Tips and Tricks:**  
Use Agent Mode when changes span **multiple files or layers** (API endpoints, domain models, tests, CI or tooling) and must remain consistent.  
Prefer inline suggestions or Edit mode for **tiny, local changes** where a full autonomous workflow would be unnecessary overhead.  
Keep Agent Mode tasks scoped so the resulting pull requests are understandable and reviewable in a single sitting.

> [!IMPORTANT]  
> A good mental shortcut: if the task sounds like a **mini-project** across code, tests, and CI, think **Agent Mode**; if it is a small local tweak, stick with inline or simple edits.

**Correct and Wrong:**  
The correct option is the only one that describes a **multi-file, multi-step feature update** exactly the kind of work Agent Mode is intended to orchestrate. The other options involve trivial, single-file edits or a quick query where Agent Mode would be excessive and where standard inline suggestions or a quick Chat answer are sufficient.

**Source:**  
[GitHub Copilot features – Agent mode](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  


**Question:** [215]  
When Copilot Agent Mode opens a **pull request** after completing a task, what is the **developer’s responsibility**?

**Options:**  
A. None, the pull request from Copilot can be merged automatically without human review or checks  
B. Only verify that the branch has no merge conflicts before approving the pull request  
C. **Review the PR like any other: inspect diffs, run tests, ensure it meets security/compliance and coding standards**  
D. Accept all changes solely because they were generated by Copilot, without additional validation  

**Correct Answer(s):** C  

**Explanation:**  
When Copilot Agent Mode or the coding agent opens a pull request, it is treated just like a PR from any other contributor. You must **review the diffs**, run or verify **tests and status checks**, and confirm that the changes meet your **security, compliance, and coding standards** before merging. The agent does not bypass branch protections or required reviews.

**Tips and Tricks:**  
- Treat agent-created PRs like contributions from a junior teammate: read the diff, question assumptions, and run tests.  
- Keep your **branch protection rules, status checks, and required reviewers** enabled when adopting Agent Mode.  

> [!IMPORTANT]  
> Copilot can **open PRs**, but it cannot **approve its own work** code review, CI, and security checks still gate what gets merged.

**Correct and Wrong:**  
The correct option is the only one that preserves full SDLC responsibility by requiring you to review diffs, run tests, and verify security and compliance before merging. The other options wrongly imply automatic merging or skipping validation.

**Source:**  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  