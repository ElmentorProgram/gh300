# Detailed Practice Test 04 - Answer Sheet & Explanation

**Question:** [091]  
Where can you find **Copilot/extension logs** and deeper **Electron logs** in **VS Code**?

**Options:**  
A. Only in GitHub.com → Your profile → Logs  
B. **Output panel / Extensions logs folder for Copilot; Developer Tools for Electron logs**  
C. Git → Show Git Output (only)  
D. Copilot Chat → /logs command  

**Correct Answer(s):** B  

**Explanation:**  
VS Code writes Copilot/extension diagnostics to the **Output** view and the **Extensions logs folder**. You can open logs via **View → Output → “GitHub Copilot”**, and open the extension log files using the Command Palette command **“Developer: Open Extension Logs Folder”**. Platform-level details live under **Developer: Toggle Developer Tools → Console** (Electron DevTools). Use these alongside **“GitHub Copilot: Collect Diagnostics”** for complete troubleshooting artifacts.

**Tips and Tricks:**  
- Snapshot **Output → GitHub Copilot**, then open the **extension logs folder** and **Developer Tools → Console** for deeper network/runtime traces, especially for **proxy**, **firewall**, or **certificate** issues.  
- When preparing a support ticket, capture **Output logs**, **extension log files**, and relevant **Console** entries together.

> [!IMPORTANT]  
> For support, use **“GitHub Copilot: Collect Diagnostics”** together with **Output logs**, **extension log files**, and **Electron DevTools Console**. This combination gives a complete view of connectivity, configuration, and runtime errors, which significantly accelerates triage.

