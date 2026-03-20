# Raw Practice Test 03 - Answer Sheet

201. You notice Copilot suggests code that logs full JWT tokens for debugging. What is the most responsible action to take?  
A. Accept the suggestion as-is because logs are internal and will not leave the organization.  
B. **Reject or modify the suggestion to avoid logging secrets and use masked or structured logging instead**  
C. Accept it and add a comment that the logging is temporary for debugging.  
D. Turn off all logging in the service to avoid any risk of exposure.  
**Correct Answer(s):** B  

202. Copilot proposes a function that closely resembles a well-known open-source project and includes a copied license header. What should you do?  
A. **Review the license and either attribute properly or replace the code with an original implementation**  
B. Remove the license header and use the code as-is to avoid attribution.  
C. Assume Copilot has already handled licensing and no further action is needed.  
D. Always reject any suggestion that mentions a license, regardless of context.  
**Correct Answer(s):** A  

203. Which scenario best demonstrates **fair and inclusive** use of GitHub Copilot?  
A. Use Copilot to generate code comments or messages that stereotype or generalize about certain user groups and commit them without edits.  
B. Ignore Copilot suggestions that might disadvantage accessibility users instead of correcting them or updating guidelines.  
C. **Using Copilot to propose error messages and UI text, then reviewing them to remove biased or exclusionary language**  
D. Allow Copilot to generate all user-facing copy and accept it without any human review or accessibility checks.  
**Correct Answer(s):** C  

204. Your team wants to adopt Copilot but is worried about **over-reliance** on AI. What is the best mitigation?  
A. Ban Copilot completely so the team never interacts with AI-assisted code.  
B. Use Copilot only for non-critical artifacts like comments, but keep no explicit guidelines or review requirements.  
C. **Define team guidelines: Copilot suggestions must be reviewed, tested, and never treated as authoritative**  
D. Allow Copilot to auto-merge pull requests when tests pass, reducing the need for human review.  
**Correct Answer(s):** C  

205. Which practice best aligns with **responsible evaluation** of Copilot in your organization?  
A. Measuring success only by how many lines of Copilot-generated code are checked in  
B. **Tracking where Copilot saves time while also monitoring bug rates, security findings, and developer feedback**  
C. Enabling Copilot across all repos without defining metrics or collecting feedback  
D. Treating Copilot seat counts and usage alone as proof of productivity improvement  
**Correct Answer(s):** B  

206. How do **Copilot Spaces** primarily improve Copilot Chat on GitHub?  
A. Running Copilot’s language models entirely on your local hardware instead of the cloud  
B. **Organizing curated context (files, repositories, pull requests, and issues) so Copilot’s responses are grounded in your project**  
C. Automatically merging pull requests that Copilot reviews and approves  
D. Ignoring organization and enterprise policies so Copilot can see all code in the org  
**Correct Answer(s):** B  

207. Who can use **Copilot Spaces**, and where are they available?  
A. Only GitHub Enterprise owners, and only on GitHub Enterprise Server (GHES)  
B. Only Copilot Enterprise subscribers, and only when using Visual Studio Code  
C. **Any user with a Copilot subscription, on GitHub.com, with IDE integration available for some workflows**  
D. Only organization owners, and only inside GitHub Desktop  
**Correct Answer(s):** C  

208. Which scenario is the **best fit** for creating a **Copilot Space** instead of just using one-off Copilot Chat?  
A. Looking up the meaning of a one-off error message that you will not need again  
B. **Onboarding a new team to a complex service by sharing curated docs, repositories, and example pull requests they’ll reuse over time**  
C. Running a single ad-hoc SQL query against a non-critical test database  
D. Making a quick, temporary change to a single local function in a small script  
**Correct Answer(s):** B  

209. How do **Copilot Spaces** interact with **content exclusion and code-referencing policies**?  
A. Copilot Spaces ignore content exclusion rules so Copilot can always read every attached file  
B. Copilot Spaces temporarily turn off matching-public-code and duplication checks while you use them  
C. **Copilot Spaces package curated context, but still respect organization and enterprise policies like content exclusion and code referencing**  
D. Copilot Spaces automatically treat all attached code as public and eligible for model training  
**Correct Answer(s):** C  

210. Which set of **sources** can you add to a **Copilot Space** to make Copilot a “project expert”?  
A. Only a single README file exported as PDF, without linking any live repositories, issues, or pull requests  
B. **Files, repositories, pull requests, and issues from GitHub that represent your project’s code and documentation**  
C. Only external data sources such as databases and cloud logs, without attaching any GitHub repositories or issues  
D. Only ad-hoc code snippets manually pasted into the chat window, with no persistent link to GitHub content  
**Correct Answer(s):** B  

211. What is a key difference between **Copilot Agent Mode** and standard Copilot Chat?  
A. Standard Chat can only answer questions, while Agent Mode is limited to viewing logs and cannot edit code or run commands  
B. **Agent Mode can autonomously perform multi-step tasks (edit files, run commands, open PRs) based on a high-level goal**  
C. Agent Mode is restricted to Q&A and cannot change files or execute any tools  
D. Agent Mode and standard Chat are identical in capability and differ only in UI  
**Correct Answer(s):** B  

212. Which is the **best prompt** to give Copilot Agent Mode when building a new feature?  
A. “Fix everything in this repository and change whatever you think is necessary across all services.”  
B. **“Implement a new /reports endpoint in this service that returns JSON summaries; update routing, handlers, and add tests. Keep existing APIs unchanged.”**  
C. “Write some code for me.”  
D. “Refactor something somewhere in the codebase to make it better.”  
**Correct Answer(s):** B  

