# Detailed Practice Test 09 - Answer Sheet & Explanation

**Question:** [241]  
Which task is **most appropriate** to assign to **GitHub Copilot coding agent in Agent mode**?  

**Options:**  
A. Designing a brand-new architecture for a mission-critical payments platform with no existing code, tests, or safety nets  
B. Handling an active production incident involving PII exposure and complex security tradeoffs  
C. **Updating a shared UI component library across the repo to use a new button component, running tests in the agent’s environment, and opening a PR with changes**  
D. Rewriting all pricing business logic from scratch based only on a vague one-line description  

**Correct Answer(s):** C  

**Explanation:**  
GitHub recommends assigning the coding agent **clear, well-scoped tasks** with concrete descriptions and acceptance criteria, such as updating a UI component across the repository and running tests before opening a PR. Open-ended architecture work, live incidents involving PII or security tradeoffs, or vague “rewrite everything” tasks fall outside recommended usage and should remain human-owned, with Copilot used only for small, reviewable suggestions.  

**Tips and Tricks:**  
- Treat the **issue or task description as the agent’s prompt**: describe the problem, acceptance criteria, and the files or modules to touch.  
- Start with **contained tasks** (bug fixes, UI updates, test coverage, documentation, technical debt) before attempting larger refactors.  
- Keep **critical, security, PII, or incident-response tasks** out of Agent mode; use Copilot as a helper around them, not as the primary owner.  

> [!IMPORTANT]  
> If a scenario mentions **broad, ambiguous, production-critical, or PII/security-sensitive work**, the exam-safe posture is: **do not give that to the coding agent**. Prefer **well-scoped, non-critical tasks** that result in a PR you can fully review.