**Source:**  
[Viewing logs for GitHub Copilot in your environment](https://docs.github.com/en/copilot/how-tos/troubleshoot-copilot/view-logs?tool=vscode) (GitHub Docs)  
[Troubleshoot GitHub Copilot](https://docs.github.com/en/copilot/how-tos/troubleshoot-copilot?tool=vscode) (GitHub Docs)  
[Introduction to GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) (Microsoft Learn)  
[Get started with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [092]  
How do you run **“GitHub Copilot: Collect Diagnostics”** from the **Command Palette** in VS Code?

**Options:**  
A. Ctrl/Cmd+` → type “diagnostics copilot”  
B. View → Explorer → Diagnostics  
C. **Ctrl/Cmd+Shift+P → type “Collect Diagnostics” → select “GitHub Copilot: Collect Diagnostics”**  
D. F1 → “Open Logs” (only)

**Correct Answer(s):** C

**Explanation:**  
Use the **Command Palette** (Windows/Linux **Ctrl+Shift+P**, macOS **Cmd+Shift+P**) and run **“GitHub Copilot: Collect Diagnostics.”** From the Command Palette, type **“Diagnostics”** or **“Collect Diagnostics”**, then select **“GitHub Copilot: Collect Diagnostics”**. The command packages Copilot logs, environment details, versions, and connectivity information into an editor tab that you can inspect or share with support to help identify **connectivity/extension issues**.

**Tips and Tricks:**  
- Run diagnostics **before** changing settings; attach the generated bundle to tickets for faster resolution, especially for **network/proxy/certificate** issues.  
- Pair the diagnostics report with **Output → GitHub Copilot** and the **extension logs folder** so support receives both high-level environment info and detailed log data in one go.

> [!IMPORTANT]  
> The diagnostics report includes a **Reachability** section showing whether Copilot can access required services. Attach this report together with **Output logs** and **extension log files** to accelerate firewall/proxy troubleshooting and reduce back-and-forth with support.

**Source:**  
[Viewing logs for GitHub Copilot in your environment](https://docs.github.com/en/copilot/how-tos/troubleshoot-copilot/view-logs?tool=vscode) (GitHub Docs)  
[Troubleshoot GitHub Copilot](https://docs.github.com/en/copilot/how-tos/troubleshoot-copilot?tool=vscode) (GitHub Docs)  
[Troubleshooting network errors for GitHub Copilot](https://docs.github.com/en/copilot/how-tos/troubleshoot-copilot/troubleshoot-network-errors) (GitHub Docs)  
[Introduction to GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) (Microsoft Learn)

**Question:** [093]  
On which **surfaces** is **Copilot Chat** available?

**Options:**  
A. Only VS Code and Visual Studio  
B. **GitHub.com, VS Code, Visual Studio, JetBrains IDEs, Eclipse, Xcode, GitHub Mobile, Windows Terminal**  
C. Only GitHub.com  
D. Only IDEs (no browser or mobile)

**Correct Answer(s):** B

**Explanation:**  
GitHub lists **multiple surfaces** for Copilot Chat, including **GitHub.com**, major **IDEs** (**Visual Studio Code**, **Visual Studio**, **JetBrains IDEs**, **Eclipse**, **Xcode**), **GitHub Mobile**, and **Windows Terminal**. Core chat behavior is similar across these environments, but effective availability still depends on your **plan** and **organization/enterprise policy**.

**Tips and Tricks:**  
- If a stem mentions **browser (GitHub.com)**, **GitHub Mobile**, or **Windows Terminal**, map it to **Copilot Chat surfaces**, not just IDE integrations.  
- Look for clues like **repository-aware chat**, **enterprise agents**, or **Spaces** when the question is really about **Enterprise-only chat capabilities**, not just surface support.

> [!IMPORTANT]  
> **Surface ≠ feature set.** Copilot Chat is broadly available on **GitHub.com**, supported **IDEs**, **GitHub Mobile**, and **Windows Terminal** for eligible plans, while advanced features such as **repository-aware chat on GitHub.com** and **enterprise agents** are tied to **Copilot Enterprise** and governed by **organization/enterprise policies**.

**Source:**  
[GitHub Copilot features](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[About GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)  
[Chat with GitHub Copilot in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[Chat with GitHub Copilot in Windows Terminal](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-windows-terminal) (GitHub Docs)

**Question:** [094]  
What’s the difference between **Copilot Edits – Edit mode** and **Agent mode**?

**Options:**  
A. Edit = disables approvals; Agent = requires approvals  
B. **Edit = user-driven targeted edits; Agent = autonomous multi-step changes (can open a PR)**  
C. Edit = chat only; Agent = inline only  
D. Edit = repository-aware; Agent = IDE-only  

**Correct Answer(s):** B  

**Explanation:**  
**Edit mode** keeps you in control: you pick files, preview diffs, and accept changes incrementally. It is a **user-driven, targeted edit experience** where you select the scope, review suggested diffs, and apply or reject changes. **Agent mode** lets the **Copilot coding agent** decide which files and commands to run and **perform autonomous multi-step work** across files and tools, often **creating or updating pull requests** that you then review and merge.

**Tips and Tricks:**  
- Use **Edit** for precise, well-scoped refactors or localized changes where you want fine-grained control over diffs.  
- Use **Agent** for broader tasks such as **migrations**, **multi-file refactors**, or **test generation**, where the agent can iterate, run commands, and update PRs under your review.

> [!IMPORTANT]  
> Governance remains: even in **Agent mode**, changes land via **PR review**. Copilot does **not** bypass **branch protections**, **required approvals**, or **CI policies**; you still own final review and merge decisions.

**Source:**  
[GitHub Copilot Edits in Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-edits?view=visualstudio) (Microsoft Learn)  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[Agent mode 101: All about GitHub Copilot’s powerful mode](https://github.blog/ai-and-ml/github-copilot/agent-mode-101-all-about-github-copilots-powerful-mode/) (GitHub Blog)  
[Copilot ask, edit, and agent modes: What they do and when to use them](https://github.blog/ai-and-ml/github-copilot/copilot-ask-edit-and-agent-modes-what-they-do-and-when-to-use-them/) (GitHub Blog)

**Question:** [095]  
What do **Copilot code reviews** and **PR summaries** provide on GitHub.com?

**Options:**  
A. Auto-merge PRs  
B. **AI review suggestions and natural-language summaries of changes**  
C. License scanning  
D. Static code analysis only  

**Correct Answer(s):** B  

**Explanation:**  
On GitHub.com, Copilot can generate **review suggestions** and **summaries** to accelerate PR understanding. **Copilot code review** can analyze pull requests and offer **inline review comments and suggested changes**, while **Copilot PR summaries** generate **natural-language overviews of the changes** so reviewers can quickly understand scope and intent. These aids do **not** replace mandatory reviews or testing; they help reviewers focus on high-risk areas by condensing diffs and spotting potential issues.

**Tips and Tricks:**  
- Treat AI suggestions as **review input**, not authoritative truth; maintain normal **approval gates**, tests, and security checks.  
- Use **PR summaries** to speed up triage and review prioritization, especially in large or noisy repositories with many incoming pull requests.

> [!IMPORTANT]  
> Copilot enhances but doesn’t **automate approval/merge**. **Branch protection rules**, **required reviewers**, **CI checks**, and **security scans** remain the authoritative gates that must pass before a PR is merged.

**Source:**  
[About GitHub Copilot code review](https://docs.github.com/en/copilot/concepts/agents/code-review) (GitHub Docs)  
[Using GitHub Copilot code review](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/request-a-code-review/use-code-review) (GitHub Docs)  
[Creating a summary for a pull request with GitHub Copilot](https://docs.github.com/en/copilot/how-tos/use-copilot-for-common-tasks/create-a-pr-summary) (GitHub Docs)  
[Leveling up code reviews and pull requests with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/code-reviews-pull-requests-github-copilot/) (Microsoft Learn)

**Question:** [096]  
For **individuals**, which statements about **access and eligibility** are correct?

**Options:**  
A. **Copilot Free** is for personal use; **Pro** is paid but may be **free for verified students/teachers/maintainers**  
B. Pro is only for organizations  
C. Business is required for single developers  
D. Enterprise includes Pro seats for free  

**Correct Answer(s):** A  

**Explanation:**  
**Copilot Free** targets individuals getting started with a **personal-use, limited-quota** plan. **Copilot Pro** (and **Pro+**) are paid individual subscriptions and **Copilot Pro** can be **free** for **verified students, teachers, and maintainers of popular open-source projects**. You do **not** need **Business** or **Enterprise** plans for a single developer using a personal GitHub account.

**Tips and Tricks:**  
- Education/maintainer benefits unlock **Pro**, not **Free**, and not **Business/Enterprise**.  
- Remember that eligibility for **free Pro** is **re-evaluated regularly**, so access can change if your student/teacher/maintainer status changes.

> [!IMPORTANT]  
> **Copilot Free** has **limited completions and premium requests** and is not designed for organization-managed users. **Copilot Pro / Pro+** unlock higher limits and premium models, while **education/maintainer benefits specifically grant Pro**, not Business or Enterprise seats.

**Source:**  
[About individual GitHub Copilot plans and benefits](https://docs.github.com/en/copilot/concepts/billing/individual-plans) (GitHub Docs)  
[GitHub Copilot billing](https://docs.github.com/en/billing/concepts/product-billing/github-copilot) (GitHub Docs)  
[Getting free access to GitHub Copilot Pro](https://docs.github.com/en/copilot/how-tos/manage-your-account/get-free-access-to-copilot-pro) (GitHub Docs)  
[Introduction to GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) (Microsoft Learn)

**Question:** [097]  
Who purchases and assigns seats for **Business vs. Enterprise** plans?

**Options:**  
A. Developers purchase directly in the IDE  
B. **Org owners purchase/assign Business; Enterprise owners manage Enterprise subscriptions and seat assignment**  
C. Repository admins purchase both  
D. Students purchase Enterprise  

**Correct Answer(s):** B  

**Explanation:**  
For **Copilot Business**, **organization owners** subscribe at the **organization level**, purchase **Copilot seats**, and assign them to organization members. For **Copilot Enterprise** (or Business managed at the enterprise level), **enterprise owners** subscribe at the **enterprise layer** and centrally manage **plans and seat assignment across organizations**, delegating as needed while respecting organization boundaries.

**Tips and Tricks:**  
- Map scope to role: **org owner ↔ Business scope (one org)**, **enterprise owner ↔ Enterprise scope (multiple orgs)**.  
- If a scenario mentions **cross-org seat management, enterprise-wide policies, or enterprise billing**, it points to **enterprise owners**, not org owners.

> [!IMPORTANT]  
> Seat management is still about assigning **Copilot seats to individual users or teams**. **Organization owners** manage seats for **org-scoped Business plans**, while **enterprise owners** manage or delegate seat assignment for **enterprise-scoped plans**, without bypassing existing organization boundaries and governance.

**Source:**  
[GitHub Copilot seat assignment](https://docs.github.com/en/copilot/reference/copilot-billing/seat-assignment) (GitHub Docs)  
[Managing the GitHub Copilot plan for your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/manage-plan) (GitHub Docs)  
[Managing the GitHub Copilot plan for your enterprise](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-plan) (GitHub Docs)  
[Administer GitHub Copilot for your team](https://docs.github.com/en/copilot/how-tos/administer-copilot) (GitHub Docs)

**Question:** [098]  
Which answer best captures the **Copilot plan taxonomy** and key highlights?

**Options:**  
A. Free, Team, Premium  
B. **Free / Pro (individual), Pro+ (individual), Business (org), Enterprise (org)**  
C. Pro, Business, Enterprise only  
D. Free, Team, Enterprise Server  

**Correct Answer(s):** B  

**Explanation:**  
GitHub’s current plan taxonomy distinguishes **individual** plans (**Copilot Free, Copilot Pro, Copilot Pro+**) and **organization/enterprise** plans (**Copilot Business, Copilot Enterprise**). As you move up tiers, you gain **governance and policy controls** (such as usage reporting and content exclusion) and then **enterprise capabilities** (for example, **SSO integrations, audit logs, repo-aware chat, and advanced data controls**).

**Tips and Tricks:**  
- First separate **individual** (Free/Pro/Pro+) from **org/enterprise** (Business/Enterprise), then look for signals like **content exclusion, usage metrics, audit logs** (Business/Enterprise) or **repository-aware chat and enterprise-wide integrations** (Enterprise) to pick the right tier.  
- When you see outdated names like **“Team”** or **“Premium”**, treat them as distractors and anchor on the official **Plans** page.

> [!IMPORTANT]  
> Exam questions often test **naming**: the current taxonomy is **Free, Pro, Pro+ for individuals** and **Business, Enterprise for organizations**. Ignore legacy labels and base your answers on what the official **GitHub Copilot Plans** page shows today.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[GitHub Copilot billing](https://docs.github.com/en/billing/concepts/product-billing/github-copilot) (GitHub Docs)  
[Getting started with a GitHub Copilot plan](https://docs.github.com/en/copilot/how-tos/manage-your-account/get-started-with-a-copilot-plan) (GitHub Docs)  
[Introduction to GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) (Microsoft Learn)

**Question:** [099]  
What’s the practical contrast in **how developers invoke** Copilot features?

**Options:**  
A. **Inline suggestions:** appear near the cursor (accept with **Tab/Enter**). **Chat:** open a chat panel and prompt (supports selections).  
B. Both are automatically applied without user action  
C. Only chat can generate code; inline cannot  
D. Inline runs in the browser; chat runs only in IDEs  

**Correct Answer(s):** A  

**Explanation:**  
**Inline** is a lightweight completion experience that appears as ghost text near the cursor and is accepted via keys such as **Tab/Enter**. **Chat** is invoked by opening a chat view or inline chat, then typing prompts that can use **selected code or files as context**. Both experiences run in supported IDEs, while **Copilot Chat** is also available on **GitHub.com** and **Windows Terminal**.

**Tips and Tricks:**  
- Think **“type and accept near cursor”** for inline when you want fast completions.  
- Think **“open chat panel and converse”** for Chat when you need explanations, multi-step reasoning, or repo-aware help; many IDEs support **select code → ask in Chat** to bootstrap prompts from real code.

> [!IMPORTANT]  
> Invocation mode does **not** change trust level: both inline and Chat suggestions are **candidates** that still require compilation, testing, and review. The exam distinction is mainly about **how you start them** (accept inline vs open chat), not different governance.

**Source:**  
[Code suggestions with GitHub Copilot](https://docs.github.com/en/copilot/concepts/completions/code-suggestions) (GitHub Docs)  
[Get IDE code suggestions with GitHub Copilot](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/get-ide-code-suggestions) (GitHub Docs)  
[Chat with GitHub Copilot in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[GitHub Copilot features overview](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)

**Question:** [100]  
Can Copilot help **generate unit tests** in supported IDEs?

**Options:**  
A. No, only refactors are supported  
B. **Yes, use Copilot Chat or context prompts to generate tests for selected code**  
C. Only on Enterprise plans  
D. Only in JetBrains IDEs  

**Correct Answer(s):** B  

**Explanation:**  
Copilot Chat and prompt patterns support **test generation** for selected code. In supported IDEs you can **select a function or file and ask Copilot to generate unit (or integration) tests**, and Copilot will propose **test cases, scaffolds, and assertions** based on the surrounding context. Guides such as **“Writing tests with GitHub Copilot”** also describe using prompts or commands (for example, **/tests**) to generate tests.

**Tips and Tricks:**  
- When prompting, specify the **testing framework**, **style** (for example, xUnit, Jest, table-driven), and **edge-case expectations**.  
- Always **review and extend** generated tests so they match your team’s conventions, coverage targets, and flakiness standards.

> [!IMPORTANT]  
> Copilot-generated tests may **not cover all scenarios** or match project style perfectly. Treat them as **accelerators**, not replacements, for human-designed test strategy, coverage analysis, and code review.

**Source:**  
[Write tests with GitHub Copilot](https://docs.github.com/en/copilot/tutorials/write-tests) (GitHub Docs)  
[Chat with GitHub Copilot in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/get-started/getting-started-with-prompts-for-copilot-chat) (GitHub Docs)  
[Test with GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/guides/test-with-copilot) (VS Code Docs)

**Question:** [101]  
Is **Windows Terminal** a supported surface for **Copilot Chat**?

**Options:**  
A. No, terminal isn’t supported  
B. **Yes, Windows Terminal is listed among supported Copilot Chat surfaces**  
C. Yes, but only on GHES  
D. Only if you disable inline suggestions  

**Correct Answer(s):** B  

**Explanation:**  
GitHub includes **Windows Terminal** among the supported surfaces for Copilot Chat. With **Terminal Chat** in **Windows Terminal**, you can ask Copilot for **command suggestions, explanations, and one-off shell scripts** directly in the terminal, alongside GitHub.com, IDEs, and GitHub Mobile.

**Tips and Tricks:**  
- Use Windows Terminal chat for **shell tasks** such as command help, flags, and short scripts.  
- Use IDE or GitHub.com chat for **deeper code reasoning, multi-file changes, and repo-aware workflows**.

> [!IMPORTANT]  
> Copilot in Windows Terminal is available to **eligible Copilot customers** and still respects **plan limits** and **enterprise policies**. You must have Copilot access and configure **Windows Terminal (Canary) → Terminal Chat** to use **GitHub Copilot** as the provider.

**Source:**  
[Chat with GitHub Copilot in Windows Terminal](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-windows-terminal) (GitHub Docs)  
[Quickstart for GitHub Copilot in Windows Terminal](https://docs.github.com/en/copilot/get-started/quickstart?tool=windowsterminal) (GitHub Docs)  
[GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)  
[GitHub Copilot is now available in Windows Terminal](https://github.blog/changelog/2024-10-29-github-copilot-is-now-available-in-windows-terminal/) (GitHub Blog)

**Question:** [102]  
How can Copilot help with **documentation tasks** such as docstrings, README sections, and code comments?

**Options:**  
A. It can only generate code, not docs  
B. **Use Copilot Chat and selection-based prompts to draft docstrings, comments, and README snippets**  
C. Docs are generated automatically on every commit  
D. Only Enterprise plans can generate documentation  

**Correct Answer(s):** B  

**Explanation:**  
Copilot supports **documentation workflows**. You can select code and ask Copilot Chat to **“write docstrings,” “explain this function,” or “draft a README section”**, and include **style constraints** such as tone, audience, and format. Inline suggestions also surface comment completions near the cursor. Copilot can iteratively refine these drafts based on follow up prompts, for example “shorter,” “more beginner friendly,” or “add examples.”

**Tips and Tricks:**  
- Highlight the **relevant code** before prompting, then give Copilot a **target style**, for example “NumPy style docstrings” or “API style README section for new contributors.”  
- Guide output with **examples**, **constraints** such as audience and brevity, and **structure** such as headings or bullets, then refine with follow up prompts like “simplify” or “make more concise.”

> [!IMPORTANT]  
> Documentation assistance is available across **supported surfaces** such as IDEs and GitHub.com, but Copilot’s output is a **draft**. Always **review for accuracy, confidentiality, and tone**, especially for public READMEs or customer facing documentation.

**Source:**  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/get-started/getting-started-with-prompts-for-copilot-chat) (GitHub Docs)  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Asking GitHub Copilot questions in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[GitHub Copilot tutorials](https://docs.github.com/en/copilot/tutorials) (GitHub Docs)

**Question:** [103]  
How can Copilot assist with **debugging and fixing errors**?

**Options:**  
A. It automatically fixes all errors at build time  
B. **Use Copilot Chat to explain error messages/stack traces and propose fixes or refactors**  
C. Errors must be fixed manually; Copilot doesn’t help  
D. Only Enterprise users can use Chat for debugging  

**Correct Answer(s):** B  

**Explanation:**  
Copilot Chat can analyze **error messages, stack traces, and selected code**, then propose **root cause hypotheses**, **fixes**, and **refactors**. You can paste error messages or stack traces into Chat, or invoke Copilot from debugging contexts, and ask it to **explain the error, identify likely causes, and propose code changes**. You remain in control, review the rationale, apply suggested changes via inline edits or Copilot Edits, and retest.

**Tips and Tricks:**  
- Paste the **exact error or stack trace**, add **context** such as environment and repro steps, and request **specific outcomes**, for example “fix without changing the public API.”  
- Include **environment details, repro steps, and relevant code snippets** in your prompt, then treat Copilot’s suggestions as **starting points** that you adapt and validate with your normal debugging workflow.

> [!IMPORTANT]  
> Copilot **augments** debugging, it does **not** replace debuggers, tests, or reviews. Use it to **reason about issues and propose fixes**, while you still step through code, run tests, and perform code review before accepting changes.

**Source:**  
[Learning to debug with GitHub Copilot](https://docs.github.com/en/get-started/learning-to-code/learning-to-debug-with-github-copilot) (GitHub Docs)  
[Debug errors with GitHub Copilot Chat](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook/debug-errors) (GitHub Docs)  
[Debug with GitHub Copilot in Visual Studio](https://learn.microsoft.com/en-us/visualstudio/debugger/debug-with-copilot) (Microsoft Learn)  
[How to debug code with GitHub Copilot](https://github.blog/ai-and-ml/github-copilot/how-to-debug-code-with-github-copilot/) (GitHub Blog)

**Question:** [104]  
How can Copilot support a **TDD (red→green→refactor)** workflow?

**Options:**  
A. By auto-approving PRs when tests pass  
B. **By generating test scaffolds/cases from selections and then helping refactor after tests pass**  
C. By disabling tests during development  
D. By replacing the need for assertions  

**Correct Answer(s):** B  

**Explanation:**  
Use Copilot Chat to **generate tests** from a selected function or acceptance criteria for the **red** stage, where tests initially fail. Then iterate on the implementation with inline suggestions or Copilot Edits until the tests pass, the **green** stage. After that, ask Copilot to **propose refactors** that preserve behavior while tests guard against regressions, the **refactor** stage. You control acceptance at each step and decide what to test, when to stop, and how far to refactor.

**Tips and Tricks:**  
- Be explicit about **framework**, **coverage goals**, and **edge cases**, and ask for **table driven or parameterized** variants where appropriate.  
- Start with **small, focused tests**, prompt Copilot for additional **edge case tests**, then ask it to **simplify or restructure** code once tests are green while you keep the public API and acceptance criteria stable.

> [!IMPORTANT]  
> Copilot can **accelerate TDD** by drafting tests and refactor ideas, but **you own the quality bar**. You decide **test quality, coverage thresholds, and refactoring decisions**, and Copilot’s suggestions remain subject to your standards for coverage, style, and review.

**Source:**  
[Writing tests with GitHub Copilot](https://docs.github.com/en/copilot/tutorials/write-tests) (GitHub Docs)  
[Generate unit tests with GitHub Copilot Chat](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook/testing-code/generate-unit-tests) (GitHub Docs)  
[Develop unit tests using GitHub Copilot tools](https://learn.microsoft.com/en-us/training/modules/develop-unit-tests-using-github-copilot-tools/) (Microsoft Learn)  
[GitHub for Beginners: Test-driven development with GitHub Copilot](https://github.blog/ai-and-ml/github-copilot/github-for-beginners-test-driven-development-tdd-with-github-copilot/) (GitHub Blog)

**Question:** [105]  
What actually happens when you **accept an inline suggestion**?

**Options:**  
A. The code is auto-committed and pushed  
B. **The suggestion is inserted into your editor; you decide whether to keep, edit, or discard**  
C. The change is merged to main if CI passes  
D. An audit log entry is always generated  

**Correct Answer(s):** B  

**Explanation:**  
Inline suggestions appear **near the cursor** as ghost text and are accepted via **Tab/Enter** or editor-specific key bindings. When you accept an inline suggestion, the **ghost text becomes real code in your editor buffer**, just as if you had typed it yourself. The code is **not automatically staged, committed, or pushed**, and there is no auto-merge. You retain full control over further edits, staging, commits, and pushes through your normal Git workflow.

**Tips and Tricks:**  
- Treat accepted suggestions like any code you or a teammate wrote: **compile, test, lint, scan**, and review in a **diff view** before committing.  
- Use your usual **branching strategy, code review, and CI** processes to decide what actually lands in main.

> [!IMPORTANT]  
> Acceptance == **insert into the editor**, not **approve or merge**. Exams may try to confuse “accepting a suggestion” with “approving a change,” but **branch protection rules, required reviews, and CI checks** are still the gates that control what gets merged.

**Source:**  
[Code suggestions with GitHub Copilot](https://docs.github.com/en/copilot/concepts/completions/code-suggestions) (GitHub Docs)  
[Get IDE code suggestions with GitHub Copilot](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/get-ide-code-suggestions) (GitHub Docs)  
[Getting code suggestions in your IDE with GitHub Copilot](https://docs.github.com/en/copilot/how-tos/completions/getting-code-suggestions-in-your-ide-with-github-copilot) (GitHub Docs)  
[Quickstart for GitHub Copilot](https://docs.github.com/en/copilot/get-started/quickstart) (GitHub Docs)

**Question:** [106]  
How can Copilot help you **understand an unfamiliar file or component** in your codebase?

**Options:**  
A. It can’t, Copilot only writes code  
B. **Use selection/file prompts in Copilot Chat to summarize purpose, dependencies, and risks**  
C. Only repository-aware chat in Enterprise can explain files  
D. You must upload files to a third-party site  

**Correct Answer(s):** B  

**Explanation:**  
In supported IDEs, you can **select a file or key regions of code** and ask Copilot Chat to **summarize the purpose**, **describe dependencies**, and **highlight potential risks or edge cases**. On GitHub.com, you can open a file or repository and use Copilot to **explain what the component does** and how it fits into the project. You can chain prompts such as “explain this module,” then “list external dependencies and side effects,” then “suggest tests for critical paths” to move from a high-level overview to deeper analysis.

**Tips and Tricks:**  
- Start with **“Explain this file”** or **“Summarize this component”**, then follow up with prompts like **“list external calls,” “enumerate invariants,” or “what assumptions does this make?”**  
- Use subsequent prompts like **“suggest integration tests”** or **“identify potential failure points”** to go from understanding to concrete action items.

> [!IMPORTANT]  
> IDE Chat handles **selection/file context** in your editor, while **repository-aware chat on GitHub.com (Enterprise)** can reason over an indexed view of the **entire repo**. Both help you understand unfamiliar code, but Enterprise repo-aware chat scales better to large, multi-folder systems.

**Source:**  
[Asking GitHub Copilot questions in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[Using GitHub Copilot to explore projects](https://docs.github.com/en/get-started/exploring-projects-on-github/using-github-copilot-to-explore-projects) (GitHub Docs)  
[Quickstart for GitHub Copilot](https://docs.github.com/en/copilot/get-started/quickstart) (GitHub Docs)  
[About GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)

**Question:** [107]  
Which is the **best-crafted prompt**?

**Options:**  
A. Write a function  
B. **Write a Python function to reverse a string using slicing**  
C. Function in code  
D. Suggest some code  

**Correct Answer(s):** B  

**Explanation:**  
Effective prompts specify **language**, **task**, and **method/constraints**. Stating **“Python”** + **“reverse a string”** + **“using slicing”** removes ambiguity and guides the model to the intended pattern. A well-crafted prompt usually names the **language**, the **action**, the **object**, and any **key constraint** in a single concise sentence, so Copilot does less guessing and more targeted completion.

**Tips and Tricks:**  
- Use a simple checklist: **Language + Action + Object + Constraint**, for example, “**Python: write a function to reverse a string using slicing**.”  
- Name the **language/tooling** and the **desired approach** (“using regex,” “with recursion,” “O(n) space”).  
- Add the **target signature/output format** if you care about it, and avoid vague prompts like “write a function” that leave everything unspecified.

> [!IMPORTANT]  
> Prompt quality is about **signal density**, not verbosity. Pack **intent, scope, and constraints** into a short prompt. In exams, the best answer is usually the one that explicitly names the **language**, **task**, and **technique**, instead of a generic “do something” request.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [108]  
How do you improve **ambiguous prompts**?

**Options:**  
A. Use shorter prompts  
B. **Provide more context and details**  
C. Avoid specifying language  
D. Retry without changes  

**Correct Answer(s):** B  

**Explanation:**  
Ambiguous prompts force the model to guess. Adding **specific context** (file or selection, domain facts), **clear intent** (what to build or change), and **constraints** (language, framework, format, performance or style requirements) reliably improves accuracy. Define **inputs/outputs** and minimal **acceptance criteria** so the model follows instead of guessing, matching the guidance to **avoid ambiguity by adding project context, clear goals, and specific requirements**.

**Tips and Tricks:**  
- Apply a refinement loop: **add context (where), add intent (what), add constraints (how/limits)** when suggestions are off target.  
- Scope to a **selection/file**, pin **language/tooling/version**, and ask for a **specific output format** (for example, “pytest tests,” “JSON schema,” “SQL query”).  
- Add **constraints** (complexity, security, style) and **edge cases** to reduce variance; “shorter prompt,” “no language,” or “retry unchanged” rarely fixes ambiguity.

> [!IMPORTANT]  
> Ambiguity is resolved by **specificity**, not by brevity. High-signal prompts align on **intent, constraints, and available context**; low-signal prompts make the model infer too much. In multi-language or multi-framework repos, explicitly name the **language/framework** and **exact output format** (pytest test, JSON schema, SQL) instead of hoping Copilot will guess correctly.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [109]  
Which technique most reliably boosts output quality?

**Options:**  
A. Use vague prompts  
B. **Use detailed instructions with examples**  
C. Avoid comments in code  
D. Skip specifying input or output  

**Correct Answer(s):** B  

**Explanation:**  
Combining **explicit instructions** with **small, concrete examples** anchors the format, tone, and structure the model should match, reducing guesswork. The prompt-engineering guidance explicitly encourages **“give examples”** so Copilot can see the pattern you want and apply it to new cases, instead of inventing style and structure on its own.

**Tips and Tricks:**  
- Provide a **2–3 line exemplar** that shows naming, error handling, and docstring or comment style, then ask Copilot to **“match this style”** for new code.  
- State **steps/constraints** (algorithms, libraries, complexity limits) and include **inputs/outputs** plus a brief **acceptance check** (for example, “handle empty input and timeouts”).  
- Prefer **tiny but high-fidelity examples** over long descriptions: they give Copilot a concrete pattern to follow.

> [!IMPORTANT]  
> Examples act as **pattern anchors**. Even a very small, high-quality example can constrain structure and tone better than multiple paragraphs of prose, raising **signal density** without bloat. Exam answers that mention **instructions + examples** usually reflect this best-practice guidance.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[GitHub Copilot Chat Cookbook](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook) (GitHub Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat) (GitHub Docs)

**Question:** [110]  
Why does adding **examples** help?

**Options:**  
A. Examples distract the AI  
B. **They align output with the desired style/pattern**  
C. They reduce Copilot’s ability to generate code  
D. They slow completions  

**Correct Answer(s):** B  

**Explanation:**  
Short **few-shot examples** show the model the **shape** you want (naming, layout, docstrings, tests), so generated output conforms to your pattern. Examples effectively **“show, not tell”** the desired **style, structure, and tone**, which is why prompt-engineering guidance recommends **“give examples”** so Copilot can generalize from patterns instead of guessing.

**Tips and Tricks:**  
- Prefer **tiny but high-fidelity** examples over long descriptions.  
- Use a **good vs. bad** pair when style distinctions are subtle.  
- Keep examples **project-realistic** (imports, assertions, error styles), and ask Copilot to **“follow this pattern for the next case”** rather than relying on prose-only style descriptions.

> [!IMPORTANT]  
> Examples increase **signal** by demonstrating format and tone. One precise, project-idiomatic example often outperforms multiple paragraphs of general guidance. Treat examples as **pattern anchors** that pull Copilot toward the structure and style you actually want.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[GitHub Copilot Chat cookbook](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook) (GitHub Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat) (GitHub Docs)

**Question:** [111]  
Why is **context** crucial in prompts?

**Options:**  
A. It slows responses  
B. **It helps Copilot generate relevant and accurate suggestions**  
C. It prevents completions  
D. It reduces security  

**Correct Answer(s):** B  

**Explanation:**  
Copilot conditions on the **surrounding code, the current file, and your prompt**. Because Copilot does **prediction, not execution**, the closer and richer the context around the prompt, the more **relevant and accurate** the suggestions. Prompts that reference the right file/selection, types, interfaces, and data shapes give Copilot a much clearer target than generic, repo-agnostic requests.

**Tips and Tricks:**  
- Work from a **selection or file near the change** instead of an empty buffer.  
- Include **domain facts**, **interfaces**, **data shapes**, and any **non-obvious constraints** (performance, style, APIs) in the prompt.  
- Build a habit of **selecting the relevant code or opening the right file** before asking a question, especially for complex refactors or bug fixes.

> [!IMPORTANT]  
> Context is one of the **highest-impact signals**. **Context + constraints** consistently outperform global prompts with no local code. Exam-wise, prefer answers that mention **nearby code, selections, or file context** over those that suggest asking Copilot “from scratch” with no context.

**Source:**  
[Code suggestions with GitHub Copilot](https://docs.github.com/en/copilot/concepts/completions/code-suggestions) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[Asking GitHub Copilot questions in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[Getting started with GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/getting-started) (VS Code Docs)

**Question:** [112]  
What should you do if Copilot generates **irrelevant suggestions**?

**Options:**  
A. Stop using Copilot  
B. **Refine or rephrase the prompt with more context**  
C. Use shorter prompts  
D. Disable duplication detection  

**Correct Answer(s):** B  

**Explanation:**  
Irrelevance usually means **missing or misaligned signals**. Instead of giving up or just retrying, you improve quality by **refining the prompt with more context and clearer intent**: add a selection/file, specify **inputs/outputs**, name the **language/tooling**, and set **constraints** so Copilot has less room to guess.

**Tips and Tricks:**  
- When output is off, tighten scope: **selection/file**, clarify goal (**what you want**), and add **constraints** (**how/limits**).  
- Constrain the **scope** and **format** of the output (for example, “one function + one pytest test”).  
- Provide a **mini spec** or **tiny example** and iterate; for multi-step tasks, ask for **“plan → code”** to structure the work.

> [!IMPORTANT]  
> Each refinement should intentionally **remove a known ambiguity**. You’re not just “trying again”; you’re **adding intent, context, and constraints** so the next suggestion has less room to drift. Shorter prompts alone rarely fix irrelevance—**better, richer prompts** do.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[GitHub Copilot Chat cookbook](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook) (GitHub Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat) (GitHub Docs)

**Question:** [113]  
Which practice helps Copilot match **project style**?

**Options:**  
A. Avoid adding comments  
B. **Add snippets and style examples**  
C. Use vague instructions  
D. Skip output format  

**Correct Answer(s):** B  

**Explanation:**  
Supplying **style exemplars** (naming, error handling, test layout, docstrings) guides Copilot to mirror your project’s conventions. Prompt-engineering guidance explicitly recommends providing **project-idiomatic examples** so Copilot can follow your patterns instead of inventing its own style.

**Tips and Tricks:**  
- Paste a **short, realistic snippet** from your codebase (imports, naming, assertions, logging) and ask Copilot to **“match this style”** for new functions or tests.  
- Call out **linting and testing expectations** (for example, ESLint rules, pytest layout) so structure and formatting align with your toolchain.  
- Use code, not prose, to teach style: examples of real code carry much stronger signals than abstract “clean code” descriptions.

> [!IMPORTANT]  
> Style is best taught with **code**, not prose. A small, accurate snippet sets stronger constraints than a long paragraph describing conventions. For exams, answers that mention **snippets and style examples** are aligned with GitHub’s official prompt-engineering guidance.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[GitHub Copilot Chat Cookbook](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [114]  
Which statement best describes **what Copilot relies on during inference**?

**Options:**  
A. Runtime execution of your code  
B. **Your prompts, file contents, and surrounding code context**  
C. Web searches via Bing  
D. Pre-stored templates  

**Correct Answer(s):** B  

**Explanation:**  
Copilot performs **contextual prediction**, not execution. It uses your **prompt**, the **current file and surrounding code**, and other allowed context (for example, chat history or repo index) to generate suggestions. It does **not** run your program or call external web search at inference time; quality depends on how good the **available context** is.

**Tips and Tricks:**  
- Open the **relevant files** and use **selection or file context** when prompting so Copilot sees the right code.  
- Provide **type information, interfaces, and data shapes** in the code or prompt to reduce ambiguity.  
- For broader reasoning, use **Chat with selection/file context** instead of asking about a repo in the abstract with no nearby code.

> [!IMPORTANT]  
> Copilot doesn’t execute your program or browse the web; it **infers from available context** (prompts + code). Exam answers that mention **prompts, file contents, and surrounding code context** are correct; options that mention **runtime execution** or **Bing/web search** are distractors.

**Source:**  
[Code suggestions with GitHub Copilot](https://docs.github.com/en/copilot/concepts/completions/code-suggestions) (GitHub Docs)  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[Using GitHub Copilot in your IDE: Tips, tricks, and best practices](https://github.blog/developer-skills/github/how-to-use-github-copilot-in-your-ide-tips-tricks-and-best-practices/) (GitHub Blog)

**Question:** [115]  
What does **content exclusion** let organizations do (and why is it relevant to prompting)?

**Options:**  
A. Speed up Copilot  
B. **Prevent specified repos/paths/file types/patterns from being used as input context**  
C. Disable Copilot entirely  
D. Publish private code  

**Correct Answer(s):** B  

**Explanation:**  
**Content exclusion** lets organizations with **Copilot Business or Enterprise** define what **input context** Copilot can see. Admins can exclude specific **repositories, directories/paths, file types, or pattern-based rules**, preventing that content from being used as context for suggestions in IDEs and on GitHub.com, even if users prompt near it. This keeps secrets and sensitive code out of Copilot’s prompt context.

**Tips and Tricks:**  
- Use content exclusion to protect **secrets, regulated data, and “crown-jewel” services**, scoping rules by **repo, path, file type, or pattern**.  
- Pair content exclusion (governing **inputs**) with **code referencing/public-code filtering** (governing **outputs**) for a complete governance posture.  
- Remember that exclusion shapes **what Copilot can read**, not how similar its outputs are to public code; that’s handled by code referencing and related policies.

> [!IMPORTANT]  
> Think **inputs vs outputs**: **Content exclusion** is an **org/enterprise governance control** that limits the **inputs** Copilot can see, starting at **Business**. **Code referencing** governs **outputs** and their similarity to public code. Exams frequently test this split, so map questions about “what Copilot can see” to **content exclusion** on Business/Enterprise plans.

**Source:**  
[Content exclusion for GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Configure content exclusion for GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Content exclusion for GitHub Copilot in IDEs is generally available](https://github.blog/changelog/2024-11-12-content-exclusion-ga/) (GitHub Blog)

**Question:** [116]  
Which **Copilot plans** include **content exclusion**?

**Options:**  
A. Free and Individual  
B. **Business and Enterprise**  
C. Individual only  
D. Free only  

**Correct Answer(s):** B  

**Explanation:**  
**Content exclusion** is an **organization-level** control available on **Copilot Business** and **Copilot Enterprise**. It lets org and enterprise admins define which **repositories, directories/paths, file types, or patterns** Copilot can use as **input context** in IDEs and on GitHub.com. Individual plans do **not** expose these admin governance features.

**Tips and Tricks:**  
- When a scenario says an **org admin defines which code Copilot can see**, think **Business/Enterprise with content exclusion**, not individual plans.  
- Use content exclusion to keep **secrets, regulated data, and “crown-jewel” repos** out of Copilot’s context, even if users prompt near them.  
- Combine **content exclusion (inputs)** with **enterprise policies and code referencing/public-code filtering (outputs)** for end-to-end governance.

> [!IMPORTANT]  
> Scope boundary: **Content exclusion** starts at **Copilot Business** and extends to **Copilot Enterprise**. It is an **org/enterprise capability**, not an individual plan feature, and it governs **what Copilot can read** as context, not whether outputs are similar to public code.

**Source:**  
[Content exclusion for GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Configure content exclusion for GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choosing your enterprise’s plan for GitHub Copilot](https://docs.github.com/en/copilot/get-started/choosing-your-enterprises-plan-for-github-copilot) (GitHub Docs)

**Question:** [117]  
Which prompt gives Copilot the **clearest output target**?

**Options:**  
A. “Summarize this.”  
B. **“Summarize this function in 3 bullets for junior devs; include inputs, outputs, and one caveat.”**  
C. “Explain code.”  
D. “Write notes.”  

**Correct Answer(s):** B  

**Explanation:**  
Stating the **audience**, **length/structure**, and **must-include items** creates a concrete target. A prompt like “summarize this function in 3 bullets for junior devs; include inputs, outputs, and one caveat” defines **format (bullets)**, **length (3)**, **audience (junior devs)**, and **required content (inputs/outputs/caveat)**, so Copilot has a very clear output shape and less room to guess.

**Tips and Tricks:**  
- Use the pattern: **do X, in Y format, for Z audience, include fields A/B/C**.  
- Always specify **format** (bullets, table, code block), **length** (3 bullets, 1 paragraph), and **audience/tone** (junior devs, SREs, product managers).  
- Call out **must-include fields** such as inputs, outputs, risks, or caveats to make results consistent and comparable.

> [!IMPORTANT]  
> Prompt quality is about **signal density**, not verbosity. The best exam answer is the one that explicitly defines **structure, length, audience, and required fields**, giving Copilot a clear, exam-ready target instead of an open-ended “summarize” or “explain” request.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [118]  
When asking Copilot to refactor code, which prompt is best?

**Options:**  
A. “Improve this.”  
B. **“Refactor to pure functions; no side effects; keep same public API; add docstrings; return early on invalid input.”**  
C. “Make it cleaner.”  
D. “Rewrite completely.”  

**Correct Answer(s):** B  

**Explanation:**  
Refactor prompts work best when constraints are explicit: **style** (pure functions, no side effects), **compatibility** (keep the same public API and behavior), **non-functional requirements** (add docstrings), and **guardrails** (return early on invalid input). This matches refactoring guidance that structure should change but **observable behavior must remain the same** and tests should continue to pass.

**Tips and Tricks:**  
- Always lock **compatibility**: “keep signatures and behavior unchanged; existing tests must still pass.”  
- State **style goals** (immutability, dependency injection, early returns) and non-functional requirements (docstrings, logging, error handling).  
- Use vague prompts like “improve this” or “make it cleaner” only as a starting point; for safe refactoring, spell out what may change and what must not.

> [!IMPORTANT]  
> Make the target **unambiguous**: name what must **change** (structure, style) and what must **not change** (contract, behavior). Exam questions favor prompts that clearly protect API/behavior while guiding structural changes; options that say “rewrite completely” or omit compatibility constraints are usually wrong for refactor scenarios.

**Source:**  
[Refactor code with GitHub Copilot](https://docs.github.com/en/copilot/tutorials/refactor-code) (GitHub Docs)  
[Develop unit tests using GitHub Copilot tools](https://learn.microsoft.com/en-us/training/modules/develop-unit-tests-using-github-copilot-tools/) (Microsoft Learn)  
[Refactor existing code using GitHub Copilot (lab)](https://microsoftlearning.github.io/mslearn-github-copilot-dev/Instructions/Labs/LAB_AK_05_refactor_improve_existing_code.html) (Microsoft Learn Lab)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [119]  
Which prompt best reduces **hallucinations** when generating API code?

**Options:**  
A. “Use the Foo API.”  
B. **“Use Foo API v3; only endpoints /users/{id}, /users/search; TypeScript; fetch; no undocumented fields; include error handling for 4xx/5xx.”**  
C. “Write users code.”  
D. “Guess the latest endpoints.”  

**Correct Answer(s):** B  

**Explanation:**  
Hallucinations drop when you **fix the API version**, **restrict which endpoints can be used**, and **specify language and tooling**. A prompt like “Use Foo API v3; only endpoints /users/{id}, /users/search; TypeScript; fetch; no undocumented fields; include error handling for 4xx/5xx” defines a **constrained, testable contract** instead of an open-ended request, and “no undocumented fields” explicitly discourages Copilot from inventing properties or methods.

**Tips and Tricks:**  
- Always **pin the API version** (for example, “Foo API v3”) and, where possible, link to or reference the **official docs**.  
- List **allowed endpoints** and explicitly **forbid undocumented fields or endpoints**, then require **error/timeout handling** for 4xx/5xx responses.  
- Ask for **types/interfaces** (for example, TypeScript interfaces) so any hallucinated fields are surfaced quickly by the type system or tests rather than slipping into production.

> [!IMPORTANT]  
> For hallucination questions, look for prompts that **lock down version and endpoints and forbid undocumented fields**. Vague prompts like “use the Foo API” or “guess the latest endpoints” actively encourage speculative behavior, while constrained prompts turn Copilot’s output into **verifiable stubs** you can test immediately.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[How to write better prompts for GitHub Copilot](https://github.blog/developer-skills/github/how-to-write-better-prompts-for-github-copilot/) (GitHub Blog)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [120]  
You want table-driven unit tests. Which prompt is best?

**Options:**  
A. “Write tests.”  
B. **“Generate table-driven tests in Go for Parse(), covering empty, invalid, edge lengths; include names and wantErr.”**  
C. “Test everything.”  
D. “Add some asserts.”  

**Correct Answer(s):** B  

**Explanation:**  
Specifying **language** (Go), **test style** (“table-driven tests”), the **target function** (`Parse()`), and **cases/fields** (“covering empty, invalid, edge lengths; include names and wantErr”) gives Copilot a concrete, idiomatic template to expand. This matches common Go patterns where tests use a `[]struct{ name string; input …; want …; wantErr bool }` table and iterate over named cases.

**Tips and Tricks:**  
- Name the **testing framework/style** explicitly, for example, “table-driven tests in Go using the standard `testing` package.”  
- Enumerate **edge cases and inputs/outputs** (empty, invalid, boundary values) and ask for fields like `name`, `input`, `want`, and `wantErr` so readability and diagnostics are built in.  
- Once you have a good canonical table, ask Copilot to **“add more table-driven cases matching this style”** instead of starting from a generic “write tests” prompt.

> [!IMPORTANT]  
> Tests are **format-sensitive**: the more you constrain **layout, style, and cases** in the prompt (language, table-driven structure, edge cases, fields), the higher the chance Copilot matches your project’s testing standards on the first try. Exam answers that pin **language + test style + edge cases + fields** are usually the correct choice.

**Source:**  
[Writing tests with GitHub Copilot](https://docs.github.com/en/copilot/tutorials/write-tests) (GitHub Docs)  
[Asking GitHub Copilot questions in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[GitHub for Beginners: Test-driven development with GitHub Copilot](https://github.blog/ai-and-ml/github-copilot/github-for-beginners-test-driven-development-tdd-with-github-copilot/) (GitHub Blog)  
[Develop unit tests using GitHub Copilot tools](https://learn.microsoft.com/en-us/training/modules/develop-unit-tests-using-github-copilot-tools/) (Microsoft Learn)