213. In a **TDD-style workflow** using Copilot Agent Mode, what is an appropriate sequence?  
A. Write implementation code first, let Agent Mode delete or skip any failing tests, then deploy if the build is green  
B. **Use Chat or Agent Mode to scaffold failing tests, then have Agent Mode implement the code to satisfy them, and finally review and refactor with tests passing**  
C. Ask Agent Mode to generate both code and tests in one pass and skip manual review as long as tests compile  
D. Turn tests off while Agent Mode works, then enable them again only in production  
**Correct Answer(s):** B  

214. Which scenario **best fits** using Copilot Agent Mode instead of a simple edit or inline suggestion?  
A. Renaming a single local variable inside one function in a single file  
B. Correcting a spelling mistake in a comment that appears in one file  
C. **Updating a feature that spans multiple files (API contract, data model, and tests), and adjusting a CI script to run new tests as part of the same change**  
D. Writing a short, one-line SQL query for a quick check in a scratch file  
**Correct Answer(s):** C  

215. When Copilot Agent Mode opens a **pull request** after completing a task, what is the **developer’s responsibility**?  
A. None, the pull request from Copilot can be merged automatically without human review or checks  
B. Only verify that the branch has no merge conflicts before approving the pull request  
C. **Review the PR like any other: inspect diffs, run tests, ensure it meets security/compliance and coding standards**  
D. Accept all changes solely because they were generated by Copilot, without additional validation  
**Correct Answer(s):** C  

216. Which scenario is the **best fit** for using the **GitHub Copilot coding agent** instead of inline suggestions or simple Chat edits?  
A. Quickly renaming a local variable in the current file using a single, simple change  
B. Formatting a single function to match style guidelines in one file  
C. **Implementing a new feature described in a GitHub issue, updating multiple files, running tests, and opening a draft PR**  
D. Viewing a read-only summary of a pull request without making any changes  
**Correct Answer(s):** C  

217. What is a **unique capability** of the **GitHub Copilot coding agent** compared to inline suggestions and basic Chat edits?  
A. It can bypass existing branch protection rules and merge changes directly to the default branch  
B. It can modify a developer’s IDE configuration and extensions without any prompts  
C. **It can work from a GitHub issue, run tasks in a separate environment, and raise a pull request for you to review**  
D. It can delete repositories automatically when tests fail in CI  
**Correct Answer(s):** C  

218. How do **branch protections and required reviews** interact with changes made by the **Copilot coding agent**?  
A. The coding agent automatically merges its pull requests as long as the tests in CI pass  
B. The coding agent ignores branch protection rules so that changes can be merged faster  
C. **The coding agent’s pull requests are still subject to existing branch protections, required reviews, and status checks**  
D. The coding agent can operate only on branches that have no protection rules configured  
**Correct Answer(s):** C  

219. For **GitHub Copilot Business and Enterprise** customers, how is **access to the Copilot coding agent** controlled?  
A. The coding agent is always enabled for all repositories and cannot be restricted or turned off  
B. **Access to the coding agent is controlled by organization and enterprise policies, which can enable or disable the agent for specific repositories and users**  
C. The coding agent can only be configured via a special `.yml` file stored in each repository  
D. Each individual developer enables or disables the coding agent solely from their IDE settings, regardless of org policy  
**Correct Answer(s):** B  

220. What’s the **practical difference** between using **Copilot Edits – Edit mode** and assigning work to the **Copilot coding agent**?  
A. Edit mode can only rename variables inside a single file, while the coding agent can only update documentation comments.  
B. **Edit mode applies scoped changes you review in your editor; coding agent autonomously executes multi-step tasks and raises a PR**  
C. Edit mode ignores branch protections while the coding agent must always merge to a protected branch.  
D. There is no functional distinction between Edit mode and the coding agent; they use the exact same workflow and capabilities.  
**Correct Answer(s):** B  

221. How does **Copilot coding agent (Agent mode)** differ from a simple Copilot Chat reply or Edit mode?  
A. Agent mode never contacts GitHub services and runs entirely offline in the IDE.  
B. **Agent mode can autonomously perform multi-step tasks (edit multiple files, run tools/commands) and can open a pull request for review**  
C. Agent mode automatically merges to the default branch whenever tests pass, without human intervention.  
D. Agent mode is allowed to bypass branch protections and required reviewers to speed up delivery.  
**Correct Answer(s):** B  

222. When Copilot coding agent runs on GitHub.com for a repository, what **permissions** does it effectively have?  
A. It automatically receives admin access to all repositories in the enterprise, regardless of the user’s role.  
B. It can push directly to protected branches and bypass required reviews if tests pass.  
C. **It acts with the same repository permissions as the signed-in user who invokes it**  
D. It can only ever read code; it cannot create branches or open pull requests.  
**Correct Answer(s):** C  

223. Which of the following is a **recommended practice** when using Copilot coding agent to make changes in your repository?  
A. Merge agent-created pull requests immediately as long as they compile, skipping reviews and tests.  
B. Turn off branch protections and required checks so the agent can push directly to the default branch.  
C. **Review the agent’s pull requests, run tests and security checks, and ensure changes meet your team’s standards before merging**  
D. Grant the agent effective admin rights so it can force-push and rewrite history to simplify fixes.  
**Correct Answer(s):** C  

224. Which scenario is the **best fit** for using Copilot coding agent instead of just inline suggestions or a single Chat prompt?  
A. **You need to update a feature across several files, run tests, and then open a PR that ties the changes together**  
B. You only need to rename a single local variable in one function within the current file.  
C. You just want a one-off code snippet in a scratch file with no follow-up work.  
D. You want to modify organization-wide billing and subscription settings in GitHub.  
**Correct Answer(s):** A  

225. Which of the following **prompting approaches** best supports **responsible use** of Copilot coding agent on GitHub.com?  
A. “Fix everything that’s wrong in this repo and push directly to `main` without opening a pull request or running tests.”  
B. “Rewrite this service however you want; I’ll merge whatever you generate without reviews or checks.”  
C. **“In this repo, update only the payment validation logic to add address checks; keep public APIs stable, add or update tests, and open a PR summarizing what you changed.”**  
D. “Gain admin access across all org repositories and remove branch protections so changes can be merged faster without approvals.”  
**Correct Answer(s):** C  

