# Detailed Practice Test 03 - Answer Sheet & Explanation

**Question:** [061]  
Which GitHub Copilot plan(s) surface **Copilot activity in the organization audit log** so admins can review who used Copilot features and when? *(Choose all that apply.)*

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B, C

**Explanation:**  
**Audit visibility** for Copilot is an **organization/enterprise** capability. **Copilot Business** and **Copilot Enterprise** record Copilot-related events (for example, seat grants, policy changes, content-exclusion edits) in the **organization or enterprise audit log** so admins can trace **who**, **what**, and **when** for governance and incident response.

**Tips and Tricks:**  
- Ask: “Is this an **org-level** trail I can query?” If yes, you are in **Business/Enterprise** territory, not **Pro/Free**.  
- Combine **audit logs** with **usage reports** and **policy controls** to close the loop: observe, measure, enforce.

> [!IMPORTANT]  
> **Business already includes audit events** for Copilot. Choose **Enterprise** when you also need **GitHub.com repository-aware Chat** and **enterprise-only integrations**; do not over-attribute “audit” as Enterprise-only.

**Source:**  
[Review activity and audit logs for Copilot](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)  
[Audit log events for your enterprise](https://docs.github.com/en/enterprise-cloud%40latest/admin/monitoring-activity-in-your-enterprise/reviewing-audit-logs-for-your-enterprise/audit-log-events-for-your-enterprise) (GitHub Docs)  
[Reviewing the audit log for your organization](https://docs.github.com/en/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/reviewing-the-audit-log-for-your-organization) (GitHub Docs)  
[Introduction to GitHub Copilot Business](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-for-business/) (Microsoft Learn)

**Question:** [062]  
Which GitHub Copilot plan(s) provide **organization-wide policy controls** such as **content/context exclusions** and **enforced public code filtering**? *(Choose all that apply.)*

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B, C

**Explanation:**  
**Copilot Business** and **Copilot Enterprise** expose **admin policy controls** that shape how suggestions are generated and governed. These include **content/context exclusions** (limit what Copilot can see) and **public-code filtering** (govern what Copilot may suggest or flag with references). Policies can be enforced at **org** scope and, for Enterprise Cloud customers, orchestrated at **enterprise** scope.

**Tips and Tricks:**  
- Map **“governance knobs”** (exclusions, public-code filter, model/feature availability) to **Business/Enterprise**.  
- **Exclusions** reduce **context exposure**; **public-code filtering / code referencing** reduces **IP and license risk** in outputs.

> [!IMPORTANT]  
> Keep controls straight: **Content/Context Exclusion = visibility control**; **Public-Code Filtering/Code Referencing = output control**. Use both for defense-in-depth.

**Source:**  
[Exclude content from Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Managing policies for Copilot in your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/manage-policies) (GitHub Docs)  
[Responsible use of Copilot code completion](https://docs.github.com/en/copilot/responsible-use/copilot-code-completion) (GitHub Docs)  
[Introduction to GitHub Copilot Enterprise](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/) (Microsoft Learn)

**Question:** [063]  
Which GitHub Copilot plan enables **GitHub.com repository-aware Copilot Chat** (summarize/explain code directly from repo files, beyond IDE-only context)?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**Copilot Enterprise** unlocks **GitHub.com repository-aware Chat** for Enterprise Cloud orgs. Beyond IDE context, Chat can reference code, docs, and issues **from the repository** (enhanced by **repository indexing**) to answer questions, summarize changes, and navigate code intelligently.

**Tips and Tricks:**  
- Signals like **“GitHub.com Chat with repo files,” “PR/issue context,”** or **“enterprise knowledge access”** point to **Enterprise**.  
- Keep **Business** for admin governance; move to **Enterprise** when you need **GitHub.com context** and **enterprise-only integrations**.

> [!IMPORTANT]  
> Performance and answer quality improve when **repositories are indexed** for semantic search. Keep indexes fresh for active codebases to maximize Chat accuracy.

**Source:**  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[Indexing repositories for Copilot Chat](https://docs.github.com/en/enterprise-cloud%40latest/copilot/concepts/context/repository-indexing) (GitHub Docs)  
[Copilot features overview](https://docs.github.com/en/enterprise-cloud%40latest/copilot/get-started/features) (GitHub Docs)  
[Get started with GitHub Copilot (product overview)](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [064]  
**Where are prompts processed** when you use GitHub Copilot?

**Options:**  
A. Only on the local IDE; nothing leaves your machine  
B. In the **Copilot cloud service**, which relays to the selected AI model according to GitHub’s **data pipeline**  
C. On your company’s GitHub Enterprise Server only  
D. Inside your repository’s CI runner

**Correct Answer(s):** B

**Explanation:**  
Prompts (plus any **allowed context**) are sent to the **GitHub Copilot service**, which processes and forwards them to the **selected AI model** following GitHub’s documented **data pipeline** and safeguards. **Org/enterprise policies** (for example, **content/context exclusion**, public code filtering) limit what context can be included.

**Tips and Tricks:**  
- Admins can shape **what Copilot can see** (exclusions) and **how suggestions are governed** (policies).  
- Know the separation: **processing = Copilot service**; **governance = org/enterprise policy**.

> [!IMPORTANT]  
> Review your **organization or enterprise policies** especially **content/context exclusion** to control **which files/repos** may be sent as context and to reinforce confidentiality.

**Source:**  
[How GitHub Copilot handles data (data pipeline)](https://resources.github.com/learn/pathways/copilot/essentials/how-github-copilot-handles-data/) (GitHub)  
[Manage enterprise policies for Copilot](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Get started with GitHub Copilot (overview)](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [065]  
**Does GitHub Copilot train on your private code?**

**Options:**  
A. Yes, always  
B. Yes, unless you disable telemetry  
C. **No, private code, prompts, and completions are not used to train Copilot models**  
D. Only for Enterprise organizations

**Correct Answer(s):** C

**Explanation:**  
GitHub’s trust materials state that **your private code, prompts, and completions are not used to train Copilot’s AI models**. Product **telemetry/metrics** are distinct from **model training** and are governed by documented **data handling** and retention practices.

**Tips and Tricks:**  
- Memorize: **telemetry ≠ training**. Telemetry summarizes **activity**, not code contents for model learning.  
- Enterprise customers can **review policies** and **usage reports** to confirm governance and visibility.

> [!IMPORTANT]  
> For **Business/Enterprise**, **private code and prompts** are **not** used to train the base models. For **individual plans**, training on your data is also **not enabled**.

**Source:**  
[Copilot Trust Center (FAQ)](https://copilot.github.trust.page/) (GitHub)  
[How GitHub Copilot handles data](https://resources.github.com/learn/pathways/copilot/essentials/how-github-copilot-handles-data/) (GitHub)  
[Introduction to GitHub Copilot for Business](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-for-business/) (Microsoft Learn)

**Question:** [066]  
Which statement best describes **telemetry/usage data** for GitHub Copilot?

**Options:**  
A. Copilot collects no usage metrics  
B. Telemetry includes **activity and feature usage** (for example, completions, chat, agents) for **reporting**  
C. Telemetry always includes your source code contents  
D. Telemetry is only available to Enterprise customers

**Correct Answer(s):** B

**Explanation:**  
GitHub documents **Copilot usage metrics** (properties, retention, and exports) that summarize **activity and feature usage** for **reporting** (for example, completions accepted, chat activity). The metrics are designed for **adoption and governance** they are **not** a raw dump of repository code.

**Tips and Tricks:**  
- Use org/enterprise **usage reports** + **audit logs** to correlate **who**, **what**, **when** with **policy outcomes**.  
- Check the **metrics reference** for exact fields and retention windows.

> [!IMPORTANT]  
> **Usage metrics** are for **visibility and governance**, not model learning. They help admins **monitor adoption** and **optimize enablement** without exposing source code contents.

**Source:**  
[Copilot metrics data properties](https://docs.github.com/en/copilot/reference/metrics-data) (GitHub Docs)  
[Copilot usage metrics (what’s included)](https://docs.github.com/en/copilot/reference/copilot-usage-metrics/copilot-usage-metrics) (GitHub Docs)  
[Get started with GitHub Copilot (overview)](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [067]  
Which statement about **AI models in GitHub Copilot** is accurate?

**Options:**  
A. Copilot uses a single fixed model for all features  
B. Copilot supports **multiple AI models** with different capabilities and trade-offs  
C. Copilot models are limited to natural language, not code  
D. Model choice never affects latency or quality

**Correct Answer(s):** B

**Explanation:**  
GitHub provides a **model comparison** showing that Copilot supports **multiple AI models**. Choosing a model affects **quality, relevance, latency, and cost controls** across chat and inline completions. Teams can align the model to task needs (for example, faster feedback loops vs. deeper reasoning).

**Tips and Tricks:**  
- Start with the **recommended defaults**, then **benchmark** for your codebase (accept rates, error fixes, test coverage).  
- Document **model-to-use-case** guidance (e.g., rapid prototyping vs. complex refactors) for consistent team outcomes.

> [!IMPORTANT]  
> **Governance controls** (for example, public code filtering, content/context exclusion, and code referencing) apply **regardless of the model**, separate **model choice** from **policy enforcement**.

**Source:**  
[AI model comparison](https://docs.github.com/en/copilot/reference/ai-models/model-comparison) (GitHub Docs)  
[Copilot features overview](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Get started with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [068]  
What is a **primary benefit of prompt engineering** when using Copilot?

**Options:**  
A. It guarantees license-compliant output  
B. It reduces IDE CPU usage  
C. It improves **clarity and specificity**, leading to **better, more relevant suggestions**  
D. It disables duplication detection

**Correct Answer(s):** C

**Explanation:**  
Clear, structured prompts (problem, constraints, inputs/outputs, examples) **raise suggestion quality** and reduce rework. Iterating, refine, add acceptance criteria, request alternatives, guides Copilot toward the target.

**Tips and Tricks:**  
- Use **role + task + constraints + examples** (“You are a reviewer… Generate parameterized tests… Must handle nulls…”).  
- Ask for **rationales** or **stepwise plans** in Chat to expose assumptions before generating code.

> [!IMPORTANT]  
> Prompt engineering **improves output quality** but does **not change policy**: duplication detection, code referencing, and content/context exclusions still apply.

**Source:**  
[Prompt engineering for Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [069]  
Which is a **common developer use case** for GitHub Copilot?

**Options:**  
A. Replacing your SCM server  
B. **Explaining code or generating unit tests** inside your IDE  
C. Running your CI pipelines  
D. Hosting container registries

**Correct Answer(s):** B

**Explanation:**  
Copilot (Chat and inline completions) assists with **code explanation**, **test generation**, and **error fixing** directly in supported IDEs and on GitHub.com, accelerating comprehension and feedback cycles.

**Tips and Tricks:**  
- For tests, provide **function signatures, edge cases, and expected behaviors** to get higher-coverage scaffolds.  
- Use Chat prompts like **“Explain this function’s complexity”** or **“Generate table-driven tests with boundary cases.”**

> [!IMPORTANT]  
> Copilot **augments** development; it doesn’t replace **code review**, **unit/integration tests**, or **security scanning**, keep your engineering gates.

**Source:**  
[About GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)  
[Copilot features overview](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Introduction to GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) (Microsoft Learn)

**Question:** [070]  
Which GitHub Copilot plan is **included by default** with **GitHub Enterprise Cloud (GHEC)**?

**Options:**  
A. Copilot Enterprise  
B. Copilot Business  
C. **None, Copilot plans are separate add-ons**  
D. Copilot Pro

**Correct Answer(s):** C

**Explanation:**  
Copilot plans are **not bundled** with GHEC by default. During a **GHEC 30-day trial**, enterprises can **enable Copilot Business** for evaluation, then decide on paid licensing afterward.

**Tips and Tricks:**  
- Separate **availability** from **entitlement**. GHEC can use **Copilot Enterprise**, however it still requires a **separate subscription**.  
- Trial language matters, “included during trial” does **not** mean “permanently included.”

> [!IMPORTANT]  
> Use the trial to validate **policy controls, usage reporting, and exclusions** with **Copilot Business**, then size licensing based on adoption and governance needs.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/enterprise-cloud%40latest/copilot/get-started/plans) (GitHub Docs)  
[Subscribing to Copilot for your enterprise, trial details](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-plan/subscribe) (GitHub Docs)  
[Setting up a GHEC trial](https://docs.github.com/en/enterprise-cloud%40latest/enterprise-onboarding/getting-started-with-your-enterprise/setting-up-a-trial-of-github-enterprise) (GitHub Docs)  
[Introduction to GitHub Copilot for Business](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-for-business/) (Microsoft Learn)

**Question:** [071]  
Who benefits most from **GitHub Copilot Free**?

**Options:**  
A. Enterprises that need audit logs and policy controls  
B. **Individuals getting started** with Copilot for **personal use**  
C. Organization admins who need usage reporting  
D. Students or teachers who need Copilot **Pro** at no cost

**Correct Answer(s):** B

**Explanation:**  
**Copilot Free** targets **individual developers** for **personal use** with limited features and no org governance. Education or maintainer benefits unlock **Copilot Pro**, not Free.

**Tips and Tricks:**  
- Match plan to scope, **Free and Pro** are **individual**. **Business and Enterprise** are **organization**.  
- If the scenario mentions **admin controls**, **usage reporting**, or **exclusions**, you are **not** in Copilot Free.

> [!IMPORTANT]  
> Verified **students, teachers, and qualified maintainers** receive **Copilot Pro** at no cost, which is distinct from **Copilot Free**.

**Source:**  
[Individual Copilot plans, Free and Pro](https://docs.github.com/en/copilot/concepts/billing/individual-plans) (GitHub Docs)  
[What is GitHub Copilot](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)  
[Get started with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [072]  
Which statement best describes **Copilot’s context awareness** when generating suggestions?

**Options:**  
A. Copilot always uses the entire repository history  
B. Copilot considers only the file name and comments  
C. Copilot uses **surrounding code**, **current file contents**, and **comments** to shape suggestions  
D. Copilot only considers public code

**Correct Answer(s):** C

**Explanation:**  
Inline suggestions rely on **local editor context**: nearby code, the active file, and your comments or docstrings. On GitHub.com, **repository-aware Chat** for **Copilot Enterprise** can reference broader repo content, improved by **repository indexing**.

**Tips and Tricks:**  
- Think **local first** for inline completions, then add **Enterprise repo context** for Chat on GitHub.com when needed.  
- Keep indexes **fresh** for active repositories to improve Chat answers.

> [!IMPORTANT]  
> Distinguish **context visibility** from **output controls**. **Exclusions** limit what Copilot can see, **code referencing/public-code filters** govern what Copilot may suggest or flag.

**Source:**  
[Code suggestions, how context is used](https://docs.github.com/en/copilot/concepts/completions/code-suggestions) (GitHub Docs)  
[Repository indexing for Copilot Chat](https://docs.github.com/en/enterprise-cloud%40latest/copilot/concepts/context/repository-indexing) (GitHub Docs)  
[Introduction to GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) (Microsoft Learn)

**Question:** [073]  
Does GitHub Copilot **guarantee** that generated code is always correct and secure?

**Options:**  
A. Yes, Copilot guarantees security  
B. Yes, Copilot guarantees correctness  
C. **No, developers must review and test suggestions**  
D. No, but Copilot automatically fixes insecure code

**Correct Answer(s):** C

**Explanation:**  
Copilot provides **non-deterministic suggestions** that can be **incomplete, incorrect, or insecure**. GitHub explicitly expects developers to **review, test, lint, scan, and validate** outputs. Copilot augments development but offers **no guarantee** of correctness or security.

**Tips and Tricks:**  
- Treat Copilot like a **junior pair**, use **code review**, **unit/integration tests**, **SAST/DAST**, and **dependency scanning** before merge.  
- Ask Chat to **explain risks**, **propose tests**, or **refactor**; still verify with your tooling.

> [!IMPORTANT]  
> Compliance-ready workflows keep **human accountability**: enforce **branch protections**, require **reviews**, run **security checks** (e.g., CodeQL, secret scanning), and **track** results in the audit log.

**Source:**  
[Code suggestions (capabilities and limitations)](https://docs.github.com/en/copilot/concepts/completions/code-suggestions) (GitHub Docs)  
[Refactor with GitHub Copilot](https://docs.github.com/en/copilot/tutorials/refactor-code) (GitHub Docs)  
[Get started with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [074]  
What types of prompts or code can be blocked by Copilot’s **safety filters**? *(Choose all that apply.)*

**Options:**  
A. Hate speech or discriminatory language  
B. Sexually explicit content  
C. Code with logical errors  
D. Strong personal opinions in comments

**Correct Answer(s):** A, B

**Explanation:**  
Copilot requests and responses pass through **content safety filters** designed to block **harmful categories** such as **toxicity (hate/discrimination)** and **sexually explicit content**. These protections target **safety and harm**, not general **code correctness** or **style**.

**Tips and Tricks:**  
- If an option names **harmful/explicit** content, it aligns with **safety filtering**.  
- **Logic, style, or quality** issues are addressed by **reviews, tests, linters, and scanners**, not safety filters.

> [!IMPORTANT]  
> Safety filters protect against **harmful categories**. Separately, **public code filtering / code referencing** governs output **similarity** to public code and licensing review; it does not replace safety filtering.

**Source:**  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)  
[Responsible use of Copilot code completion](https://docs.github.com/en/copilot/responsible-use/copilot-code-completion) (GitHub Docs)  
[Get started with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [075]  
In **VS Code**, which built-in action helps you gather logs and diagnostics for Copilot issues?

**Options:**  
A. GitHub Copilot: Export Telemetry  
B. Developer: Open Runtime Console  
C. **GitHub Copilot: Collect Diagnostics**  
D. GitHub Copilot: Reset Extension Cache

**Correct Answer(s):** C

**Explanation:**  
Use the Command Palette action **“GitHub Copilot: Collect Diagnostics”** to gather **environment details and Copilot extension logs** for troubleshooting connectivity, auth, or extension behavior in VS Code. This is the standard first step before escalating.

**Tips and Tricks:**  
- After collecting diagnostics, verify **sign-in**, **proxy/SSL/allowlisting**, and check the **Output → GitHub Copilot** channel for errors.  
- Disable conflicting extensions if symptoms persist.

> [!IMPORTANT]  
> In enterprise environments, confirm that **network egress** to Copilot endpoints is **allowed**; most connection issues trace back to **proxy or firewall** policy.

**Source:**  
[Introduction to GitHub Copilot (VS Code setup and troubleshooting)](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) (Microsoft Learn)  
[About GitHub Copilot Chat (surfaces and setup)](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)

**Question:** [076]  
Which of the following is **not** a valid, current **Copilot plan name**?

**Options:**  
A. Copilot Free  
B. Copilot Pro+  
C. **Copilot Premium**  
D. Copilot Enterprise

**Correct Answer(s):** C

**Explanation:**  
Official plan names include **Copilot Free**, **Copilot Pro / Pro+** (individual), **Copilot Business** (organization), and **Copilot Enterprise** (enterprise). **“Copilot Premium”** is **not** an official plan name.

**Tips and Tricks:**  
- Always verify plan names on the **Plans** page and **individual plans** pages before answering.  
- Distractors often use **legacy- or enterprise-sounding** labels that are not in GitHub’s taxonomy.

> [!IMPORTANT]  
> Map by **scope**: **Free/Pro/Pro+ = individual**, **Business/Enterprise = organization**. If a name does not fit this taxonomy, treat it as a distractor.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Individual Copilot plans (Free, Pro, Pro+)](https://docs.github.com/en/copilot/concepts/billing/individual-plans) (GitHub Docs)  
[Introduction to GitHub Copilot for Business](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-for-business/) (Microsoft Learn)

**Question:** [077]  
Where is GitHub Copilot **not available**?

**Options:**  
A. GitHub Enterprise Cloud  
B. GitHub.com  
C. **GitHub Enterprise Server (GHES)**  
D. Visual Studio Code

**Correct Answer(s):** C

**Explanation:**  
GitHub documents that **Copilot is not available for self-hosted GitHub Enterprise Server (GHES)**. Copilot is provided as a **cloud service** for **GitHub Enterprise Cloud (GHEC)** organizations, **GitHub.com**, and **supported IDEs** such as **VS Code**, **Visual Studio**, and **JetBrains**.

**Tips and Tricks:**  
- If a scenario mentions **GHES** or **self-hosted Enterprise Server**, the safe mapping is **not supported**.  
- If you need private network controls, evaluate **Copilot Enterprise** on **GHEC** with **enterprise proxy** configuration, not GHES.

> [!IMPORTANT]  
> **Self-hosted GHES ≠ supported** for Copilot. To use Copilot with enterprise controls, choose **GHEC** and the appropriate Copilot plan.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[GitHub Copilot features, availability](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Introduction to GitHub Copilot for Business](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-for-business/) (Microsoft Learn)

**Question:** [078]  
Which Copilot **admin control** limits what content the models can access as **input context**?

**Options:**  
A. Code referencing  
B. **Content exclusion**  
C. Prompt engineering  
D. Telemetry retention

**Correct Answer(s):** B

**Explanation:**  
**Content exclusion** lets **enterprise owners**, **organization owners**, and **repository administrators** prevent specific **repositories, paths, file types, or patterns** from being used as **context** by Copilot. It is available on **Copilot Business** and **Copilot Enterprise**. Users with **Maintain** can typically **view** but not **edit** these settings.

**Tips and Tricks:**  
- Think **“what Copilot can see”** equals **Content exclusion**.  
- Think **“what Copilot may show”** equals **Code referencing** or **public-code filtering**.

> [!IMPORTANT]  
> Map controls cleanly. **Visibility control = Content exclusion** (inputs). **Similarity or attribution control = Code referencing / public-code filter** (outputs). Use both for defense-in-depth.

**Source:**  
[Exclude content from GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Managing policies for Copilot in your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/manage-policies) (GitHub Docs)  
[Introduction to GitHub Copilot for Business](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-for-business/) (Microsoft Learn)

**Question:** [079]  
When **matching public code** controls are enabled, about how much surrounding code does Copilot compare to detect matches?

**Options:**  
A. ~50 characters  
B. **~150 characters**  
C. ~300 characters  
D. The entire file

**Correct Answer(s):** B

**Explanation:**  
**Code referencing** checks a suggestion and **about 150 characters of surrounding code** against public GitHub code to detect close matches. Admins or users can **block** matched suggestions entirely, or **allow** them while **showing references** to the public source for review.

**Tips and Tricks:**  
- Use **block** for stricter IP posture, or **allow + references** for informed review and attribution.  
- Pair with **Content exclusion** to control **inputs**, then use **Code referencing** to govern **outputs**.

> [!IMPORTANT]  
> **Enterprise policy enforcement** can make code-referencing settings **mandatory** across organizations. **Enterprise-enforced** rules **override** org or user preferences.

**Source:**  
[Find matching public code in suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  
[Copilot code referencing, concept](https://docs.github.com/en/copilot/concepts/completions/code-referencing) (GitHub Docs)  
[Manage Copilot policies (account, org, enterprise)](https://docs.github.com/en/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)

**Question:** [080]  
When an **enterprise policy** enforces a Copilot setting (for example, “block matching public code”), what can organizations do?

**Options:**  
A. Override it at the organization level  
B. Override it at the repository level  
C. **Not override it, enterprise-enforced policies take precedence**  
D. Override it for public repos only

**Correct Answer(s):** C

**Explanation:**  
In **GitHub Enterprise Cloud**, **enterprise-enforced Copilot policies** (for example, “block matching public code”) **cannot be loosened** by organizations or repositories. Lower scopes must comply; they can only add **stricter** controls, not weaken an enforced setting.

**Tips and Tricks:**  
- Read the verb: **“enforce” = no override**; **“set default” = org may adjust** within bounds.  
- Use enterprise policies to standardize **IP posture** (e.g., code referencing), **features/models**, and **chat surfaces** across all orgs.

> [!IMPORTANT]  
> **Policy hierarchy**: **Enterprise** (enforced/defaults) → **Organization** (within enterprise bounds) → **Repository** (granular controls like **Content exclusion**). **Enterprise enforcement wins**.

**Source:**  
[Managing policies for Copilot in your organization](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/administer-copilot/manage-for-organization/manage-policies) (GitHub Docs)  
[Enforcing policies for GitHub Copilot in your enterprise](https://docs.github.com/en/enterprise-cloud%40latest/admin/enforcing-policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-copilot-in-your-enterprise) (GitHub Docs)  
[Manage enterprise policies for Copilot](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Introduction to GitHub Copilot Enterprise](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/) (Microsoft Learn)

**Question:** [081]  
Is **GitHub Copilot available in the command line**, and what does it help with?

**Options:**  
A. No, Copilot is IDE-only  
B. **Yes, via Copilot in the CLI for drafting/explaining commands**  
C. Yes, only for Enterprise plans  
D. Yes, if GHES is enabled

**Correct Answer(s):** B

**Explanation:**  
**Copilot CLI** brings Copilot to the **terminal**, helping you **draft/explain shell and Git commands**, refine flags, and learn usage interactively. Availability depends on your **Copilot plan** and **org policy**; **GHES** is **not supported** for Copilot.

**Tips and Tricks:**  
- If CLI access fails in enterprises, check **org/enterprise Copilot CLI policy**, **auth**, and **proxy/allowlisting**.  
- Use CLI for quick command scaffolds; use IDE Chat for **code reasoning** and inline for **cursor-near edits**.

> [!IMPORTANT]  
> Copilot surfaces (IDE, GitHub.com, **CLI**) are **policy-controllable**. Ensure **CLI is enabled** at your org/enterprise level if access is restricted.

**Source:**  
[Using GitHub Copilot CLI](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/use-copilot-cli) (GitHub Docs)  
[GitHub Copilot CLI (feature page)](https://github.com/features/copilot/cli/) (GitHub)  
[Copilot CLI 101: how to use it from the terminal](https://github.blog/ai-and-ml/github-copilot/github-copilot-cli-101-how-to-use-github-copilot-from-the-command-line/) (GitHub Blog)

**Question:** [082]  
How does **Content exclusion** differ from a **.gitignore** file?

**Options:**  
A. Both prevent files from being pushed to GitHub  
B. **Content exclusion limits what Copilot can use as input context; .gitignore controls what Git tracks**  
C. Content exclusion blocks outputs similar to excluded files  
D. .gitignore disables Copilot on ignored files

**Correct Answer(s):** B

**Explanation:**  
**Content exclusion** is a **Copilot governance control** that **prevents specified repos/paths/file types/patterns from being used as context**. It does **not** change Git behavior. **.gitignore** is a **Git setting** that influences **what files Git tracks/commits** and has **no direct effect** on Copilot context.

**Tips and Tricks:**  
- For **inputs**, use **Content exclusion** (and audit its changes).  
- For **outputs**, use **code referencing/public-code filter** to block or reference matches to public code.

> [!IMPORTANT]  
> Memorize the mapping: **Context boundary = Content exclusion**; **SCM tracking = .gitignore**; **Output similarity = Code referencing**. Use **both** exclusion and referencing for defense-in-depth.

**Source:**  
[Exclude content from Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Content exclusion (concepts and limitations)](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Git .gitignore documentation](https://git-scm.com/docs/gitignore) (Git SCM Docs)

**Question:** [083]  
At which **scopes** can **code referencing / “Suggestions matching public code”** be configured?

**Options:**  
A. Only at the IDE level  
B. **At the individual account level and via organization/enterprise policies**  
C. Only at the repository level  
D. Only at the enterprise level

**Correct Answer(s):** B

**Explanation:**  
**Code referencing** (also called **Suggestions matching public code**) can be set by **individual users** and governed by **organization or enterprise** administrators. When an **enterprise policy** enforces a setting (for example, **block**), it **overrides** org and user preferences; when it sets a **default**, lower scopes may adjust within allowed bounds.

**Tips and Tricks:**  
- Think **personal preference** at the **account** level, and **standardization** at **org/enterprise**.  
- Use **block** for strict IP posture, or **allow with references** to review the public source and license before use.

> [!IMPORTANT]  
> Pair **code referencing** (controls **outputs** similar to public code) with **content/context exclusion** (controls **inputs** Copilot can see) for defense in depth.

**Source:**  
[Find matching public code in suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  
[Manage Copilot policies (account, organization, enterprise)](https://docs.github.com/en/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)  
[Manage enterprise policies for Copilot](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Introduction to GitHub Copilot Enterprise](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/) (Microsoft Learn)

**Question:** [084]  
If an **enterprise policy** restricts Copilot to a specific **set of AI models/surfaces**, what can organizations do?

**Options:**  
A. Choose any model/surface regardless of enterprise policy  
B. **Configure org settings only within the enterprise-allowed set**  
C. Override enterprise policy at the repo level  
D. Disable enterprise policy from the org settings page

**Correct Answer(s):** B

**Explanation:**  
**Enterprise owners** can **enforce** or **preset** Copilot policies (for example, allowed **models** and **surfaces** like Chat/Edits/CLI). When **enforced**, organizations may only configure **within the allowed set**; repositories inherit and **cannot weaken** enterprise posture.

**Tips and Tricks:**  
- Read verbs carefully: **enforce = no override**, **default = orgs may refine** within bounds.  
- Keep a short policy matrix (enterprise vs. org vs. repo) to avoid accidental misconfiguration.

> [!IMPORTANT]  
> **Hierarchy wins:** **Enterprise** (enforced/defaults) → **Organization** (configure within bounds) → **Repository** (granular controls such as **Content exclusion**). Enforced enterprise policy **takes precedence**.

**Source:**  
[Manage enterprise policies for Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Administer Copilot for your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization) (GitHub Docs)  
[Introduction to GitHub Copilot Enterprise](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/) (Microsoft Learn)

**Question:** [085]  
Which GitHub Copilot capability can **autonomously make multi-step code changes** and open a **pull request** for review?

**Options:**  
A. Copilot Chat inline replies  
B. **Copilot coding agent**  
C. Content exclusion  
D. Code referencing / matching public code

**Correct Answer(s):** B

**Explanation:**  
The **Copilot coding agent** can plan and execute **multi-step workflows** (spanning files and, where permitted, terminal actions) and then **open a pull request (PR)** for review. This differs from **Copilot Edits** in VS Code: **Edit mode** and **Agent mode** focus on local, editor-driven changes, you still commit and raise PRs via your normal flow.

**Tips and Tricks:**  
- Use the **coding agent** when you want **task-level autonomy** that culminates in a **PR** (e.g., “implement feature X across services”).  
- Use **Copilot Edits (Agent mode)** for **multi-step local refactors** with tight human control; use **Edits (Edit mode)** for **surgical, file-scoped** changes.  
- Keep **branch protections**, **reviews**, and **security checks** enforced, agent PRs go through the same gates.

> [!IMPORTANT]  
> Autonomy ≠ bypassing governance. Pair the **coding agent** with **code review**, **tests**, **CodeQL/secret scanning**, and **policy controls** (e.g., content exclusion, public-code filtering) to maintain compliance.

**Source:**  
[Copilot features (coding agent and edits)](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Getting started with prompts for Copilot Chat](https://docs.github.com/en/copilot/get-started/getting-started-with-prompts-for-copilot-chat) (GitHub Docs)  
[Get started with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)

**Question:** [086]  
Which statement about **Copilot Knowledge Bases** is accurate?

**Options:**  
A. Available on all Copilot plans  
B. Available on Business and Enterprise  
C. **Enterprise-only: use curated docs as chat context on GitHub.com/VS Code**  
D. Available on Pro+ and Enterprise

**Correct Answer(s):** C

**Explanation:**  
**Copilot Knowledge Bases** are an **Enterprise-only** capability that lets you **curate organization-approved documentation** and **ground Copilot Chat** (on GitHub.com and VS Code) in those sources for higher-quality answers.

**Tips and Tricks:**  
- Treat Knowledge Bases as **approved context** distinct from raw repo context; curate concise, authoritative docs to reduce noise.  
- Combine with **repository indexing** to improve retrieval quality for repo content.

> [!IMPORTANT]  
> GitHub has communicated a **transition from Knowledge Bases toward Copilot Spaces**. Check current docs for **availability and migration guidance** before architecting long-term solutions.

**Source:**  
[Copilot features overview](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[About GitHub Copilot Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/set-up/set-up-for-enterprise) (GitHub Docs)  
[Introduction to GitHub Copilot Enterprise](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/) (Microsoft Learn)

**Question:** [087]  
At which **scopes** can **code referencing / “Suggestions matching public code”** be configured?

**Options:**  
A. Only in IDE settings  
B. **At the individual account level and via organization/enterprise policies**  
C. Only at the repository level  
D. Only at the enterprise level

**Correct Answer(s):** B

**Explanation:**  
**Code referencing** can be set by **individual users** and governed by **organization/enterprise policies**. If an **enterprise policy** enforces a value (for example, **block**), it **overrides** org and user preferences; if it sets a **default**, lower scopes may refine within bounds.

**Tips and Tricks:**  
- Think **personal preference** at **account** scope and **standardization** at **org/enterprise** scope.  
- Use **block** for strict IP posture; **allow with references** to review the public source and license before use.

> [!IMPORTANT]  
> Pair **code referencing** (controls **outputs** similar to public code) with **content/context exclusion** (controls **inputs** Copilot can see) for defense in depth.

**Source:**  
[Find matching public code in suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  
[Manage Copilot policies (account, organization, enterprise)](https://docs.github.com/en/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)  
[Manage enterprise policies for Copilot](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Introduction to GitHub Copilot Enterprise](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/) (Microsoft Learn)

**Question:** [088]  
Which **targets** can be specified in **Content exclusion** rules?

**Options:**  
A. Only repositories  
B. Repositories and branches  
C. **Repositories, paths/directories, file types, and pattern-based rules**  
D. Only file extensions

**Correct Answer(s):** C

**Explanation:**  
**Content exclusion** supports **multiple target types**: entire **repositories**, specific **paths/directories**, **file types** (extensions), and **pattern/glob-based** selectors. This lets admins draw precise **context boundaries** without disabling Copilot for the whole codebase.

**Tips and Tricks:**  
- Start **narrow** (secrets, credentials folders, regulated data paths), then widen if needed.  
- Keep an auditable change log for exclusion rules to aid incident response.

> [!IMPORTANT]  
> Exclusion limits **inputs**; combine with **code referencing/public-code filtering** to govern **outputs** and reduce IP/licensing risk.

**Source:**  
[Exclude content from Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Content exclusion (concepts and limitations)](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Introduction to GitHub Copilot for Business](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-for-business/) (Microsoft Learn)

**Question:** [089]  
Which statement best describes **repository-aware Copilot Chat on GitHub.com**?

**Options:**  
A. It is available to all plans by default  
B. **It’s an Enterprise capability that lets chat reference repository files/docs on GitHub.com**  
C. It runs offline using the IDE only  
D. It requires GHES

**Correct Answer(s):** B

**Explanation:**  
**Copilot Enterprise** enables **GitHub.com repository-aware Chat**, allowing authorized users to **reference and reason over repository files and docs** in the browser. This goes beyond **IDE-local context** and benefits from **repository indexing**.

**Tips and Tricks:**  
- If a scenario says “**chat with repo files on GitHub.com**,” choose **Enterprise**.  
- Keep indexes **fresh** to improve retrieval quality and answer accuracy.

> [!IMPORTANT]  
> Availability ≠ inclusion: it’s an **Enterprise** capability for **GHEC** orgs and is **not** bundled with individual or Business plans.

**Source:**  
[About GitHub Copilot Enterprise](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/set-up/set-up-for-enterprise) (GitHub Docs)  
[Repository indexing for Copilot Chat](https://docs.github.com/en/enterprise-cloud%40latest/copilot/concepts/context/repository-indexing) (GitHub Docs)  
[Copilot features overview](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Introduction to GitHub Copilot Enterprise](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot-enterprise/) (Microsoft Learn)

**Question:** [090]  
In **VS Code**, where do you enable or disable **Copilot inline suggestions** globally or per language?

**Options:**  
A. File → Preferences → Keyboard Shortcuts → GitHub  
B. **Settings → Extensions → GitHub Copilot (Inline Suggest: Enable / Enable for [Language])**  
C. Source Control → Git → Copilot  
D. Terminal → Integrated → Copilot

**Correct Answer(s):** B

**Explanation:**  
In VS Code, Copilot’s inline behavior is controlled in **Settings → Extensions → GitHub Copilot**. You can toggle **Inline Suggest: Enable** globally and configure **per-language** enablement, letting teams keep Copilot active generally while restricting specific stacks.

**Tips and Tricks:**  
- Pair **global on + targeted per-language off** for sensitive templates (for example, **IaC**, policy code).  
- If suggestions don’t appear, confirm **sign-in**, **workspace trust**, and check **Output → GitHub Copilot** for errors.

> [!IMPORTANT]  
> Editor settings optimize ergonomics; **enterprise/org policies** still set the guardrails (features/models, exclusions, public code filter).

**Source:**  
[Set up GitHub Copilot in VS Code](https://docs.github.com/en/copilot/how-tos/set-up/install-copilot-extension?tool=vscode) (GitHub Docs)  
[Code suggestions (inline)](https://docs.github.com/en/copilot/concepts/completions/code-suggestions) (GitHub Docs)  
[Get started with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/get-started-github-copilot/) (Microsoft Learn)