**Correct and Wrong:**  
Option C is correct because it describes a **repo-wide but bounded UI update** with tests and a PR, exactly the kind of task GitHub calls out as a good fit for the coding agent. The other options push the agent into **architecture-from-scratch**, **active production incidents**, or **vague, high-risk rewrites** without clear scope or safety nets, all of which should remain under direct human control.  

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[Onboarding your AI peer programmer: setting up GitHub Copilot coding agent for success](https://github.blog/ai-and-ml/github-copilot/onboarding-your-ai-peer-programmer-setting-up-github-copilot-coding-agent-for-success/) (GitHub Blog)  

**Question:** [242]  
Which statement best describes **where and how** GitHub Copilot coding agent runs your code changes?

**Options:**  
A. It compiles and runs everything directly on each developer’s local machine using their local tools  
B. It runs only in a fixed, shared VM that you manually provision and manage  
C. **It uses an ephemeral development environment powered by GitHub Actions, where it can explore the repo, make changes, and run tests/linters before opening a PR**  
D. It can only edit text and cannot run tests or tools at all  

**Correct Answer(s):** C  

**Explanation:**  
Copilot coding agent works in an **ephemeral development environment** powered by **GitHub Actions**, separate from your local IDE. In that environment it can clone the repository, explore the code, change files, and run tests or linters before proposing those changes in a pull request for review. You can customize this environment so it has the tools and dependencies your project needs.

**Tips and Tricks:**  
- Associate **“ephemeral environment” + “GitHub Actions” + “branch + PR”** with coding agent behavior.  
- Remember that the agent does **not** run directly in your IDE; it uses a GitHub-hosted dev environment.  
- Use environment customization so the agent can build and test reliably before opening a PR.

> [!IMPORTANT]  
> On the exam, phrases like **“ephemeral environment powered by GitHub Actions”** or **“runs tests/linters before opening a PR”** are strong signals that the scenario is describing the **Copilot coding agent**, not inline suggestions or simple Chat.

**Correct and Wrong:**  
The correct option is the only one that matches GitHub’s description of the coding agent: it runs in an **ephemeral GitHub Actions–powered environment**, changes code in a branch, and opens a PR. The other options incorrectly suggest it runs only on local machines, uses a fixed manual VM, or can’t run tools at all, none of which align with the documented behavior.

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[Customizing the development environment for GitHub Copilot coding agent](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/customize-the-agent-environment) (GitHub Docs)  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  


**Question:** [243]  
Which statement about **plan availability** for GitHub Copilot coding agent is correct?

**Options:**  
A. Coding agent is available only on Copilot Enterprise  
B. Coding agent is available on all Copilot plans, including Copilot Free  
C. **Coding agent is available with Copilot Pro, Copilot Pro+, Copilot Business, and Copilot Enterprise**  
D. Coding agent is available only on Copilot Business and Enterprise (not on individual plans)  

**Correct Answer(s):** C  

**Explanation:**  
GitHub’s documentation states that **GitHub Copilot coding agent** is available with **Copilot Pro**, **Copilot Pro+**, **Copilot Business**, and **Copilot Enterprise**. Copilot Free is not listed as supporting the coding agent, and Pro/Pro+ are the individual plans that enable its use outside organizations.

**Tips and Tricks:**  
- Remember the set: **Pro, Pro+, Business, Enterprise** all include coding agent; **Free does not**.  
- Any option that claims coding agent is “Enterprise-only” or “on all plans including Free” is incomplete or wrong.  
- When a stem mentions coding agent in a personal context, think **Pro/Pro+**; for org-wide use, think **Business/Enterprise**.

> [!IMPORTANT]  
> For plan questions, keep this mental model: **coding agent is available on Copilot Pro, Pro+, Business, and Enterprise, but not on Copilot Free**.

**Correct and Wrong:**  
The correct option explicitly lists **Pro, Pro+, Business, and Enterprise**, which matches GitHub’s plan documentation. The other options either over-restrict coding agent to Enterprise-only, incorrectly include Copilot Free, or omit the individual Pro tiers that also support the feature.

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  


**Question:** [244]  
You want Copilot coding agent to **build and test faster and more reliably** when it works on tasks in your repository. What should you do?

**Options:**  
A. Ask every developer to run `npm install` locally before assigning issues to Copilot  
B. **Add a `copilot-setup-steps.yml` file that pre-installs your project’s dependencies in the agent’s environment**  
C. Disable all tests so the agent doesn’t need dependencies  
D. Create a `.gitignore` entry for `node_modules` so Copilot can infer everything automatically  

**Correct Answer(s):** B  

**Explanation:**  
Because Copilot coding agent runs in an **ephemeral GitHub-hosted environment**, it cannot rely on developers’ local setups. GitHub recommends adding a **`copilot-setup-steps.yml`** file that installs the required languages, tools, and dependencies so the agent can reliably build, test, and lint your project before proposing a pull request.

**Tips and Tricks:**  
- Use `copilot-setup-steps.yml` to install **runtimes, package managers, build tools, and test dependencies**.  
- Keep the setup **minimal but sufficient**: only what’s needed for builds, tests, and linters to succeed.  
- Never “optimize” by disabling tests; tests are core guardrails for AI-driven changes.

> [!IMPORTANT]  
> On exam questions about **speeding up or stabilizing the coding agent**, look for **pre-installing dependencies** in the agent environment via `copilot-setup-steps.yml` rather than changing developers’ local machines or disabling tests.

**Correct and Wrong:**  
The correct option is the only one that configures the **agent’s own environment** with a `copilot-setup-steps.yml` file, as GitHub recommends. The other options either focus on local setup, turn off tests entirely, or rely on `.gitignore` in a way that does nothing to prepare the agent’s environment, so they do not solve the reliability problem.

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[Customizing the development environment for GitHub Copilot coding agent](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/customize-the-agent-environment) (GitHub Docs)  


**Question:** [245]  
Which scenario best reflects **GitHub’s guidance on when *not* to assign a task** to Copilot coding agent?

**Options:**  
A. Updating CSS variables across the design system and running existing visual regression tests  
B. Improving unit test coverage for a well-documented service with clear acceptance criteria  
C. Refactoring a small helper module to remove duplication, with existing tests in place  
D. **Investigating and fixing a live incident involving PII leakage and authentication failures in production**  

**Correct Answer(s):** D  

**Explanation:**  
GitHub explicitly calls out **sensitive and critical tasks**, such as live production incidents and issues involving **PII, authentication, or security trade-offs**, as work that should **remain human-led**. In contrast, scoped tasks like UI tweaks, test improvements, or small refactors with tests are considered good candidates for the coding agent because they are PR-driven and testable.

**Tips and Tricks:**  
- Do **not** assign production incidents, PII/security/auth tasks, or high-risk refactors without clear scope to the coding agent.  
- Do assign **well-scoped, non-critical tasks** with tests and clear acceptance criteria.  
- Use the agent as an **assistant**, not as the primary owner of incident response or security-sensitive decision making.

> [!IMPORTANT]  
> If a scenario mentions **“production incident,” “PII,” “authentication failures,” or “incident response,”** the safe exam answer is: handle it with humans and use Copilot only for small, reviewable pieces around it.

**Correct and Wrong:**  
The correct option is the only one that describes a **live production incident involving PII and auth**, which GitHub documentation explicitly treats as out of scope for the coding agent. The other options are routine, testable engineering tasks exactly the kind of work that can safely be delegated to the agent under normal PR and test workflows.

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  


**Question:** [246]  
You need to **standardize logging** in a small service:  
- Update a helper to emit **structured JSON logs**  
- Add one new log call in a **single controller**  
- You want to **review a focused diff** before any changes land, and you don’t need the tool to run tests or touch other files.  

Which Copilot capability is the **best fit** for this task?

**Options:**  
A. Use the Copilot coding agent in Agent mode to refactor the entire repository  
B. **Use Copilot Edits in Edit mode on the two affected files**  
C. Ask Copilot Chat to “fix logging everywhere” without specifying files  
D. Use repository-aware chat on GitHub.com to auto-merge a PR  

**Correct Answer(s):** B  

**Explanation:**  
**Copilot Edits – Edit mode** is designed for **targeted, user-scoped changes**: you pick the files to modify, ask for the change, and then review a **proposed diff** before applying it. For a small, localized logging update in two files, Edit mode keeps the scope tight and the diff easy to understand, without the overhead or autonomy of the coding agent.

**Tips and Tricks:**  
- Choose Edit mode when you can **name the files and functions** you want changed.  
- Keep prompts specific, for example: “Update `log_error()` to emit JSON and add a log in `UserController.handle()`.”  
- Review the diff and run tests locally after applying the edit to confirm behavior.

> [!IMPORTANT]  
> Think in terms of **scope and control**: use **Edit mode** for small, predictable diffs in known files, and reserve **Agent mode** for broader, multi-step workflows that span multiple files and tools.

**Correct and Wrong:**  
The correct option selects **Copilot Edits in Edit mode**, which matches the small, two-file logging refactor described. Using the coding agent to refactor the entire repository, asking Chat to “fix logging everywhere,” or trying to auto-merge via chat all either over-expand the scope or skip normal review, making them weaker and less aligned with GitHub’s recommended usage.

**Source:**  
[GitHub Copilot features](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[About GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)  


**Question:** [247]  
How does **Copilot coding agent** typically operate on a task assigned from GitHub.com?

**Options:**  
A. It edits files directly and permanently in your local IDE without using branches or pull requests  
B. It connects to a self-hosted GitHub Enterprise Server (GHES) instance and runs entirely on-premises  
C. **It initializes a cloud dev environment (GitHub Actions–powered), makes changes in a branch, and drafts a pull request for review**  
D. It automatically merges its changes to the default branch as soon as tests pass, bypassing normal review rules  

**Correct Answer(s):** C  

**Explanation:**  
Copilot coding agent runs in an **ephemeral cloud development environment** backed by **GitHub Actions**, where it clones the repo, works on a **separate branch**, and maintains a **draft pull request** for you to review. It does not run on GHES, does not make direct local edits, and cannot auto-merge; your existing **branch protections, reviews, and status checks** still apply.

**Tips and Tricks:**  
- Think of coding agent as a **GitHub Actions–hosted teammate** that always works via branches and PRs.  
- Use it from issues or pull requests when you want **“PR-first” automation** rather than local edits.  
- Treat its PRs as **draft contributions** that still need human review and CI.

> [!IMPORTANT]  
> Coding agent is **PR-centric**: it works in a **GitHub Actions environment**, pushes to its own branch, and opens a **draft PR**. It never bypasses GitHub’s normal governance (branch protections, reviews, workflows).

**Correct and Wrong:**  
The correct option is the only one that mentions an **ephemeral cloud environment**, branch-based changes, and a **draft PR workflow**, which matches how coding agent is implemented. The other options incorrectly suggest local-only edits, on-prem GHES support, or automatic merging, all of which conflict with GitHub’s documented behavior.

**Source:**  
[GitHub Copilot coding agent](https://docs.github.com/en/copilot/tutorials/coding-agent) (GitHub Docs)  
[About GitHub Copilot coding agent](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[GitHub Copilot coding agent 101](https://github.blog/ai-and-ml/github-copilot/github-copilot-coding-agent-101-getting-started-with-agentic-workflows-on-github/) (GitHub Blog)  


**Question:** [248]  
Which responsibilities remain with **developers/teams** when using Copilot coding agent? *(Choose all that apply.)*  

**Options:**  
A. **Reviewing and approving the pull request before merge**  
B. **Ensuring tests, linters, and security scans pass for the changes**  
C. Allowing the agent to auto-merge its pull requests directly into production branches as long as tests pass  
D. **Defining safe, well-scoped tasks and issues for the agent to work on**  

**Correct Answer(s):** A, B, D  

**Explanation:**  
Copilot coding agent is an **assistive contributor**, not an autonomous release system. Teams still own the work: they must **scope issues clearly**, **review agent-created PRs**, and ensure **tests, linters, security checks, and policies** all pass before merging. The agent cannot approve or merge its own PRs and is treated much like an external contributor.

**Tips and Tricks:**  
- Look for words like **“review,” “CI checks,” “team responsibility”** these are always human roles.  
- Keep **branch protections, required reviews, and status checks** enabled for agent-created PRs.  
- Write issues with clear **intent, constraints, and acceptance criteria** so the agent doesn’t have to guess.

> [!IMPORTANT]  
> Coding agent can **propose changes** but cannot approve or merge them; **independent human review and CI** remain mandatory safeguards in both regulated and non-regulated environments.

**Correct and Wrong:**  
Options A, B, and D are correct because they emphasize **human review**, **quality and security checks**, and **clear task definition**, which GitHub explicitly calls out as team responsibilities. Option C is wrong because the agent cannot merge its own PRs or bypass branch protections and review rules.

**Source:**  
[About GitHub Copilot coding agent](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[Piloting GitHub Copilot coding agent in your organization](https://docs.github.com/en/copilot/tutorials/coding-agent/pilot-coding-agent) (GitHub Docs)  
[Leveling up code reviews and pull requests with Copilot](https://learn.microsoft.com/en-us/training/modules/level-up-code-reviews-pull-requests-github-copilot/) (Microsoft Learn)  


**Question:** [249]  
How do you customize the **environment** that Copilot coding agent uses when working on a repository?

**Options:**  
A. By editing a personal `.copilot-env.json` file in your local home directory, which the agent automatically syncs and executes in the cloud  
B. By updating your local dev container configuration and assuming the agent will mirror that environment without any repository-side config  
C. **By adding a `copilot-setup-steps.yaml` file that declares setup steps (tools, commands, environment) for the agent’s cloud environment**  
D. By setting environment variables only in the GitHub UI and ignoring any workflow files in the repository  

**Correct Answer(s):** C  

**Explanation:**  
To make coding agent runs **reliable and fast**, you define setup instructions in a dedicated **`copilot-setup-steps` workflow** (for example, `.github/workflows/copilot-setup-steps.yml`) that installs tools, dependencies, and configuration in the agent’s **GitHub Actions–powered environment** before it starts modifying code. Local dev containers and dotfiles are **not** automatically reused by the agent.

**Tips and Tricks:**  
- Use `copilot-setup-steps` to install **languages, package managers, build tools, and test dependencies** needed for your repo.  
- Keep the setup **minimal but sufficient** to run builds, tests, and linters efficiently.  
- Store secrets as **GitHub Actions secrets/variables**, not directly in the workflow file.

> [!IMPORTANT]  
> Coding agent’s environment is **ephemeral and separate** from your local machine configure it explicitly with `copilot-setup-steps` so tests and builds behave consistently on every run.

**Correct and Wrong:**  
The correct option is the only one that describes the documented **workflow-based setup** used by coding agent. The other options incorrectly assume that local configuration is reused automatically or that only ad-hoc UI variables matter, which is not how the agent’s environment is provisioned.

**Source:**  
[Customizing the development environment for GitHub Copilot coding agent](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/customize-the-agent-environment) (GitHub Docs)  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[Copilot coding agent custom setup steps](https://github.blog/changelog/2025-07-30-copilot-coding-agent-custom-setup-steps-are-more-reliable-and-easier-to-debug/) (GitHub Blog)  


**Question:** [250]  
Which scenario is **most appropriate** for assigning work to **Copilot coding agent**?

**Options:**  
A. Directly rotating production database credentials and applying schema changes in a live production environment  
B. **Implementing a feature from a well-defined issue (with acceptance criteria), where the agent can work in a branch and open a pull request for review**  
C. Performing manual hotfixes during a live production outage using ad-hoc shell access on production hosts  
D. Automatically configuring enterprise SSO, audit logging, and other security-sensitive admin settings without human oversight  

**Correct Answer(s):** B  

**Explanation:**  
GitHub guidance is clear: coding agent is best used for **code-level tasks** that fit within a **branch + PR + tests** workflow like implementing a feature from a well-scoped issue. High-risk **production operations** (credential rotation, live outage handling, SSO configuration) should remain **human-led** with established operational procedures and guardrails.

**Tips and Tricks:**  
- Assign coding agent tasks like **bug fixes, UI updates, test improvements, docs, and tech-debt cleanup** with clear acceptance criteria.  
- Keep critical operations (prod incidents, auth, PII) under **manual control**, using Copilot at most for **small, reviewable code edits**.  
- Ensure there’s always a **testable path** (unit/integration tests) that validates the agent’s changes before merge.

> [!IMPORTANT]  
> If a scenario mentions **production incidents, credentials, or identity/security settings**, that’s a signal *not* to use coding agent as the primary actor those remain **human-owned** tasks.

**Correct and Wrong:**  
The correct scenario is the only one that keeps work inside a **safe PR workflow** with **clear acceptance criteria** and room for review. The other options all describe **high-risk, production or security-admin tasks** that GitHub explicitly warns against delegating to coding agent.

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[Piloting GitHub Copilot coding agent in your organization](https://docs.github.com/en/copilot/tutorials/coding-agent/pilot-coding-agent) (GitHub Docs)  


**Question:** [251]  
Which task is **best suited** for GitHub Copilot **coding agent** rather than being handled entirely by a human developer?  

**Options:**  
A. Designing a new cross-team architecture that spans several organizations and requires months of stakeholder alignment  
B. Leading an incident call to triage an active production outage and manually applying hotfixes in production  
C. **Implementing a backlog item to add pagination to an existing list view, updating the API, UI, and tests, and opening a PR for review**  
D. Running a brown-bag training session to teach new hires how the legacy monolith works in detail  

**Correct Answer(s):** C  

**Explanation:**  
GitHub positions Copilot coding agent for **incremental, code-centric tasks** such as implementing modest new features, fixing bugs, improving test coverage, updating documentation, and addressing technical debt, all within a **branch + tests + PR** workflow. Complex, broad, multi-month architecture decisions, live incident response, or primarily human communication/teaching work are all better suited to humans, not the coding agent.  

**Tips and Tricks:**  
- Think “**incremental feature or bugfix with tests and a PR**” as the agent’s sweet spot.  
- Keep **mission-critical, strategic, or strongly human-centred work** (architecture, training, incident command) human-owned.  
- Use the agent to clear **backlog items** that are well-scoped but time-consuming.  

> [!IMPORTANT]  
> If a task looks like a **normal, testable backlog item** that results in a PR, it’s a strong candidate for **Copilot coding agent**. If it looks like **strategy, incident management, or training**, keep it human-led.  

**Correct and Wrong:**  
Option C is correct because it describes an incremental feature with clear scope and tests that fits the “task → branch → tests → PR” pattern GitHub recommends for coding agent. The other options involve either high-risk decisions (architecture, incidents) or inherently human work (training), which GitHub describes as work you generally **do not** delegate to the agent.  

**Source:**  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[GitHub Copilot coding agent 101: Getting started with agentic workflows on GitHub](https://github.blog/ai-and-ml/github-copilot/github-copilot-coding-agent-101-getting-started-with-agentic-workflows-on-github/) (GitHub Blog)  


**Question:** [252]  
How does **GitHub Copilot coding agent** execute builds and tests for a task it’s working on?  

**Options:**  
A. It runs directly in your IDE, reusing your local tools and terminal session, and never uses GitHub Actions  
B. It runs only on GitHub Enterprise Server (GHES), inside runners that you manage entirely on-premises  
C. **It uses an ephemeral development environment backed by GitHub Actions runners, where it can clone the repo, make changes, and run tests and linters before updating a PR**  
D. It edits files in your default branch on GitHub.com but cannot run any builds, tests, or other commands  

**Correct Answer(s):** C  

**Explanation:**  
While working on a task, Copilot coding agent has access to its own **ephemeral development environment powered by GitHub Actions**. In that environment, it can **explore your code, make changes, build/compile, and run tests and linters**, then push commits to a branch and open or update a pull request. You can customize this environment (for example, pre-install tools or use larger or ARC-managed runners) via a `copilot-setup-steps.yml` workflow in your repository.  

**Tips and Tricks:**  
- Associate **“ephemeral dev environment + GitHub Actions runners + branch + PR”** with coding agent.  
- Use `copilot-setup-steps.yml` to make builds/tests **fast and reliable** for the agent.  
- Remember: coding agent does **not** run purely in your IDE and does **not** bypass branch protections.  

> [!IMPORTANT]  
> For Copilot coding agent questions, phrases like **“ephemeral development environment”** or **“powered by GitHub Actions”** plus **tests/linters + PR** are strong signals you’re looking at the **coding agent execution model**.  

**Correct and Wrong:**  
Option C is correct because it matches the documented architecture: an ephemeral GitHub Actions–powered environment used to edit code, run tools, and drive PRs. Option A wrongly moves execution into the IDE only, option B incorrectly claims GHES-only, and option D denies the ability to run tests/linters, all contradicting GitHub’s docs.  

**Source:**  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[Customizing the development environment for GitHub Copilot coding agent](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/customize-the-agent-environment) (GitHub Docs)  
[Copilot coding agent now supports self-hosted runners](https://github.blog/changelog/2025-10-28-copilot-coding-agent-now-supports-self-hosted-runners/) (GitHub Blog)  



**Question:** [253]  
Which statement correctly describes **who can use GitHub Copilot coding agent**?  

**Options:**  
A. Coding agent is available only with Copilot Enterprise; Pro, Pro+, Business, and Free users cannot use it  
B. Coding agent is available on **all** Copilot plans, including Copilot Free  
C. **Coding agent is available with Copilot Pro, Copilot Pro+, Copilot Business, and Copilot Enterprise**  
D. Coding agent is available only with Copilot Business and Enterprise, and not with any individual plans  

**Correct Answer(s):** C  

**Explanation:**  
GitHub’s “Who can use this feature?” sections for coding agent state that **Copilot coding agent is available with Copilot Pro, Copilot Pro+, Copilot Business, and Copilot Enterprise**. Recent GitHub blog updates about the agents panel also describe coding agent as available for **all paid Copilot plans**, which aligns with these four plan types and excludes Copilot Free.  

**Tips and Tricks:**  
- Memorize the set: **Pro, Pro+, Business, Enterprise** → coding agent is available; **Free** → no coding agent.  
- Any answer that claims “Enterprise only” or “Business + Enterprise only” is **too narrow**.  
- Any answer that includes **Free** for coding-agent availability is **too broad**.  

> [!IMPORTANT]  
> Exam shorthand: **“All paid Copilot plans” = Pro, Pro+, Business, Enterprise → coding agent yes; Free → coding agent no.**  

**Correct and Wrong:**  
Option C is correct because it matches the exact list in the GitHub Docs plan matrix for Copilot coding agent. Options A and D ignore Pro/Pro+ individual plans; option B incorrectly includes Copilot Free, which the docs do not list as supporting the coding agent.  

**Source:**  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[Managing access to GitHub Copilot coding agent](https://docs.github.com/en/enterprise-cloud%40latest/copilot/concepts/agents/coding-agent/coding-agent-for-business-and-enterprise) (GitHub Docs)  
[Agents panel: Launch Copilot coding agent tasks anywhere on GitHub](https://github.blog/news-insights/product-news/agents-panel-launch-copilot-coding-agent-tasks-anywhere-on-github/) (GitHub Blog)  
[Management and customization considerations with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/github-copilot-management-and-customizations/) (Microsoft Learn)  



**Question:** [254]  
Your team notices that Copilot coding agent spends a lot of time **figuring out how to install dependencies**, and sometimes fails to run tests because private packages aren’t available. How should you improve the **speed and reliability** of the agent’s runs?  

**Options:**  
A. Ask each developer to run all installs locally and push `node_modules` or `vendor` directories into the repo so the agent doesn’t need to install anything  
B. Put your usual setup commands into a personal shell script in your home directory; the agent will automatically detect and run it  
C. **Create a `.github/workflows/copilot-setup-steps.yml` workflow that pre-installs required tools and dependencies in the agent’s environment**  
D. Disable tests in the repository’s CI so Copilot never has to run them and will always “succeed” quickly  

**Correct Answer(s):** C  

**Explanation:**  
GitHub recommends using a special workflow file, **`.github/workflows/copilot-setup-steps.yml`**, containing a single `copilot-setup-steps` job, to **preinstall tools and dependencies** in Copilot’s **ephemeral GitHub Actions environment** before the agent starts working. This makes builds and tests more **deterministic, faster, and more reliable**, especially when you need to fetch private or custom dependencies that Copilot can’t easily infer or install by trial and error.  

**Tips and Tricks:**  
- Use `copilot-setup-steps.yml` to install **runtimes, package managers, and project dependencies** up front.  
- Keep the setup **minimal but sufficient**—only what’s needed for builds/tests/linters.  
- Don’t “optimize” by disabling tests; tests are key guardrails for AI-generated PRs.  

> [!IMPORTANT]  
> When you see “**make the coding agent faster or more reliable in your repo**,” the exam-safe pattern is: **configure `copilot-setup-steps.yml` to pre-install tools and dependencies in the agent’s GitHub Actions environment**.  

**Correct and Wrong:**  
Option C is correct because it uses the documented mechanism (`copilot-setup-steps.yml`) to preconfigure the agent’s environment. Option A bloats the repo and doesn’t help the agent’s environment, option B assumes local scripts are auto-used (they aren’t), and option D undermines test guardrails instead of fixing the underlying environment problem.  

**Source:**  
[Customizing the development environment for GitHub Copilot coding agent](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/customize-the-agent-environment) (GitHub Docs)  
[Onboarding your AI peer programmer: Setting up GitHub Copilot coding agent for success](https://github.blog/ai-and-ml/github-copilot/onboarding-your-ai-peer-programmer-setting-up-github-copilot-coding-agent-for-success/) (GitHub Blog)  
[Copilot coding agent now supports self-hosted runners](https://github.blog/changelog/2025-10-28-copilot-coding-agent-now-supports-self-hosted-runners/) (GitHub Blog)  



**Question:** [255]  
Which scenario best exemplifies a task that **should not** be delegated to GitHub Copilot coding agent, according to GitHub’s guidance?  

**Options:**  
A. Cleaning up duplicated helper functions in a utility module, with good test coverage in place  
B. Adding accessibility improvements (ARIA attributes) to a few UI components and updating snapshots  
C. Writing missing unit tests for a well-understood service with clear acceptance criteria  
D. **Coordinating and implementing fixes for an ongoing production incident involving leaked access tokens and repeated authentication failures**  

**Correct Answer(s):** D  

**Explanation:**  
GitHub’s best practices list **“sensitive and critical tasks”**—including **production-critical issues, security tasks, PII/authentication repercussions, and incident response**—as work that you should **handle yourself** rather than assigning to Copilot coding agent. Routine refactors, accessibility tweaks, and test improvements are explicitly called out as appropriate tasks for the agent because they are **well-scoped, testable, and non-critical**.  

**Tips and Tricks:**  
- Treat **production incidents, auth/PII issues, and security-sensitive changes** as **off-limits** for coding agent.  
- Prefer the agent for **non-critical, well-scoped, PR-driven tasks** like refactors, tests, docs, and UI fixes.  
- If a stem mentions “**incident response**”, “**leaked tokens**”, or “**auth failures in production**”, it’s almost always a **don’t-use-the-agent** signal.  

> [!IMPORTANT]  
> Coding agent is for **safe, reviewable, non-critical code changes**. **Active incidents, security/PII/auth problems, and production-critical decisions** should remain human-led, with Copilot only assisting around the edges if at all.  

**Correct and Wrong:**  
Option D is correct because it describes an **ongoing production incident** involving leaked tokens and authentication failures—exactly the sort of sensitive, production-critical work GitHub says you should not delegate to the coding agent. Options A, B, and C are all examples of scoped, testable engineering work that GitHub highlights as good candidates for the agent (refactors, accessibility improvements, and tests).  

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/tutorials/coding-agent/get-the-best-results) (GitHub Docs)  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[Responsible use of GitHub Copilot coding agent on GitHub.com](https://docs.github.com/en/enterprise-cloud%40latest/copilot/responsible-use/copilot-coding-agent) (GitHub Docs)  



**Question:** [256]  
You want to **standardize error handling** in a service by:  
- Updating a shared `handleError` helper in one file  
- Adding a single new `try/catch` around one call site in another file  
- Reviewing a **small, focused diff** before committing  

You **do not** need Copilot to run tests, call tools, or discover additional files on its own. Which Copilot capability is the **best fit**?  

**Options:**  
A. Use Copilot coding agent from GitHub.com to autonomously refactor the entire service and open a PR  
B. **Use Copilot Edits in Edit mode on just the two relevant files, then review and apply the proposed diff**  
C. Use agent mode in your IDE so Copilot can freely edit any file in the workspace and run terminal commands  
D. Ask Copilot Chat in Ask mode for code snippets and paste them into files manually without any diff view  

**Correct Answer(s):** B  

**Explanation:**  
**Copilot Edits – Edit mode** is designed for **quick, specific updates to a defined set of files**, where you pick which files Copilot may change, submit a prompt, and then **review per-file diffs before applying or discarding changes**. GitHub documentation and blog guidance recommend Edit mode when you want **granular control** and a tight feedback loop, while **agent mode** (either in IDE or coding agent on GitHub.com) is better for **broader, multi-step workflows** that may touch multiple files and run tools autonomously.  

**Tips and Tricks:**  
- Use **Edit mode** when you can **name the files and change** you want and you care about a small, reviewable diff.  
- Use **agent mode** when the task is **larger, multi-step, and may need tools/commands**.  
- Ask mode is great for **explanations and snippets**, not for managed multi-file diffs.  

> [!IMPORTANT]  
> Think **“scope and control”**:  
> - **Edit mode** → *targeted, file-scoped changes with explicit diffs*  
> - **Agent mode / coding agent** → *larger, multi-step workflows across files and tools*  

**Correct and Wrong:**  
Option B is correct because it matches the documented Edit-mode use case: a **quick, specific update across a known set of files** with a clear diff review experience. Options A and C both give Copilot more autonomy than needed (full-service refactor or workspace-wide agent mode), and option D loses the integrated diff/review flow that Copilot Edits provides.  

**Source:**  
[GitHub Copilot features](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Asking GitHub Copilot questions in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[Copilot ask, edit, and agent modes: What they do and when to use them](https://github.blog/ai-and-ml/github-copilot/copilot-ask-edit-and-agent-modes-what-they-do-and-when-to-use-them/) (GitHub Blog)  
[GitHub Copilot Edits in Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-edits) (Microsoft Learn)  



**Question:** [257]  
A product manager opens a GitHub issue describing a **new API endpoint**. You want Copilot to:  

1. Read the issue and existing code  
2. Add the new route, handler, and tests across several files  
3. Run the project’s tests  
4. Open a **pull request** with a summary of what changed  

Which Copilot capability is designed for this **end-to-end, multi-step workflow**?

**Options:**  
A. Inline suggestions at the cursor to manually implement the endpoint and tests in one file at a time.  
B. Copilot Chat in a single IDE conversation to propose patches, then copy and apply them manually.  
C. **Copilot coding agent (Agent mode) acting from the issue**  
D. Repository-aware chat on GitHub.com to discuss the design without applying any code changes.  

**Correct Answer(s):** C  

**Explanation:**  
The **Copilot coding agent in Agent mode** is built to handle **multi-step workflows**: it can take context from an issue, modify multiple files, run commands like tests or linters in its environment, and then open a pull request summarizing the changes. Chat and inline suggestions help you write code, but they don’t own the full “issue → edits → tests → PR” lifecycle in the way the coding agent does.

**Tips and Tricks:**  
- Use **Agent mode** when you want Copilot to manage **edits, tests, and PR creation** from a GitHub issue.  
- Keep issues **narrow and well-scoped** with clear acceptance criteria to improve agent output.  
- Use Chat/inline when you prefer to **apply patches yourself** and keep Copilot as an assistant.  

> [!IMPORTANT]  
> When a question combines **reading an issue, editing multiple files, running tests, and opening a PR**, the intended answer is almost always **Copilot coding agent in Agent mode**.

**Correct and Wrong:**  
The correct option is the right answer because it matches the documented capability of the **coding agent** to pick up a task from an issue, make cross-file changes, run tests, and open a PR. The other options either limit Copilot to advisory roles (Chat/inline) or keep the interaction at discussion-only level without applying changes or creating a PR.

**Source:**  
[GitHub Copilot coding agent](https://docs.github.com/en/copilot/tutorials/coding-agent) (GitHub Docs)  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/using-github-copilot/coding-agent/best-practices-for-using-copilot-to-work-on-tasks) (GitHub Docs)  
[Responsible use of GitHub Copilot coding agent on GitHub.com](https://docs.github.com/en/enterprise-cloud@latest/copilot/responsible-use/copilot-coding-agent) (GitHub Docs)  


**Question:** [258]  
Which scenario is **most appropriate** for using the **Copilot coding agent**, rather than only using Copilot Chat inside your IDE?

**Options:**  
A. Asking “Why does this function fail?” and pasting a stack trace for Copilot Chat to explain in your IDE.  
B. **Implementing a backlog item that requires edits across multiple services, running tests, and opening a PR**  
C. Renaming a local variable in a single file, then manually committing the change.  
D. Generating a one-off code snippet for a small helper function you’ll paste into a file.  

**Correct Answer(s):** B  

**Explanation:**  
**Copilot coding agent** is designed for **complex, multi-step tasks** that span multiple files and may require running tests or other commands, then creating a PR. A backlog item that touches several services and includes tests and PR creation fits this pattern. Smaller, local tasks debug explanations, tiny refactors, or one-off snippets are faster and safer with Chat, Ask mode, or inline suggestions.

**Tips and Tricks:**  
- Use the coding agent for **cross-file or cross-service work** that includes edits, tests, and PRs.  
- Use Chat/Ask mode for **debugging and explanations** and inline suggestions for small local edits.  
- Match the tool to **task complexity**; over-using the agent for tiny changes adds overhead with no benefit.  

> [!IMPORTANT]  
> When a scenario mentions **multiple services or files, running tests, and opening a PR**, it’s a strong signal that **Copilot coding agent** not just Chat is the best fit.

**Correct and Wrong:**  
The correct option is the right answer because it describes exactly the kind of **multi-step, cross-service workflow** that GitHub positions the coding agent to perform end-to-end. The other options are small, localized tasks where Chat or inline suggestions are sufficient and the agent’s extra autonomy and orchestration are unnecessary.

**Source:**  
[GitHub Copilot features](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Asking GitHub Copilot questions in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[GitHub Copilot coding agent](https://docs.github.com/en/copilot/tutorials/coding-agent) (GitHub Docs)  


**Question:** [259]  
You want to delegate a task to the **Copilot coding agent**. Which instruction gives it the **most useful guidance**?

**Options:**  
A. “Fix everything that’s wrong in this repo and refactor as needed until there are no issues left.”  
B. **“From this issue, implement the `order-cancellation` endpoint end-to-end: update the API spec, add handler + routing, write integration tests, and open a PR when tests pass.”**  
C. “Refactor as you see fit; you decide what to change and where.”  
D. “Make the code better and faster in general, using your judgment.”  

**Correct Answer(s):** B  

**Explanation:**  
GitHub’s guidance for Copilot coding agent emphasizes **clear, well-scoped tasks with acceptance criteria**. Option B names a concrete feature (“`order-cancellation` endpoint”), lists the steps (spec, handler, routing, tests), and defines a completion condition (tests pass and a PR is opened). The other options are vague and unconstrained, making it hard for the agent to stay focused and for you to verify success.

**Tips and Tricks:**  
- Frame agent tasks as **bounded work items** (feature/endpoint/bug) with explicit steps.  
- Include **acceptance criteria** such as “tests passing,” “docs updated,” or “lint clean” as a stop condition.  
- If you wouldn’t accept an issue because it’s too vague, don’t hand that same wording to the agent.  

> [!IMPORTANT]  
> For Copilot coding agent, **tight scope + explicit acceptance criteria** is the safety net that keeps the agent’s changes focused and PRs reviewable.

**Correct and Wrong:**  
The correct option is the right answer because it gives the agent a **specific endpoint name, concrete implementation steps, and a clear done condition** that aligns with GitHub’s best practices for assigning tasks to the coding agent. The other options use open-ended language like “fix everything” or “make it better,” which invites over-broad changes and goes against the documented guidance.

**Source:**  
[Best practices for using GitHub Copilot to work on tasks](https://docs.github.com/en/copilot/using-github-copilot/coding-agent/best-practices-for-using-copilot-to-work-on-tasks) (GitHub Docs)  
[Concepts for GitHub Copilot agents](https://docs.github.com/en/copilot/concepts/agents/concepts-for-github-copilot-agents) (GitHub Docs)  
[GitHub Copilot coding agent](https://docs.github.com/en/copilot/tutorials/coding-agent) (GitHub Docs)  

**Question:** [260]  
After the **Copilot coding agent** completes a task and opens a pull request, what is the **team’s responsibility**?

**Options:**  
A. None, the agent’s PR can be merged without human review, because all tests are implicitly guaranteed to pass.  
B. Only check that the PR description is formatted nicely before allowing automatic merge rules to apply.  
C. **Review the changes, run or verify tests, and ensure the PR meets security and quality standards before merging**  
D. Re-run the agent until it merges the PR on its own without any human approval.  

**Correct Answer(s):** C  

**Explanation:**  
GitHub’s documentation makes it clear that after Copilot coding agent opens a pull request, the team must still **review the changes, enforce branch protections, and verify tests and checks** before merging. Agent-created PRs behave like any other PRs and remain subject to your normal security, quality, and compliance processes.

**Tips and Tricks:**  
- Treat **agent-created PRs exactly like human-created PRs**: review diffs, verify tests, and check security-impacting changes.  
- Remember that **branch protections and required checks still apply** to branches created by Copilot coding agent.  
- Use Copilot Chat or code review helpers to explain or refine changes, but do not skip human approval.  

> [!IMPORTANT]  
> Copilot coding agent can open PRs, but it does **not** change your accountability model teams remain responsible for reviewing, testing, and deciding what ships.

**Correct and Wrong:**  
The correct option is the right answer because it aligns with GitHub’s guidance that teams must **review, test, and enforce quality/security standards** on any PR created by Copilot coding agent. The other options incorrectly suggest skipping review, doing only superficial checks, or expecting the agent to merge PRs autonomously, all of which conflict with documented branch protection and review practices.

**Source:**  
[Reviewing a pull request created by GitHub Copilot](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/review-copilot-prs) (GitHub Docs)  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/coding-agent/coding-agent) (GitHub Docs)  
[Best practices for using GitHub Copilot](https://docs.github.com/en/copilot/get-started/best-practices) (GitHub Docs)  
[GitHub Copilot: Meet the new coding agent](https://github.blog/news-insights/product-news/github-copilot-meet-the-new-coding-agent/) (GitHub Blog)  

**Question:** [261]  
Where are Copilot prompts and allowed context processed?

**Options:**  
A. Only on the local IDE; nothing leaves the machine, and no data is sent to any GitHub or model service.  
B. **In the Copilot cloud service, which relays requests to the selected AI model per GitHub’s data pipeline**  
C. On your company’s GitHub Enterprise Server only, with no Copilot cloud service involved.  
D. Inside your CI runners, where prompts are stored and processed as part of builds.  

**Correct Answer(s):** B  

**Explanation:**  
GitHub describes a data pipeline in which **prompts and their allowed context** are sent from the client (IDE or GitHub.com) to the **GitHub Copilot service**, which then routes the request to the configured AI model to generate suggestions. Content exclusion and enterprise/org policies determine what code and metadata can be included as context in those requests.

**Tips and Tricks:**  
- Remember that Copilot is a **cloud-backed service**: prompts do leave the IDE and go to GitHub plus an AI model.  
- Use **content exclusion** to control which repositories and paths can be used as context.  
- Combine content exclusion with **code referencing and duplication filters** to manage what Copilot is allowed to suggest.  

> [!IMPORTANT]  
> For “where is data processed?” questions, the key is: **prompts go to the Copilot cloud service, then to an AI model**, shaped by your content-exclusion and policy settings not only on your local machine or CI.

**Correct and Wrong:**  
The correct option is the right answer because it matches GitHub’s description that **Copilot prompts are processed by a cloud Copilot service which relays them to an AI model**, constrained by enterprise policies. The other options incorrectly imply purely local processing, GHES-only processing without the Copilot service, or CI-only handling, none of which reflect the documented architecture.

**Source:**  
[How to responsibly adopt GitHub Copilot with the GitHub Copilot Trust Center](https://github.blog/news-insights/policy-news-and-insights/how-to-responsibly-adopt-github-copilot-with-the-github-copilot-trust-center/) (GitHub Blog)  
[Content exclusion for GitHub Copilot](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Excluding content from GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[GitHub Copilot code referencing](https://docs.github.com/en/copilot/concepts/completions/code-referencing) (GitHub Docs)  

**Question:** [262]  
Does GitHub Copilot train on your **private code**?

**Options:**  
A. Yes, always your private code is automatically used to train Copilot models in all plans.  
B. Yes, unless product telemetry is disabled at the enterprise or org level.  
C. **No, private code is not used to train Copilot models**  
D. Only for Enterprise customers, where private code is always used for training unless they opt out.  

**Correct Answer(s):** C  

**Explanation:**  
GitHub’s trust and policy materials state that **private code from Copilot for Business and similar enterprise scenarios is not used to train shared Copilot models by default**, and that model training is distinct from telemetry or product-improvement metrics. Custom model training relies on separate, explicit flows rather than automatically including all private repositories.

**Tips and Tricks:**  
- Separate **telemetry/product analytics** from **model training** in your mental model.  
- For enterprise and business plans, answers claiming “always trains on your private code” are usually wrong.  
- Use the **Copilot Trust Center** and policy docs to back up statements during audits and regulatory reviews.  

> [!IMPORTANT]  
> Key exam message: **Copilot does not use your private code to train shared models by default**; training on private repos is a separate, explicit configuration choice.

**Correct and Wrong:**  
The correct option is the right answer because it is consistent with GitHub’s published statements that **private code is not automatically used to train Copilot’s shared AI models**, especially in business and enterprise plans. The other options incorrectly claim that private code is always used, tied directly to telemetry toggles, or specifically and unavoidably used for enterprise training, which contradicts the documented behavior.

**Source:**  
[Managing GitHub Copilot policies as an individual subscriber](https://docs.github.com/en/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)  
[How to responsibly adopt GitHub Copilot with the GitHub Copilot Trust Center](https://github.blog/news-insights/policy-news-and-insights/how-to-responsibly-adopt-github-copilot-with-the-github-copilot-trust-center/) (GitHub Blog)  
[Creating a custom model for GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/use-ai-models/create-a-custom-model) (GitHub Docs)  

**Question:** [263]  
What does **Content exclusion** actually do?

**Options:**  
A. Censors outputs that are similar to excluded files, but still allows those files to be used as input context.  
B. **Prevents specified repositories/paths/file types/patterns from being used as input context**  
C. Disables Copilot completely for the repository or organization.  
D. Removes excluded files from Git history so Copilot cannot see prior versions.  

**Correct Answer(s):** B  

**Explanation:**  
GitHub’s **content exclusion** feature lets admins define **repositories, directories, and patterns that Copilot is not allowed to use as input context**. It limits what Copilot can read when forming suggestions but does not delete code, disable Copilot entirely, or directly govern output similarity that is handled by **code referencing** and duplication filters.

**Tips and Tricks:**  
- Think of content exclusion as an **input fence** that Copilot cannot look beyond.  
- Start by excluding **secret-bearing, regulated, or highly sensitive paths** from Copilot context.  
- Use **code referencing and duplication detection** alongside content exclusion to cover the output side.  

> [!IMPORTANT]  
> Exam shorthand: **Content exclusion = input control**, **code referencing/duplication filters = output control**; you typically need all of them for a complete risk story.

**Correct and Wrong:**  
The correct option is the right answer because it matches the docs: content exclusion **prevents selected repositories and paths from being used as context** by Copilot. The other options misinterpret it as output censorship, a global Copilot kill switch, or history rewriting, none of which describes how the feature actually works.

**Source:**  
[Content exclusion for GitHub Copilot](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Excluding content from GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Configure and audit content exclusion](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion) (GitHub Docs)  
[GitHub Copilot code referencing](https://docs.github.com/en/copilot/concepts/completions/code-referencing) (GitHub Docs)  

**Question:** [264]  
How does Copilot handle suggestions that **exactly match** long segments of public code?

**Options:**  
A. Always allows long exact matches from public code, but adds a warning about possible licensing issues.  
B. Allows or blocks long exact matches purely based on the original repository’s license.  
C. **Uses duplication-detection filters to block long exact matches (≈150+ characters)**  
D. Publishes any long exact matches it generates directly back to public GitHub repositories.  

**Correct Answer(s):** C  

**Explanation:**  
When “block suggestions matching public code” is enabled or enforced, Copilot uses **duplication-detection filters** that compare each suggestion (plus its surrounding context of roughly 150 characters) against public GitHub code. If the system detects a long exact or near-exact match above this threshold, it suppresses the suggestion, independent of license.

**Tips and Tricks:**  
- Remember the **“about 150 characters”** figure as the duplication-detection threshold.  
- Blocking is driven by **length and similarity**, not just by license.  
- Pair duplication detection with **code referencing** so shorter, allowed matches can still be attributed when appropriate.  

> [!IMPORTANT]  
> Memory hook: **“≈150 characters + exact or near-exact match to public code = blocked suggestion”** when matching-public-code blocking is enabled.

**Correct and Wrong:**  
The correct option is the right answer because it captures that Copilot uses **duplication-detection filters with around a 150-character context window** to block long exact matches to public code. The other options either ignore the filter, depend solely on licensing, or describe behavior such as auto-publishing code that is not supported by the documentation.

**Source:**  
[Managing GitHub Copilot policies as an individual subscriber](https://docs.github.com/en/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)  
[Managing Copilot policies (Enterprise Cloud)](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)  
[Getting code suggestions in your IDE with GitHub Copilot](https://docs.github.com/en/copilot/using-github-copilot/getting-code-suggestions-in-your-ide-with-github-copilot) (GitHub Docs)  
[Finding public code that matches GitHub Copilot suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  


**Question:** [265]  
Which statement best describes **Copilot usage telemetry/metrics**?

**Options:**  
A. Copilot collects no usage data  
B. **Telemetry aggregates activity and feature usage (e.g., suggestions, chat, agents), not a dump of your source code**  
C. Telemetry always includes raw file contents  
D. Telemetry is only available to Enterprise customers  

**Correct Answer(s):** B  

**Explanation:**  
Copilot usage telemetry underpins the **usage metrics** dashboards and APIs, which report structured events and fields about how Copilot is used (for example, suggestions, chat, agents) across different surfaces. These metrics are based on aggregated activity and feature usage, not raw copies of your source code, and they are separate from any model-training data flows.

**Tips and Tricks:**  
- Use usage metrics to track **adoption and engagement** by feature and surface (IDE, GitHub.com, CLI, Mobile).  
- Keep a clear mental separation: **telemetry/metrics ≠ model training**.  
- For detail-heavy questions, refer back to the **metrics data properties** and retention documentation.  

> [!IMPORTANT]  
> Copilot usage metrics capture **how** features are used (activity and counts), not full dumps of your repositories 
supports **governance and ROI**, not code reconstruction.

**Correct and Wrong:**  
The correct option is the right answer because it matches GitHub’s description of usage metrics as **aggregated activity and feature-usage signals**, not raw source files. The other options either deny that telemetry exists, incorrectly claim that telemetry always includes file contents, or limit metrics to Enterprise customers only, none of which align with the metrics documentation.

**Source:**  
[GitHub Copilot usage metrics](https://docs.github.com/en/copilot/reference/copilot-usage-metrics) (GitHub Docs)  
[Metrics data properties for GitHub Copilot usage metrics](https://docs.github.com/en/copilot/reference/metrics-data) (GitHub Docs)  
[Get started with GitHub Copilot](https://docs.github.com/en/enterprise-cloud/latest/copilot/get-started) (GitHub Docs)  

**Question:** [266]  
Do **content exclusion** rules apply across all supported Copilot **surfaces** (IDE, GitHub.com, CLI, Mobile)?

**Options:**  
A. No, only in VS Code  
B. Only on GitHub.com  
C. Only in JetBrains IDEs  
D. **Yes, exclusion defines the input context boundary for Copilot regardless of surface**  

**Correct Answer(s):** D  

**Explanation:**  
Content exclusion is evaluated in the **Copilot service**, not inside a single IDE, so the same exclusion rules constrain which repositories, paths, and patterns can be used as input context across supported Copilot surfaces. This makes exclusion a cross-surface input boundary, rather than a client-specific toggle.

**Tips and Tricks:**  
- Treat content exclusion as a **server-side “do not read” list** for Copilot, shared across IDEs and GitHub.com.  
- Start with **secret-bearing or highly sensitive areas** when defining exclusions, then refine over time.  
- Combine exclusion with **code referencing** to also manage what Copilot is allowed to suggest.  

> [!IMPORTANT]  
> Content exclusion is about **inputs across surfaces** it limits what Copilot can **see**, while code referencing governs what it can **suggest** when matching public code.

**Correct and Wrong:**  
The correct option is the right answer because it reflects that content exclusion is enforced centrally and sets an input boundary regardless of which Copilot surface you use. The distractors incorrectly scope exclusion to a single client (VS Code, GitHub.com, or JetBrains only), which doesn’t match the service-level behavior described in the docs.

**Source:**  
[Exclude content from GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-github-copilot) (GitHub Docs)  
[Content exclusion is now generally available in IDEs](https://github.blog/changelog/2024-11-12-content-exclusion-ga/) (GitHub Blog)  
[GitHub Copilot features](https://docs.github.com/en/enterprise-cloud/latest/copilot/get-started/features) (GitHub Docs)  

**Question:** [267]  
At which **scopes** can you configure **code referencing / matching public code**?

**Options:**  
A. Only at the repo level  
B. Only at the enterprise level  
C. **At the individual account level and via org/enterprise policies**  
D. Only in IDE settings  

**Correct Answer(s):** C  

**Explanation:**  
GitHub lets **individual users** control how suggestions that match public code are handled in their personal Copilot settings, and also allows **organizations and enterprises** to set defaults or enforce stricter policies at higher scopes. Enterprise-enforced policies override user-level preferences, but configuration exists at all three levels.

**Tips and Tricks:**  
- Memorize the hierarchy: **Enterprise → Organization → User**; enforcement at the top wins.  
- Use **Allow + show references** when you want to permit matches but still surface links for due diligence.  
- Pair code referencing with **duplication detection** to also block long exact matches to public code.  

> [!IMPORTANT]  
> Code referencing is a **multi-scope control**: users can set preferences, but org and enterprise policies can enforce stricter rules that everyone must follow.

**Correct and Wrong:**  
The correct option is the right answer because it aligns with the docs that describe settings for matching public code at both the **individual** level and via **org/enterprise policies**. The other options incorrectly restrict configuration to a single level (repo-only, enterprise-only, or IDE-only) and ignore the documented policy hierarchy.

**Source:**  
[Find matching public code in suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  
[Managing GitHub Copilot in your enterprise](https://docs.github.com/en/enterprise-cloud/latest/copilot/how-tos/administer-copilot/manage-for-enterprise) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/enterprise-cloud/latest/copilot/get-started/plans) (GitHub Docs)  

**Question:** [268]  
Is GitHub Copilot supported on **GitHub Enterprise Server (GHES)**?

**Options:**  
A. Yes, Copilot runs entirely on-prem  
B. Yes, but only chat  
C. **No, Copilot requires the cloud service; GHES is not supported**  
D. Yes, with a self-hosted model  

**Correct Answer(s):** C  

**Explanation:**  
Copilot plans and setup are documented for **GitHub.com and GitHub Enterprise Cloud**, and Copilot’s inference and policy services are cloud-hosted. There is no supported deployment where Copilot runs fully on-prem on GHES without connecting to GitHub’s Copilot cloud service, so a GHES-only environment does not support Copilot.

**Tips and Tricks:**  
- “Air-gapped GHES only, no outbound internet” is a strong signal that **Copilot is not supported**.  
- References to **Enterprise Cloud** or GHE.com in plan tables are hints that Copilot **is** available.  
- Ignore distractors that mention uploading a “self-hosted Copilot model” to GHES this isn’t a documented product capability.  

> [!IMPORTANT]  
> Copilot is a **cloud-hosted service** attached to GitHub.com / GHEC accounts; GHES alone cannot host or replace Copilot.

**Correct and Wrong:**  
The correct option is the right answer because it reflects the documented availability of Copilot as a cloud service for GitHub.com and Enterprise Cloud, not GHES-only environments. The other options incorrectly suggest a fully on-prem Copilot, partial support on GHES, or a self-hosted model option that does not exist in the official documentation.

**Source:**  
[What is GitHub Copilot?](https://docs.github.com/en/enterprise-cloud/latest/copilot/get-started/what-is-github-copilot) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/enterprise-cloud/latest/copilot/get-started/plans) (GitHub Docs)  
[Setting up GitHub Copilot](https://docs.github.com/en/enterprise-cloud/latest/copilot/how-tos/set-up) (GitHub Docs)  

**Question:** [269]  
Which statement about **repository-aware Copilot Chat on GitHub.com** is accurate?

**Options:**  
A. Available to all plans by default  
B. Requires GHES  
C. **It’s an Enterprise capability that lets chat reference repository files/docs on GitHub.com**  
D. It runs offline in the IDE only  

**Correct Answer(s):** C  

**Explanation:**  
With **Copilot Enterprise**, Copilot Chat on GitHub.com becomes **repository-aware**, meaning it can use your organization’s repositories and associated documentation as context when answering questions in the browser. This is positioned as an Enterprise capability and respects repo permissions and governance controls.

**Tips and Tricks:**  
- Map “**Chat in GitHub.com that understands your code/docs**” directly to **Copilot Enterprise**.  
- Remember that repository-aware chat still obeys **permissions, content exclusion, and policies**.  
- Don’t confuse general chat availability (across many plans) with Enterprise-only repository-aware features.  

> [!IMPORTANT]  
> Repository-aware chat on GitHub.com is a **Copilot Enterprise** feature: it brings your repos and docs into chat but does not bypass governance.

**Correct and Wrong:**  
The correct option is the right answer because it matches GitHub’s description of **repository-aware chat** as an Enterprise capability that references repository files and docs on GitHub.com. The other options either overstate availability to all plans, wrongly tie the feature to GHES, or mischaracterize it as an offline IDE-only capability.

**Source:**  
[GitHub Copilot Enterprise is now generally available](https://github.blog/changelog/2024-02-27-copilot-enterprise-is-now-generally-available/) (GitHub Blog)  
[Asking GitHub Copilot questions in GitHub](https://docs.github.com/en/enterprise-cloud/latest/copilot/how-tos/chat-with-copilot/chat-in-github) (GitHub Docs)  
[Introduction to GitHub Copilot Enterprise](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/) (Microsoft Learn)  

**Question:** [270]  
If an **enterprise policy** enforces “Block matching public code,” can an organization **override** it?

**Options:**  
A. Yes, at the org level an organization owner can always change “Block matching public code” to “Allow” even if the enterprise enforces it.  
B. Yes, at the repo level repo admins can override an enforced enterprise policy for their specific repositories.  
C. **No, enterprise-enforced policies take precedence**  
D. Only for public repositories orgs can override enforcement for private repos but not public ones.  

**Correct Answer(s):** C  

**Explanation:**  
Copilot policies follow a **hierarchy**: enterprise → organization → repository/user. When an enterprise owner sets a policy like “Block matching public code” to **enforced**, lower levels must comply with that posture and can only make it stricter, not weaker. Organizations and repositories cannot change an enforced enterprise setting from “block” to “allow.”

**Tips and Tricks:**  
- Read stems carefully: **“enforced” = no override**, **“default” = lower scopes may tighten**.  
- Remember that **policy strength can only increase** as you go down the hierarchy, not decrease.  
- For exams, treat “enterprise-enforced” as a hard ceiling that orgs and repos cannot weaken.  

> [!IMPORTANT]  
> Policy hierarchy: **Enterprise-enforced Copilot policies always win** orgs and repos can only be stricter, never more permissive, than an enforced enterprise rule.

**Correct and Wrong:**  
The correct option is the right answer because it reflects GitHub’s documented policy model: once an enterprise enforces “Block matching public code,” organizations and repositories must honor it and cannot switch to “Allow.” The other options wrongly suggest that orgs or repos can override enforcement or that there is a special exception for public vs. private repos, none of which are supported by the enterprise policy behavior.

**Source:**  
[Manage enterprise policies for Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Manage organization policies for Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-organizations/manage-organization-policies) (GitHub Docs)  
[Find matching public code in suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  