226. Which set of **sources** can you add to a **Copilot Space** to make Copilot a “project expert”?  
A. Only a single README file exported as PDF, without linking any live repositories, issues, or pull requests  
B. **Files, repositories, pull requests, and issues from GitHub that represent your project’s code and documentation**  
C. Only external data sources such as databases and cloud logs, without attaching any GitHub repositories or issues  
D. Only ad-hoc code snippets manually pasted into the chat window, with no persistent link to GitHub content  
**Correct Answer(s):** B  

227. What is the primary advantage of using the **Copilot coding agent (Agent mode)** compared to regular inline suggestions or simple chat edits?  
A. It guarantees that all generated code is secure, fully compliant, and bug-free without any need for testing or review.  
B. **It can autonomously perform multi-step tasks across files and tools, and then propose changes or open a PR for review**  
C. It runs entirely on-premises with no dependency on GitHub’s cloud services or hosted environments.  
D. It bypasses branch protections, required reviews, and CI checks so changes can be merged more quickly.  
**Correct Answer(s):** B  

228. In a **regulated enterprise**, what is the main purpose of the **Copilot coding agent firewall**?  
A. To prevent the coding agent from ever generating code that calls external APIs, even as plain source code.  
B. To enforce project-level formatting and linting rules before any pull request can be opened.  
C. **To control which domains/URLs the coding agent can access, reducing data exfiltration risk**  
D. To limit the agent to editing only one file per task so that multi-file changes cannot occur.  
**Correct Answer(s):** C  

229. Which type of request is **best suited** for the **Copilot coding agent**, rather than a simple inline suggestion?  
A. “Add a single null-check on this line so the app doesn’t crash; don’t touch any other code.”  
B. “Reformat this file with our standard code style, but don’t change behavior or add tests.”  
C. **“Investigate why these tests are failing, update the implementation if needed, and propose a fix I can review.”**  
D. “Rename this local variable to something clearer in just this function.”  
**Correct Answer(S):** C  

230. How does **extending the Copilot coding agent with MCP (Model Context Protocol) servers** help in real-world workflows?  
A. It gives Copilot the ability to retrain its base foundation models directly on your repositories and telemetry data.  
B. **It lets the coding agent call specialized tools and data sources (for example, GitHub or Playwright MCP servers) as part of a task**  
C. It automatically disables the agent firewall, content exclusion, and other governance policies whenever MCP tools are used.  
D. It forces all coding agent computation to run entirely on-premises instead of in GitHub-hosted environments.  
**Correct Answer(s):** B  

231. From an **enterprise admin** perspective, what is a recommended approach to rolling out the **Copilot coding agent**?  
A. Enable the coding agent everywhere for all members with no firewall, no policies, and no monitoring, and let each team decide how to use it.  
B. **Pilot the coding agent with a small group, keep the firewall enabled, and monitor usage before broader rollout**  
C. Disable the coding agent permanently and rely only on inline suggestions and basic chat.  
D. Allow the coding agent only if all content exclusion and code-referencing policies are turned off so it has unrestricted access.  
**Correct Answer(s):** B  

232. How does **Copilot coding agent** typically operate on a task assigned from GitHub.com?  
A. It edits files directly in your local IDE without ever creating branches or pull requests  
B. It connects to an on-premises GitHub Enterprise Server (GHES) instance and runs entirely there  
C. **It initializes a cloud dev environment (GitHub Actions–powered), makes changes in a branch, and drafts a pull request for review**  
D. It automatically merges its changes into the default branch as soon as tests pass, bypassing normal reviews  
**Correct Answer(s):** C  

233. Which responsibilities remain with **developers/teams** when using Copilot coding agent? *(Choose all that apply.)*  
A. **Reviewing and approving the pull request before merge**  
B. **Ensuring tests, linters, and security scans pass for the changes**  
C. Allowing the agent to bypass branch protections and merge directly to production as long as tests appear to pass  
D. **Defining safe, well-scoped tasks/issues for the agent to work on**  
**Correct Answer(s):** A, B, D  

234. How do you customize the **environment** that Copilot coding agent uses when working on a repository?  
A. Configuring a `.copilot-env.json` file in your personal home directory so the agent automatically mirrors your local tools  
B. Changing your local dev container configuration so the agent reuses it without any repository-level setup  
C. **Adding a `.github/workflows/copilot-setup-steps.yml` workflow that declares setup steps (tools, commands, environment) for the agent’s cloud environment**  
D. Setting environment variables only in the GitHub UI while ignoring any repository configuration files  
**Correct Answer(s):** C  

235. Which scenario is **most appropriate** for assigning work to **Copilot coding agent**?  
A. Directly rotating production database credentials and applying schema changes live in production without going through a branch or pull request  
B. **Implementing a feature from a well-defined issue (with acceptance criteria), where the agent can work in a branch and open a PR**  
C. Manually hotfixing a live outage in production using ad-hoc shell access and one-off commands  
D. Automatically managing enterprise SSO configuration and audit log settings without human involvement  
**Correct Answer(s):** B  

236. Which task is **most appropriate** to assign to **GitHub Copilot coding agent in Agent mode**?  
A. Designing an entirely new mission-critical payments architecture from scratch, with no existing codebase, tests, or clear acceptance criteria  
B. Taking over an active production incident involving PII exposure and making security tradeoffs autonomously in real time  
C. **Updating a UI component library across the repo to use a new button component, running tests in the agent’s environment, and opening a PR with changes**  
D. Rewriting all pricing-related business logic based only on a vague one-line description with no tests or documentation  
**Correct Answer(s):** C  

237. How does **Copilot coding agent** typically operate on a task assigned from GitHub.com?  
A. It edits files directly in your local IDE without ever creating a branch or PR  
B. It connects to and runs directly inside your on-prem GHES instance  
C. **It initializes a cloud dev environment (GitHub Actions–powered), makes changes in a branch, and drafts a pull request for review**  
D. It automatically merges its changes to the default branch as soon as tests pass  
**Correct Answer(s):** C  

238. Which responsibilities remain with **developers/teams** when using Copilot coding agent? *(Choose all that apply.)*  
A. **Reviewing and approving the pull request before merge**  
B. **Ensuring tests, linters, and security scans pass for the changes**  
C. Allowing the agent to merge directly to production without any human review  
D. **Defining safe, well-scoped tasks or issues for the agent to work on**  
**Correct Answer(s):** A, B, D  

239. How do you customize the **environment** that Copilot coding agent uses when working on a repository?  
A. By editing a `.copilot-env.json` file in your local home directory  
B. By modifying your local dev container; the agent automatically mirrors it in the cloud  
C. **By adding a `copilot-setup-steps.yaml` file that declares setup steps (tools, commands, environment) for the agent’s cloud environment**  
D. By setting environment variables only in the GitHub UI; repository workflow files are ignored  
**Correct Answer(s):** C  

240. Which scenario is **most appropriate** for assigning work to **Copilot coding agent**?  
A. Rotating live production database credentials and applying schema changes directly in production  
B. **Implementing a feature from a well-defined issue (with acceptance criteria), where the agent can work in a branch and open a PR**  
C. Manually hotfixing a live outage in production over shell access  
D. Automating enterprise SSO, audit log configuration, and other security admin tasks  
**Correct Answer(s):** B  


241. Which task is **most appropriate** to assign to **GitHub Copilot coding agent in Agent mode**?  
A. Designing a brand-new architecture for a mission-critical payments platform with no existing code, tests, or safety nets  
B. Handling an active production incident involving PII exposure and complex security tradeoffs  
C. **Updating a shared UI component library across the repo to use a new button component, running tests in the agent’s environment, and opening a PR with changes**  
D. Rewriting all pricing business logic from scratch based only on a vague one-line description  
**Correct Answer(s):** C  

242. Which statement best describes **where and how** GitHub Copilot coding agent runs your code changes?  
A. It compiles and runs everything directly on each developer’s local machine using their local tools  
B. It runs only in a fixed, shared VM that you manually provision and manage  
C. **It uses an ephemeral development environment powered by GitHub Actions, where it can explore the repo, make changes, and run tests/linters before opening a PR**  
D. It can only edit text and cannot run tests or tools at all  
**Correct Answer(s):** C  

243. Which statement about **plan availability** for GitHub Copilot coding agent is correct?  
A. Coding agent is available only on Copilot Enterprise  
B. Coding agent is available on all Copilot plans, including Copilot Free  
C. **Coding agent is available with Copilot Pro, Copilot Pro+, Copilot Business, and Copilot Enterprise**  
D. Coding agent is available only on Copilot Business and Enterprise (not on individual plans)  
**Correct Answer(s):** C  

244. You want Copilot coding agent to **build and test faster and more reliably** when it works on tasks in your repository. What should you do?  
A. Ask every developer to run `npm install` locally before assigning issues to Copilot  
B. **Add a `copilot-setup-steps.yml` file that pre-installs your project’s dependencies in the agent’s environment**  
C. Disable all tests so the agent doesn’t need dependencies  
D. Create a `.gitignore` entry for `node_modules` so Copilot can infer everything automatically  
**Correct Answer(s):** B  

245. Which scenario best reflects **GitHub’s guidance on when *not* to assign a task** to Copilot coding agent?  
A. Updating CSS variables across the design system and running existing visual regression tests  
B. Improving unit test coverage for a well-documented service with clear acceptance criteria  
C. Refactoring a small helper module to remove duplication, with existing tests in place  
D. **Investigating and fixing a live incident involving PII leakage and authentication failures in production**  
**Correct Answer(s):** D  

246. You need to **standardize logging** in a small service: update a helper to emit structured JSON logs, add one new log call in a single controller, and review a focused diff before any changes land. Which Copilot capability is the **best fit** for this task?  
A. Use the Copilot coding agent in Agent mode to refactor the entire repository  
B. **Use Copilot Edits in Edit mode on the two affected files**  
C. Ask Copilot Chat to “fix logging everywhere” without specifying files  
D. Use repository-aware chat on GitHub.com to auto-merge a PR  
**Correct Answer(s):** B  

247. How does **Copilot coding agent** typically operate on a task assigned from GitHub.com?  
A. It edits files directly and permanently in your local IDE without using branches or pull requests  
B. It connects to a self-hosted GitHub Enterprise Server (GHES) instance and runs entirely on-premises  
C. **It initializes a cloud dev environment (GitHub Actions–powered), makes changes in a branch, and drafts a pull request for review**  
D. It automatically merges its changes to the default branch as soon as tests pass, bypassing normal review rules  
**Correct Answer(s):** C  

248. Which responsibilities remain with **developers/teams** when using Copilot coding agent? *(Choose all that apply.)*  
A. **Reviewing and approving the pull request before merge**  
B. **Ensuring tests, linters, and security scans pass for the changes**  
C. Allowing the agent to auto-merge its pull requests directly into production branches as long as tests pass  
D. **Defining safe, well-scoped tasks and issues for the agent to work on**  
**Correct Answer(s):** A, B, D  

249. How do you customize the **environment** that Copilot coding agent uses when working on a repository?  
A. By editing a personal `.copilot-env.json` file in your local home directory, which the agent automatically syncs and executes in the cloud  
B. By updating your local dev container configuration and assuming the agent will mirror that environment without any repository-side config  
C. **By adding a `copilot-setup-steps.yaml` file that declares setup steps (tools, commands, environment) for the agent’s cloud environment**  
D. By setting environment variables only in the GitHub UI and ignoring any workflow files in the repository  
**Correct Answer(s):** C  

250. Which scenario is **most appropriate** for assigning work to **Copilot coding agent**?  
A. Directly rotating production database credentials and applying schema changes in a live production environment  
B. **Implementing a feature from a well-defined issue (with acceptance criteria), where the agent can work in a branch and open a pull request for review**  
C. Performing manual hotfixes during a live production outage using ad-hoc shell access on production hosts  
D. Automatically configuring enterprise SSO, audit logging, and other security-sensitive admin settings without human oversight  
**Correct Answer(s):** B  

251. Which task is **best suited** for GitHub Copilot **coding agent** rather than being handled entirely by a human developer?  
A. Designing a new cross-team architecture that spans several organizations and requires months of stakeholder alignment  
B. Leading an incident call to triage an active production outage and manually applying hotfixes in production  
C. **Implementing a backlog item to add pagination to an existing list view, updating the API, UI, and tests, and opening a PR for review**  
D. Running a brown-bag training session to teach new hires how the legacy monolith works in detail  
**Correct Answer(s):** C  

252. How does **GitHub Copilot coding agent** execute builds and tests for a task it’s working on?  
A. It runs directly in your IDE, reusing your local tools and terminal session, and never uses GitHub Actions  
B. It runs only on GitHub Enterprise Server (GHES), inside runners that you manage entirely on-premises  
C. **It uses an ephemeral development environment backed by GitHub Actions runners, where it can clone the repo, make changes, and run tests and linters before updating a PR**  
D. It edits files in your default branch on GitHub.com but cannot run any builds, tests, or other commands  
**Correct Answer(s):** C  

253. Which statement correctly describes **who can use GitHub Copilot coding agent**?  
A. Coding agent is available only with Copilot Enterprise; Pro, Pro+, Business, and Free users cannot use it  
B. Coding agent is available on **all** Copilot plans, including Copilot Free  
C. **Coding agent is available with Copilot Pro, Copilot Pro+, Copilot Business, and Copilot Enterprise**  
D. Coding agent is available only with Copilot Business and Enterprise, and not with any individual plans  
**Correct Answer(s):** C  

254. Your team notices that Copilot coding agent spends a lot of time **figuring out how to install dependencies**, and sometimes fails to run tests because private packages aren’t available. How should you improve the **speed and reliability** of the agent’s runs?  
A. Ask each developer to run all installs locally and push `node_modules` or `vendor` directories into the repo so the agent doesn’t need to install anything  
B. Put your usual setup commands into a personal shell script in your home directory; the agent will automatically detect and run it  
C. **Create a `.github/workflows/copilot-setup-steps.yml` workflow that pre-installs required tools and dependencies in the agent’s environment**  
D. Disable tests in the repository’s CI so Copilot never has to run them and will always “succeed” quickly  
**Correct Answer(s):** C  

255. Which scenario best exemplifies a task that **should not** be delegated to GitHub Copilot coding agent, according to GitHub’s guidance?  
A. Cleaning up duplicated helper functions in a utility module, with good test coverage in place  
B. Adding accessibility improvements (ARIA attributes) to a few UI components and updating snapshots  
C. Writing missing unit tests for a well-understood service with clear acceptance criteria  
D. **Coordinating and implementing fixes for an ongoing production incident involving leaked access tokens and repeated authentication failures**  
**Correct Answer(s):** D  

256. You want to **standardize error handling** in a service by:  
- Updating a shared `handleError` helper in one file  
- Adding a single new `try/catch` around one call site in another file  
- Reviewing a **small, focused diff** before committing  

You **do not** need Copilot to run tests, call tools, or discover additional files on its own. Which Copilot capability is the **best fit**?  
A. Use Copilot coding agent from GitHub.com to autonomously refactor the entire service and open a PR  
B. **Use Copilot Edits in Edit mode on just the two relevant files, then review and apply the proposed diff**  
C. Use agent mode in your IDE so Copilot can freely edit any file in the workspace and run terminal commands  
D. Ask Copilot Chat in Ask mode for code snippets and paste them into files manually without any diff view  
**Correct Answer(s):** B  


257. A product manager opens a GitHub issue describing a **new API endpoint**. You want Copilot to: read the issue and code, add route/handler/tests, run tests, and open a PR with a summary. Which capability fits?  
A. Inline suggestions at the cursor to manually implement the endpoint and tests in one file at a time.  
B. Copilot Chat in a single IDE conversation to propose patches, then copy and apply them manually.  
C. **Copilot coding agent (Agent mode) acting from the issue**  
D. Repository-aware chat on GitHub.com to discuss the design without applying any code changes.  
**Correct Answer(s):** C  

258. Which scenario is **most appropriate** for using the **Copilot coding agent**, rather than only using Copilot Chat inside your IDE?  
A. Asking “Why does this function fail?” and pasting a stack trace for Copilot Chat to explain in your IDE.  
B. **Implementing a backlog item that requires edits across multiple services, running tests, and opening a PR**  
C. Renaming a local variable in a single file, then manually committing the change.  
D. Generating a one-off code snippet for a small helper function you’ll paste into a file.  
**Correct Answer(s):** B  

259. You want to delegate a task to the **Copilot coding agent**. Which instruction gives it the **most useful guidance**?  
A. “Fix everything that’s wrong in this repo and refactor as needed until there are no issues left.”  
B. **“From this issue, implement the `order-cancellation` endpoint end-to-end: update the API spec, add handler + routing, write integration tests, and open a PR when tests pass.”**  
C. “Refactor as you see fit; you decide what to change and where.”  
D. “Make the code better and faster in general, using your judgment.”  
**Correct Answer(s):** B  

260. After the **Copilot coding agent** completes a task and opens a pull request, what is the **team’s responsibility**?  
A. None, the agent’s PR can be merged without human review, because all tests are implicitly guaranteed to pass.  
B. Only check that the PR description is formatted nicely before allowing automatic merge rules to apply.  
C. **Review the changes, run or verify tests, and ensure the PR meets security and quality standards before merging**  
D. Re-run the agent until it merges the PR on its own without any human approval.  
**Correct Answer(s):** C  

261. Where are Copilot prompts and allowed context processed?  
A. Only on the local IDE; nothing leaves the machine, and no data is sent to any GitHub or model service.  
B. **In the Copilot cloud service, which relays requests to the selected AI model per GitHub’s data pipeline**  
C. On your company’s GitHub Enterprise Server only, with no Copilot cloud service involved.  
D. Inside your CI runners, where prompts are stored and processed as part of builds.  
**Correct Answer(s):** B  

262. Does GitHub Copilot train on your **private code**?  
A. Yes, always your private code is automatically used to train Copilot models in all plans.  
B. Yes, unless product telemetry is disabled at the enterprise or org level.  
C. **No, private code is not used to train Copilot models**  
D. Only for Enterprise customers, where private code is always used for training unless they opt out.  
**Correct Answer(s):** C  

263. What does **Content exclusion** actually do?  
A. Censors outputs that are similar to excluded files, but still allows those files to be used as input context.  
B. **Prevents specified repositories/paths/file types/patterns from being used as input context**  
C. Disables Copilot completely for the repository or organization.  
D. Removes excluded files from Git history so Copilot cannot see prior versions.  
**Correct Answer(s):** B  

264. How does Copilot handle suggestions that **exactly match** long segments of public code?  
A. Always allows long exact matches from public code, but adds a warning about possible licensing issues.  
B. Allows or blocks long exact matches purely based on the original repository’s license.  
C. **Uses duplication-detection filters to block long exact matches (≈150+ characters)**  
D. Publishes any long exact matches it generates directly back to public GitHub repositories.  
**Correct Answer(s):** C  

265. Which statement best describes **Copilot usage telemetry/metrics**?  
A. Copilot collects no usage data  
B. **Telemetry aggregates activity and feature usage (e.g., suggestions, chat, agents), not a dump of your source code**  
C. Telemetry always includes raw file contents  
D. Telemetry is only available to Enterprise customers  
**Correct Answer(s):** B  

266. Do **content exclusion** rules apply across all supported Copilot **surfaces** (IDE, GitHub.com, CLI, Mobile)?  
A. No, only in VS Code  
B. Only on GitHub.com  
C. Only in JetBrains IDEs  
D. **Yes, exclusion defines the input context boundary for Copilot regardless of surface**  
**Correct Answer(s):** D  

267. At which **scopes** can you configure **code referencing / matching public code**?  
A. Only at the repo level  
B. Only at the enterprise level  
C. **At the individual account level and via org/enterprise policies**  
D. Only in IDE settings  
**Correct Answer(s):** C  

268. Is GitHub Copilot supported on **GitHub Enterprise Server (GHES)**?  
A. Yes, Copilot runs entirely on-prem  
B. Yes, but only chat  
C. **No, Copilot requires the cloud service; GHES is not supported**  
D. Yes, with a self-hosted model  
**Correct Answer(s):** C  

269. Which statement about **repository-aware Copilot Chat on GitHub.com** is accurate?  
A. Available to all plans by default  
B. Requires GHES  
C. **It’s an Enterprise capability that lets chat reference repository files/docs on GitHub.com**  
D. It runs offline in the IDE only  
**Correct Answer(s):** C  

270. If an **enterprise policy** enforces “Block matching public code,” can an organization **override** it?  
A. Yes, at the org level—an organization owner can always change “Block matching public code” to “Allow” even if the enterprise enforces it.  
B. Yes, at the repo level—repo admins can override an enforced enterprise policy for their specific repositories.  
C. **No, enterprise-enforced policies take precedence**  
D. Only for public repositories—orgs can override enforcement for private repos but not public ones.  
**Correct Answer(s):** C  


271. What’s the difference between **Content exclusion** and **Code referencing (“matching public code”)**?  
A. Both features block any suggestion that looks similar to either private or public code, acting as identical output filters.  
B. Content exclusion hides Copilot’s suggestions that look similar to excluded files, while code referencing only limits which repositories Copilot can read from.  
C. **Content exclusion limits what Copilot can see as input context; code referencing governs outputs that resemble public code**  
D. They’re identical governance controls with different names and UIs, and are always configured together.  
**Correct Answer(s):** C  

272. Which statement best describes what **Copilot usage metrics** capture (and don’t capture)?  
A. Full copies of your source files and diffs, stored indefinitely for auditing and replay of developer activity.  
B. Private repository file contents that are fed directly into model training pipelines for Copilot.  
C. **Activity and feature-usage signals (e.g., suggestions, chat, agents) with defined fields/retention not raw source code**  
D. Only low-level error logs from IDE extensions, with no information about feature usage or adoption.  
**Correct Answer(s):** C  

273. How can Copilot best support a **TDD (red→green→refactor)** workflow?  
A. Use Copilot to automatically approve and merge pull requests whenever the test suite passes, replacing human review.  
B. **By drafting test stubs/cases from a selection or spec, then assisting with targeted code changes until tests pass**  
C. Use Copilot to automatically comment out or disable failing tests during development to keep the suite green.  
D. Ask Copilot to skip or remove assertions to speed up development cycles, adding them back later if needed.  
**Correct Answer(s):** B  

274. After Copilot generates a suite of unit tests, what’s the **next** best action?  
A. Merge the changes immediately because AI-generated tests guarantee correctness and coverage.  
B. **Review assertions/fixtures, add missing edge cases, and run the suite to measure coverage**  
C. Delete all generated tests and always rewrite them entirely by hand.  
D. Temporarily disable branch protections so you can merge faster without running tests.  
**Correct Answer(s):** B  

275. Which of the following is **NOT** something Copilot does for testing?  
A. Generate test templates, scaffolds, and suggested assertions for functions and classes.  
B. Help create parameterized or table-driven tests based on a highlighted function and your chosen framework.  
C. Assist with test refactors, naming, and organizing fixtures to improve readability and maintainability.  
D. **Run your test framework automatically in CI**  
**Correct Answer(s):** D  

276. How does Copilot help during **pull request reviews** on GitHub.com?  
A. Automatically approve and merge pull requests whenever required checks pass, bypassing human reviewers.  
B. **Generates natural-language PR summaries and review suggestions to speed understanding**  
C. Rewrite commit history and amend commits to enforce style and format rules.  
D. Disable required reviewers or branch protections when its confidence in the change is high.  
**Correct Answer(s):** B  

277. Which combination best enforces **quality gates** when adopting Copilot-generated changes?  
A. Accept Copilot’s suggestions, skip tests entirely, and merge to maximize speed.  
B. Accept Copilot’s suggestions, rely only on informal review, and merge without CI checks.  
C. **Accept suggestions → run tests/coverage in CI → code review with PR summaries → (optionally) code scanning → merge**  
D. Accept suggestions and rely only on duplication filters to catch any issues before merging.  
**Correct Answer(s):** C  

278. What’s the most effective way to have Copilot generate **parameterized (table-driven) tests**?  
A. Ask Copilot to “write tests” with no further details about the code under test, the framework, or how you want cases structured.  
B. **Select the target function and ask for “parameterized/table-driven tests” in your framework (e.g., pytest parametrize/JUnit @MethodSource)**  
C. First generate large, end-to-end integration tests, then manually split them into smaller parameterized unit tests.  
D. Rely on duplication filters alone to expand a single example into multiple parameterized cases automatically.  
**Correct Answer(s):** B  

279. Which statement about **coverage and quality** is accurate when using Copilot for tests?  
A. Copilot guarantees 100% test coverage whenever you ask it to “cover all cases,” so manual coverage measurement is unnecessary.  
B. Copilot automatically runs mutation testing tools in your CI pipeline and tunes assertions accordingly.  
C. **Developers must measure coverage and strengthen assertions; Copilot provides a starting point**  
D. Coverage no longer matters if you enable AI PR summaries and rely on them to catch issues.  
**Correct Answer(s):** C  

280. You accepted Copilot’s suggested tests, but some are **flaky**. What’s the best next step?  
A. Disable flaky tests so CI stays green and rely on manual testing in production to catch regressions.  
B. **Stabilize by isolating external dependencies (mocks/fakes), add deterministic fixtures, and minimize timing sensitivity**  
C. Increase global timeouts or add retries across the entire suite to hide intermittent failures.  
D. Rerun the CI job repeatedly until it passes once, then merge and mark the issue as resolved.  
**Correct Answer(s):** B  

281. How do **Content exclusion** and **code referencing (matching public code)** relate to testing with Copilot?  
A. Both features only apply to application source files; test files are always fully visible to Copilot and exempt from governance controls.  
B. **Content exclusion restricts what Copilot can read as input (including test files); code referencing governs output similarity to public code**  
C. Content exclusion automatically detects and quarantines flaky tests so they are never executed.  
D. Code referencing runs your test suite to find failing tests that match public code snippets.  
**Correct Answer(s):** B  

282. You want Copilot to draft **Given/When/Then** test **templates** before implementation. What should you do?  
A. Write all production code first so Copilot can only infer tests from existing implementations, then ask it to add tests afterward.  
B. **Provide a short BDD-style spec (Given/When/Then), the test framework, and ask Copilot to scaffold failing tests**  
C. Ask Copilot to implement the feature and explicitly skip test creation to save time.  
D. Rely on PR summaries alone to auto-generate tests after the feature is implemented.  
**Correct Answer(s):** B  

283. When should you choose **Copilot Edits (Edit mode)** instead of **Agent mode**?  
A. Ask Copilot to autonomously run terminal commands, update multiple files, and open a pull request without you selecting specific files.  
B. **When you want targeted, reviewable diffs on a small, well-scoped change**  
C. Use Copilot to coordinate edits across many files, update tests and configs, and run commands as part of a multi-step workflow.  
D. Use Copilot to bypass branch protections and required reviews so changes can merge immediately.  
**Correct Answer(s):** B  

284. What can **Copilot Agent mode** do in a repository that **Copilot Edits** does not?  
A. Let Copilot bypass required reviews and merge directly when it thinks changes are safe.  
B. Merge directly to the default branch, ignoring status checks and branch protection rules.  
C. **Run multi-step workflows (e.g., edit across files, run commands) and open a pull request**  
D. Temporarily disable branch protections to allow Copilot to push hotfixes.  
**Correct Answer(s):** C  

285. You must: generate tests, update config, run tests, fix failures, and then open a PR. Which split best reflects **Chat vs. Agent**?  
A. Let Copilot Chat run tests and open PRs while the coding agent focuses only on drafting test code.  
B. **Chat: draft tests/config; Agent: run commands, iterate, open PR**  
C. Use Copilot Chat for every step (draft, run, open PR) and never use the coding agent.  
D. Use the coding agent only to write code, while Copilot Chat runs terminal commands and manages PRs.  
**Correct Answer(s):** B  

286. Which workflow is **safest** when asking the coding agent to run terminal steps?  
A. Run the coding agent directly on the default branch to avoid branch management and potential conflicts.  
B. Skip running tests to save time, relying on the agent’s confidence instead.  
C. **Work on a feature branch, keep changes small, run tests, and be ready to revert**  
D. Temporarily disable required checks and protections so the agent can land changes faster.  
**Correct Answer(s):** C  

287. What’s the right way to treat **Copilot PR summaries and review suggestions**?  
A. Treat Copilot PR summaries and review suggestions as authoritative approvals that replace human reviewers.  
B. Use Copilot summaries as automatic passes for required status checks so PRs can merge without tests.  
C. **As helpful input that does not replace required reviews or protections**  
D. Use Copilot summaries to merge directly to main without any approvals when changes look small.  
**Correct Answer(s):** C  

288. When is **Agent mode** likely **overkill**, and a different approach is better?  
A. You need to rename a parameter and update one docstring in a single file.  
B. You must run tests, fix failures across multiple packages, and open a PR with the results.  
C. You need to regenerate a lockfile and re-run a multi-step build or test workflow in CI.  
D. You want the tool to bypass required reviews and branch protections so changes can merge automatically.  
**Correct Answer(s):** A  

289. What’s a **safe boundary** pattern when letting the coding agent run commands?  
A. Run the coding agent directly on the default branch with protections disabled so it can land changes faster.  
B. **Work on a feature branch, require status checks, commit in small steps, and provide a rollback plan**  
C. Allow force-pushes to the main branch so the agent can rewrite history as needed.  
D. Skip tests to reduce noise in PRs and rely on manual spot-checking instead.  
**Correct Answer(s):** B  

290. How do **branch protections** interact with **Copilot review suggestions**?  
A. Copilot suggestions automatically count as approving reviews and satisfy required reviewers.  
B. Copilot can merge a pull request whenever CI is green, even if no human has approved it.  
C. **Required reviewers and status checks still apply; Copilot suggestions don’t override protections**  
D. Copilot can dismiss CODEOWNERS and other required reviewers to speed up merges.  
**Correct Answer(s):** C  

291. Which is the **best practice** when Copilot suggests changes during PR review?  
A. Auto-commit Copilot’s suggestions directly to the default branch so they bypass pull request review.  
B. **Apply suggestions to the PR branch, rerun checks, and request required reviewers to re-review**  
C. Merge immediately after applying a suggestion if the code compiles locally.  
D. Remove or relax CODEOWNERS to avoid delays from expert review.  
**Correct Answer(s):** B  

292. You want subject-matter experts to always review changes in specific paths. What should you rely on?  
A. Copilot PR summaries alone to automatically route reviews and decide who must approve.  
B. The coding agent to infer the right reviewers from file names and assign them dynamically.  
C. **A CODEOWNERS file to require reviews from designated owners for matching paths**  
D. Configure repository secrets so merges are blocked unless experts leave a comment.  
**Correct Answer(s):** C  

293. You need to: run tests, update failing snapshots, touch code across 4 files, refresh docs, and open a PR. Which Copilot flow is the best fit?  
A. Rely only on inline completions at the cursor and manage tests, snapshots, and PR creation manually.  
B. **Copilot coding agent (Agent mode) orchestrating edits + commands + PR creation**  
C. Use Copilot Edits (Edit mode) for code changes but skip tests entirely to simplify the workflow.  
D. Skip reviews because CI will catch issues, letting changes merge without human sign-off.  
**Correct Answer(s):** B  

294. Which statement about **PRs created by the coding agent** is correct?  
A. Agent-created PRs automatically merge whenever required checks are green, regardless of review settings.  
B. Agent-created PRs ignore CODEOWNERS rules and only require a maintainer to click merge.  
C. **Branch protections, required checks, and CODEOWNERS still apply**  
D. Agent-created PRs always have admin bypass and can merge even if protections would normally block them.  
**Correct Answer(s):** C  

295. You’re in a **monorepo**. What’s the best way to keep the coding agent from making **unintended cross-package edits**?  
A. Let the agent freely modify the entire monorepo and plan to clean up any unwanted changes later.  
B. **Scope the task with clear paths/packages and request reviewable diffs per package**  
C. Disable tests to speed up iterations even if multiple packages are affected.  
D. Force-push directly to main to avoid branch drift when the agent changes many packages.  
**Correct Answer(s):** B  

296. Which task **best** leverages the coding agent instead of Chat alone?  
A. Use Copilot Chat only to explain a single error message in one file, without asking it to run commands or modify many files.  
B. **Run tests, fix lint issues across modules, update config, and push a branch with a draft PR**  
C. Ask Copilot to generate a one-off helper function inline in your editor.  
D. Use Copilot just to rephrase a paragraph in the README.  
**Correct Answer(s):** B  

297. What’s a **good rollback pattern** when the agent performs iterative fixes?  
A. Work directly on the default branch so rollback is just another commit on main.  
B. Squash all agent commits into a single large commit so intermediate states are hidden.  
C. **Use a feature branch, keep commits small, and revert the PR if needed**  
D. Force-push over history to remove bad states created by the agent.  
**Correct Answer(s):** C  

298. You ask the agent to “**run the test suite and fix failing tests**.” What’s the **safest** expectation?  
A. Expect the agent to bypass branch protections, commit hotfixes directly on main, and merge without review.  
B. **It should run tests, propose minimal code changes with diffs, and push to a branch for PR review**  
C. Expect it to auto-merge its branch whenever tests pass, even if required reviewers haven’t approved.  
D. Let it edit anywhere in the repo until CI turns green, without regard for scope or review.  
**Correct Answer(s):** B  

299. What’s the **primary value** of **Copilot PR summaries**?  
A. They auto-approve PRs when short enough.  
B. **They help reviewers grasp intent, risky areas, and change scope quickly**  
C. They replace CODEOWNERS requirements.  
D. They guarantee no semantic diff errors.  
**Correct Answer(s):** B  

300. How should you treat **Copilot review suggestions** in a security-sensitive repo?  
A. Trust them if CI passes.  
B. **Treat as advisory; apply on a branch, run required checks, and get owner review**  
C. Merge directly to main to minimize drift.  
D. Disable CODEOWNERS for AI-authored changes.  
**Correct Answer(s):** B  
