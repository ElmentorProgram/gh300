# Detailed Practice Test 02 - Answer Sheet & Explanation

**Question:** [031]  
Which GitHub Copilot plan is available at no cost to verified students, teachers, and maintainers of popular open-source projects?

**Options:**  
A. GitHub Copilot Free  
B. GitHub Copilot Pro  
C. GitHub Copilot Business  
D. GitHub Copilot Enterprise

**Correct Answer(s):** B  

**Explanation:**  
GitHub states that **verified** **students**, **teachers**, and **open-source maintainers** can get **Copilot Pro** for free. This is documented on the Copilot plans and licensing pages and the “Get free access” how-to. **The no-cost benefit grants Copilot Pro after verification as a student, teacher, or eligible open-source maintainer; activation is done from Account, then Billing.** **Copilot Free** is a separate, limited tier and is **not** the education/maintainer benefit.

**Tips and Tricks:**  
- If **license** is needed for a **verified** **student/teacher/maintainer**, choose **Copilot Pro** (not **Free**). If the stem mentions **org controls**, **SSO**, or **audit logs**, that points to **Business/Enterprise**, not this question.  
- When a question contrasts **Copilot Free** and **Copilot Pro**, remember the **verification** requirement aligns with **Pro at no cost**; without verification, users remain on **Free** with **limited features**.

> [!IMPORTANT]  
> GH-300 items often check whether you can separate **Copilot Pro’s free eligibility** from other plans. The free offer applies only to **verified** **students**, **teachers**, and **maintainers** of popular open-source projects. Confusing it with **Copilot Free** or organizational plans like **Business/Enterprise** is a common mistake.

**Source:**  
[Getting free access to GitHub Copilot Pro](https://docs.github.com/en/copilot/how-tos/manage-your-account/get-free-access-to-copilot-pro) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Getting started with a Copilot plan](https://docs.github.com/en/copilot/how-tos/manage-your-account/get-started-with-a-copilot-plan) (GitHub Docs)  
[Use GitHub Copilot Free in Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-free-plan) (Microsoft Learn)

**Question:** [032]  
Which GitHub Copilot plan is designed for organizations that require **license management**, **policy controls**, and **usage reporting** but do not need **enterprise integrations**?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B  

**Explanation:**  
The **GitHub Copilot Business** plan targets organizations that need **centralized license management**, **policy control**, and **usage reporting**. It is positioned below **Copilot Enterprise** for teams that do **not** require **enterprise integrations**. **Note:** Copilot **Business includes audit logs** for organizational visibility; “do not need enterprise integrations” refers to features beyond Business, not to the absence of audit logs.

**Tips and Tricks:**  
- Look for keywords like **organization**, **licenses**, **policies**, **usage reporting**  these align with **Copilot Business**.  
- If the stem highlights **SSO**, **enterprise-wide integrations**, or **advanced governance** across multiple orgs, that indicates **Copilot Enterprise** instead.

> [!IMPORTANT]  
> **Copilot Business** provides **policy controls**, **content exclusion**, **usage reporting**, and **audit logs** for organizations. Choose **Enterprise** only when the scenario requires **enterprise-level integrations** and broader governance beyond an individual organization.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Reviewing audit logs for GitHub Copilot Business](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)  
[GitHub Copilot policies to control availability of features and models](https://docs.github.com/en/copilot/concepts/policies) (GitHub Docs)  
[Content exclusion for GitHub Copilot](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)

**Question:** [033]  
Which GitHub Copilot plan provides enterprise features like audit logs, SSO integration, and advanced compliance capabilities?

**Options:**  
A. GitHub Copilot Free  
B. GitHub Copilot Pro  
C. GitHub Copilot Business  
D. GitHub Copilot Enterprise

**Correct Answer(s):** D

**Explanation:**  
**GitHub Copilot Enterprise** includes **enterprise-grade integrations**, **SSO** via your organization’s or enterprise account’s identity provider, and **advanced policy and compliance controls** across organizations. **Copilot Business** also has **audit logs**, the Enterprise tier adds broader governance and enterprise-level capabilities.

**Tips and Tricks:**  
- If the stem highlights **SSO with an IdP**, **enterprise compliance reporting**, or **centralized enterprise policies**, choose **Copilot Enterprise**.  
- If the stem focuses only on **license management**, **policy controls**, and **usage reporting** at the org level, that fits **Copilot Business**, not Enterprise.  
- **SSO is a GitHub Enterprise or organization capability, not exclusive to any Copilot plan**, in exams, SSO plus enterprise-wide governance usually implies **Copilot Enterprise**, but SSO itself belongs to the GitHub Enterprise layer.

> [!IMPORTANT]  
> Pick **Copilot Enterprise** when the scenario requires **enterprise-wide identity integration (SSO)** and **advanced governance**. **Audit logs** exist in **Business** too, so look for **SSO** and **enterprise compliance** to distinguish **Enterprise** from **Business**.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choosing your enterprise's plan for GitHub Copilot](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[Managing policies and features for GitHub Copilot in your enterprise](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[About authentication with single sign-on](https://docs.github.com/en/enterprise-cloud%40latest/authentication/authenticating-with-single-sign-on/about-authentication-with-single-sign-on) (GitHub Docs)  
[Reviewing audit logs for GitHub Copilot Business](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)

**Question:** [034]  
Which GitHub Copilot feature lets developers ask **natural-language** questions about code, get **explanations**, and generate suggestions directly within **supported IDEs**?

**Options:**  
A. GitHub Copilot Chat  
B. GitHub Copilot coding agent  
C. Context exclusions  
D. GitHub Copilot Enterprise

**Correct Answer(s):** A

**Explanation:**  
**GitHub Copilot Chat** is the conversational interface for **natural-language** Q&A about code, **explanations**, troubleshooting, and task guidance inside **supported IDEs** and on GitHub. It supports prompts such as **“explain this code,” “generate unit tests,” “why is this failing,”** and suggests relevant fixes and examples.

**Tips and Tricks:**  
- Prompts about **explaining code**, **writing tests**, or **fixing errors in the IDE** indicate **Copilot Chat**, not the **coding agent** which focuses on multi step task execution, not **Enterprise** which is a plan, and not **context exclusions** which are policy controls.  
- Think surfaces, when interaction happens **in the IDE or on GitHub**, choose **Copilot Chat**.

> [!IMPORTANT]  
> **Copilot Chat** spans multiple surfaces including **VS Code**, **Visual Studio**, **JetBrains IDEs**, and **GitHub.com**. If the scenario is interactive Q&A about code in a developer environment, select **Copilot Chat**.

**Source:**  
[About GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)  
[Ask GitHub Copilot questions in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[GitHub Copilot features](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Introduction to GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) (Microsoft Learn)

**Question:** [035]  
Which GitHub Copilot feature helps organizations prevent **sensitive data** such as **secrets**, **credentials**, or **proprietary code** from being used as context in AI suggestions, available on **Copilot Business** and **Copilot Enterprise**?

**Options:**  
A. GitHub Copilot Chat  
B. Content exclusion  
C. GitHub Copilot Pro  
D. Coding agent

**Correct Answer(s):** B

**Explanation:**  
**Content exclusion** lets administrators define files, repositories, or patterns that Copilot must not use as context during generation, protecting **secrets**, **credentials**, and **proprietary code**. It is available for **Copilot Business** and **Copilot Enterprise**.

**Tips and Tricks:**  
- Map **policy control that limits model context** to **Content exclusion**, not **Chat**, not **Pro**, not **coding agent**.  
- If the stem emphasizes **preventing internal code or secrets from influencing suggestions**, choose **Content exclusion**.

> [!IMPORTANT]  
> **Content exclusion** controls **what Copilot can see**, not the general ability to generate code. Use it with **organization or enterprise policies** to reduce inadvertent data exposure.

**Source:**  
[Content exclusion for GitHub Copilot](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Configure content exclusion for your organization](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[GitHub Copilot policies to control availability of features and models](https://docs.github.com/en/copilot/concepts/policies) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)

**Question:** [036]  
Which GitHub Copilot plan is most suitable for enterprises that need centralized management, audit logs, SSO, and advanced compliance reporting?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**GitHub Copilot Enterprise** is designed for organizations requiring enterprise-grade **compliance**, **governance**, and **security**. For **GitHub Enterprise Cloud** organizations with **SSO** configured, Copilot Enterprise **uses your org’s SSO** for access control, and surfaces **Copilot events in audit activity**, while adding **enterprise integrations** and **centralized management**. **Premium Support** with **SLAs** is a **separate, paid** offering for GitHub Enterprise customers, it is **not bundled** with Copilot Enterprise.

**Tips and Tricks:**  
- **Business** includes **policy controls**, **usage reporting**, and **audit logs**, choose **Enterprise** when scenarios require **enterprise integrations**, **GitHub.com repository-aware chat**, or **organization-wide governance**.  
- Treat **SSO** as a **GitHub Enterprise Cloud organization capability** that Copilot Enterprise **relies on**, not a Copilot-plan-exclusive feature.  
- Remember that **Premium Support with SLAs** is **purchased separately** for Enterprise customers, not included in any Copilot plan.

> [!IMPORTANT]  
> Map cues like **enterprise integrations**, **SSO in an Enterprise Cloud org**, **advanced compliance and governance**, and **centralized enterprise control** to **Copilot Enterprise**. Distinguish tiers by noting that **audit logs exist in Business**, while **Enterprise** layers on **enterprise-only integrations** and **GitHub.com context features**.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Reviewing audit logs for GitHub Copilot Business](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[GitHub Copilot Enterprise is now generally available](https://github.blog/news-insights/product-news/github-copilot-enterprise-is-now-generally-available/) (GitHub Blog)

**Question:** [037]  
Which GitHub Copilot plan allows organization administrators to manage **licenses**, configure **content (context) exclusion** policies, and view **usage reporting**?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B

**Explanation:**  
**GitHub Copilot Business** provides **organization-level administration** including **license assignments**, **content exclusion** policies to control what Copilot can use as context, and **usage reporting** for visibility across the org. Relevant **Copilot events appear in the organization audit log**, and Business does **not** include Enterprise-only integrations such as **SSO configuration** (an Enterprise Cloud org capability that Copilot Enterprise uses).

**Tips and Tricks:**  
- “**Org admin controls**,” “**license management**,” “**usage reporting**,” and “**content exclusion**” point to **Copilot Business**.  
- **Audit logs** exist for **Business**; choose **Enterprise** when scenarios add **enterprise-only integrations** (for example, SSO used by Enterprise Cloud orgs) and **GitHub.com repository-aware Chat**.

> [!IMPORTANT]  
> Map **policy enforcement + org reporting** to **Business**. Escalate to **Enterprise** only when the stem requires **enterprise integrations** and **organization-level identity (SSO) usage** in **Enterprise Cloud**.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Reviewing audit logs for GitHub Copilot Business](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)  
[Configure content exclusion for Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)

**Question:** [038]  
Which GitHub Copilot plan provides enterprise-grade **integrations** and **compliance** capabilities, and can be paired with **GitHub Premium Support (SLAs) as a separate purchase**?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**GitHub Copilot Enterprise** adds **enterprise integrations**, **audit/compliance features**, and **organization-wide governance** for GitHub Enterprise Cloud orgs. Note that **GitHub Premium Support with SLAs is a separate, paid offering** that some enterprises purchase alongside Copilot Enterprise; it is **not bundled** with any Copilot plan.

**Tips and Tricks:**  
- Cues like **enterprise integrations**, **compliance**, **governance**, or **GitHub.com repo-aware Chat** point to **Copilot Enterprise**.  
- **Business** covers **org controls, usage reporting, and audit logs**; **Pro** is **individual** only.

> [!IMPORTANT]  
> When you see **service commitments (SLAs)**, think **optional GitHub Premium Support** purchased by **Enterprise** customers, not a Copilot plan feature.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[GitHub Copilot licenses](https://docs.github.com/en/billing/concepts/product-billing/github-copilot-licenses) (GitHub Docs)  
[GitHub Copilot Enterprise is now generally available](https://github.blog/news-insights/product-news/github-copilot-enterprise-is-now-generally-available/) (GitHub Blog)

**Question:** [039]  
Which GitHub Copilot plan provides **repository-level context awareness on GitHub.com**, allowing Copilot Chat to reference and understand repository files directly?

**Options:**  
A. GitHub Copilot Business  
B. GitHub Copilot Pro  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**Copilot Enterprise** enables **repo-aware Chat on GitHub.com**, so it can **summarize, explain, and reference** your organization’s repository code and docs beyond IDE-only context.

**Tips and Tricks:**  
- Phrases like **“Chat with repository files on GitHub.com”** or **“org-level repo context”** map to **Enterprise**.  
- **Pro** and **Business** focus on **IDE** surfaces without **GitHub.com repo-aware** context.

> [!IMPORTANT]  
> **Repo-aware Copilot Chat** is an **Enterprise-only** differentiator, separate from administrative controls already present in **Business**.

**Source:**  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)  
[GitHub Copilot Enterprise is now generally available](https://github.blog/news-insights/product-news/github-copilot-enterprise-is-now-generally-available/) (GitHub Blog)

**Question:** [040]  
Which GitHub Copilot plan includes enterprise-grade **integrations** and **compliance** capabilities, while **GitHub Premium Support with SLAs** can be purchased **separately** if needed?

**Options:**  
A. GitHub Copilot Business  
B. GitHub Copilot Pro  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**GitHub Copilot Enterprise** adds **enterprise integrations**, **audit/compliance features**, and **organization-wide governance** for GitHub Enterprise Cloud orgs. Note that **GitHub Premium Support with SLAs** is a **separate, paid** offering for Enterprise customers and is **not bundled** with any Copilot plan.

**Tips and Tricks:**  
- Cues like **enterprise integrations**, **compliance**, **governance**, or **GitHub.com repo-aware Chat** point to **Copilot Enterprise**.  
- **Business** covers **org controls, usage reporting, and audit logs**; **Pro** is **individual** only.

> [!IMPORTANT]  
> Treat **Premium Support (SLAs)** as an **org-level support purchase**, independent of Copilot plans. Use **Copilot Enterprise** for enterprise integrations and GitHub.com **repository-aware** Chat, and layer **Premium Support** only if your org requires SLA-backed response targets.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[GitHub Copilot licenses](https://docs.github.com/en/billing/concepts/product-billing/github-copilot-licenses) (GitHub Docs)  
[GitHub Copilot Enterprise is now generally available](https://github.blog/news-insights/product-news/github-copilot-enterprise-is-now-generally-available/) (GitHub Blog)

**Question:** [041]  
Which GitHub Copilot plan provides **usage reporting** and **organizational policy controls** without enterprise-only integrations?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B

**Explanation:**  
**GitHub Copilot Business** offers **usage reporting**, **policy enforcement**, **license management**, and **audit logs** at the organization level, but **does not** include Enterprise-only integrations (for example, GitHub.com **repo-aware** Chat).

**Tips and Tricks:**  
- Phrases like **admin controls**, **policy/usage governance**, **license assignments**, and **audit visibility** align with **Business**.  
- Choose **Enterprise** when scenarios add **enterprise integrations** or **GitHub.com repository-aware** Chat.

> [!IMPORTANT]  
> Use **Business** to standardize Copilot controls across teams (**policies, usage insights, audit events**) without introducing enterprise integration complexity. Reserve **Enterprise** for orgs that need **GitHub.com context features** and broader integration surfaces.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Reviewing audit logs for GitHub Copilot Business](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)  
[GitHub Copilot licenses](https://docs.github.com/en/billing/concepts/product-billing/github-copilot-licenses) (GitHub Docs)

**Question:** [042]  
Which GitHub Copilot plan integrates with enterprise identity providers to support **Single Sign-On (SSO)**?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**Copilot Enterprise** works with a **GitHub Enterprise Cloud** organization’s configured **IdP/SSO** for centralized access control and adds broader enterprise governance features.

**Tips and Tricks:**  
- **SSO + enterprise governance** → **Copilot Enterprise**.  
- **Business** focuses on org controls and reporting for Team or Enterprise Cloud orgs; **Pro** is individual.

> [!IMPORTANT]  
> Treat **SSO** as an **organization capability** of **Enterprise Cloud**. **Copilot Enterprise relies on your org’s SSO**, it does not “include” SSO as a Copilot plan feature. This distinction prevents over-attributing identity features to Copilot itself.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[GitHub Copilot Enterprise is now generally available](https://github.blog/news-insights/product-news/github-copilot-enterprise-is-now-generally-available/) (GitHub Blog)

**Question:** [043]  
Which GitHub Copilot plan is best suited for **individual developers** who want AI-assisted coding features **without** organizational controls or policy management?

**Options:**  
A. GitHub Copilot Business  
B. GitHub Copilot Enterprise  
C. GitHub Copilot Pro  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**GitHub Copilot Pro** is the **individual** plan, providing AI-assisted coding (including **Copilot Chat**) for a single user and **no** organization-level features like **policy controls**, **usage reporting**, or **license administration** (these exist in **Business/Enterprise**).

**Tips and Tricks:**  
- Stems with **“single developer,” “personal subscription,” “no org controls”** → **Copilot Pro**.  
- Any mention of **org policy**, **license management**, **SSO/audit integrations**, or **usage reporting** shifts the answer to **Business**/**Enterprise**.

> [!IMPORTANT]  
> Keep **plan scope** straight: **Pro** = powerful AI for one developer; **Business/Enterprise** = admin/governance for organizations (policies, reporting, identity, audit).

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[GitHub Copilot licenses](https://docs.github.com/en/billing/concepts/product-billing/github-copilot-licenses) (GitHub Docs)  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)

**Question:** [044]  
Which GitHub Copilot plan(s) provide **organization-level usage reporting**? *(Choose all that apply.)*

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B, C

**Explanation:**  
**Usage reporting** is an **organization** capability available with **Copilot Business** and **Copilot Enterprise**. **Pro** and **Free** do not expose org-wide metrics.

**Tips and Tricks:**  
- Cues like **“admin visibility,” “org metrics,” “reporting”** point to **Business/Enterprise**, not **Pro/Free**.  
- Use reporting to monitor **adoption**, **policy impact**, and guide **enablement**.

> [!IMPORTANT]  
> **Org features live at org tiers.** Map **usage reporting** to **Business/Enterprise**; individuals won’t have admin dashboards.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[GitHub Copilot licenses](https://docs.github.com/en/billing/concepts/product-billing/github-copilot-licenses) (GitHub Docs)  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)

**Question:** [045]  
Which GitHub Copilot plan introduces **content (context) exclusion** policies for admins **without** requiring enterprise-only integrations?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B

**Explanation:**  
**Copilot Business** lets admins set **content/context exclusions** (for example, block specific repos or file paths from being used as context) and combines this with **policy** and **usage reporting**—all **without** enterprise-only integrations.

**Tips and Tricks:**  
- Think **“policy controls + exclusions + reporting”** → **Business**.  
- **Enterprise** also supports exclusions, but adds **enterprise integrations** and **GitHub.com repo-aware Chat**.

> [!IMPORTANT]  
> Use exclusions to reduce **sensitive data exposure** in suggestions by constraining what Copilot can **see** during generation.

**Source:**  
[Configure content exclusion for Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)

**Question:** [046]  
Your organization is on the **GitHub Team** plan and needs **license management**, **policy controls**, and **usage reporting**, but no enterprise integrations. Which Copilot plan fits?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B

**Explanation:**  
**Copilot Business** is available to orgs on **GitHub Team** **and** **Enterprise Cloud**. It provides **license assignment**, **policy enforcement**, **content exclusions**, **usage reporting**, and **audit logs**—without the enterprise-only integrations of **Copilot Enterprise**.

**Tips and Tricks:**  
- **Team or Enterprise Cloud org + admin controls (no enterprise integrations)** → **Business**.  
- If the stem mentions **GitHub.com repo-aware Chat** or **enterprise integrations**, move to **Enterprise**.

> [!IMPORTANT]  
> Match the **base org plan** first: **Team/Enterprise Cloud → Business**, **Enterprise Cloud with enterprise integrations → Enterprise**.

**Source:**  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Reviewing audit logs for GitHub Copilot Business](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)

**Question:** [047]  
Which GitHub Copilot plan(s) provide **content/context exclusion** to prevent specific files or repositories from being used as suggestion context? *(Choose all that apply.)*

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B, C

**Explanation:**  
**Content/context exclusion** is available at the **organization/enterprise** tiers—**Copilot Business** and **Copilot Enterprise**—to govern what Copilot can see when generating suggestions.

**Tips and Tricks:**  
- Think **data governance** features (exclusions, policies, audit) → **org/enterprise** tiers, not **individual**.  
- Use exclusions to reduce **sensitive data exposure** by constraining model context.

> [!IMPORTANT]  
> Configure and **audit** exclusions centrally so changes are tracked in your org/enterprise logs.

**Source:**  
[Content exclusion for Copilot (availability)](https://docs.github.com/en/enterprise-cloud%40latest/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Configure & audit content exclusion](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/configure-content-exclusion) (GitHub Docs)  
[Changelog: content exclusion GA for Business/Enterprise](https://github.blog/changelog/2024-11-12-content-exclusion-ga/) (GitHub Blog)

**Question:** [048]  
Which statement about **support SLAs** and Copilot plans is **accurate**?

**Options:**  
A. Copilot Enterprise **includes** Premium Support SLAs by default  
B. **GitHub Premium Support (with SLAs) is a separate, paid offering** for Enterprise customers and can be paired with Copilot Enterprise  
C. Copilot Business includes 24/7 SLA-backed support by default  
D. Copilot Pro includes SLA-backed support for individuals

**Correct Answer(s):** B

**Explanation:**  
**Premium Support with SLAs** is **not bundled** with any Copilot plan; it is a **separate, paid** support tier for GitHub Enterprise customers that can be added alongside Copilot Enterprise.

**Tips and Tricks:**  
- When stems mention **SLA targets/response times**, think **Premium Support add-on**, not a Copilot plan feature.  
- Keep **plan features** (Copilot) distinct from **support entitlements** (Premium Support).

> [!IMPORTANT]  
> Align **enterprise governance** needs with **Copilot Enterprise**, and add **Premium Support SLAs** only if your operational model requires contractual response times.

**Source:**  
[**About GitHub Premium Support** (paid add-on)](https://docs.github.com/en/enterprise-cloud%40latest/support/learning-about-github-support/about-github-premium-support) (GitHub Docs)  
[GitHub Support tiers overview](https://docs.github.com/en/enterprise-cloud%40latest/support) (GitHub Docs)  
[Premium Support offering page](https://github.com/enterprise/premium-support) (GitHub)

**Question:** [049]  
Which statement about **SSO** and Copilot plans is **correct**?

**Options:**  
A. SSO is **bundled** with Copilot Enterprise as a plan feature  
B. **SSO is an Enterprise Cloud organization capability; Copilot Enterprise uses your org’s SSO if configured**  
C. Copilot Business enables SSO for **GitHub Team** orgs  
D. Copilot Pro enables SSO for individuals

**Correct Answer(s):** B

**Explanation:**  
**SSO** is configured at the **GitHub Enterprise Cloud organization/enterprise** level. **Copilot Enterprise relies on the org’s existing SSO**, it doesn’t include SSO as a Copilot-specific feature.

**Tips and Tricks:**  
- Evaluate **identity** at the **org/enterprise** layer first; then choose the Copilot plan.  
- This avoids over-attributing **identity features** to Copilot itself.

> [!IMPORTANT]  
> Use Copilot Enterprise **with** your org’s SAML/IdP setup; configure SSO in **Enterprise Cloud** (not within Copilot plan settings).

**Source:**  
[Managing SAML SSO for your organization (Enterprise Cloud)](https://docs.github.com/en/enterprise-cloud%40latest/organizations/managing-saml-single-sign-on-for-your-organization) (GitHub Docs)  
[About SAML for enterprise IAM](https://docs.github.com/en/enterprise-cloud%40latest/admin/managing-iam/understanding-iam-for-enterprises/about-saml-for-enterprise-iam) (GitHub Docs)  
[Choosing your enterprise’s Copilot plan](https://docs.github.com/copilot/get-started/choosing-your-enterprises-plan-for-github-copilot) (GitHub Docs)

**Question:** [050]  
When you start a **free 30-day trial of GitHub Enterprise Cloud**, which GitHub Copilot plan is **included with the trial**?

**Options:**  
A. GitHub Copilot Free  
B. GitHub Copilot Pro  
C. GitHub Copilot Business  
D. GitHub Copilot Enterprise  
E. None, Copilot always requires a separate purchase

**Correct Answer(s):** C

**Explanation:**  
The **GitHub Enterprise Cloud trial includes GitHub Copilot Business** so enterprises can evaluate **org-level controls**, **policies**, and **reporting** during the trial period.

**Tips and Tricks:**  
- “**Trial includes**” maps to **Copilot Business**, not Pro, not Enterprise.  
- After the trial, ongoing Copilot usage requires **paid licensing**.

> [!IMPORTANT]  
> During the trial you can enable **Copilot Business**. GitHub notes you may need to **add a card**, but **no charge occurs during the trial**. **Copilot Enterprise** is available to Enterprise Cloud orgs, but **not included by default**.

**Source:**  
[Subscribing to GitHub Copilot for your enterprise](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-plan/subscribe) (GitHub Docs)  
[Setting up a trial of GitHub Enterprise Cloud](https://docs.github.com/en/enterprise-cloud%40latest/enterprise-onboarding/getting-started-with-your-enterprise/setting-up-a-trial-of-github-enterprise) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/enterprise-cloud%40latest/copilot/get-started/plans) (GitHub Docs)

**Question:** [051]  
Who can **manage** (create or edit) **content exclusion** settings for GitHub Copilot? *(Choose all that apply.)*

**Options:**  
A. Repository administrators  
B. Organization owners  
C. Enterprise owners  
D. People with the **Maintain** role for a repository  
E. Outside collaborators

**Correct Answer(s):** A, B, C

**Explanation:**  
**Repository administrators**, **organization owners**, and **enterprise owners** can **configure content exclusion**. **Maintain** can **view** but **not edit**. **Outside collaborators** cannot manage exclusions.

**Tips and Tricks:**  
- **Manage** is not **view**, **Maintain = view only**.  
- Content exclusion is available for **Copilot Business** and **Copilot Enterprise** orgs.

> [!IMPORTANT]  
> **Content exclusion** controls **what Copilot can see**. It is distinct from **duplication detection or code referencing**, which governs **what Copilot may suggest or show**.

**Source:**  
[Excluding content from GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Content exclusion, concept and roles](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)

**Question:** [052]  
What is the purpose of GitHub Copilot’s **duplication detection or code-referencing controls**?

**Options:**  
A. To compress prompts for faster latency  
B. To block or identify suggestions that **match public code** on GitHub  
C. To disable Copilot Chat history  
D. To auto-attribute licenses in your repository

**Correct Answer(s):** B

**Explanation:**  
Copilot can **check a suggestion** (including about **~150 surrounding characters**) against **public GitHub code**. You can **block** matching suggestions or **allow with references** that show the **origin repository and license**.

**Tips and Tricks:**  
- **Block** suppresses the suggestion. **Allow with references** shows the source for legal or engineering review.  
- Configure at **organization** or **individual** level, depending on plan and surface.

> [!IMPORTANT]  
> Pair **code referencing** with **content exclusion**. Exclusion limits **context visibility**, referencing limits or labels **suggested output**. Together they reduce **IP and license risk**.

**Source:**  
[Finding public code that matches suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  
[Copilot code referencing, concept](https://github.blog/news-insights/product-news/introducing-code-referencing-for-github-copilot/) (GitHub Blog)

**Question:** [053]  
Which GitHub Copilot plan is available to enterprises using **GitHub Enterprise Cloud**, providing **advanced compliance**, **audit**, and **identity** features?

**Options:**  
A. GitHub Copilot Business  
B. GitHub Copilot Enterprise  
C. GitHub Copilot Pro  
D. GitHub Copilot Free

**Correct Answer(s):** B

**Explanation:**  
**GitHub Copilot Enterprise** is available to **GitHub Enterprise Cloud** organizations and adds **enterprise-grade governance** (for example, **audit visibility**, **enterprise integrations**, and **GitHub.com repository-aware Copilot Chat**). Identity such as **SSO** is configured at the **Enterprise Cloud organization** level; Copilot Enterprise **uses your org’s SSO** rather than bundling SSO in the plan.

**Tips and Tricks:**  
- Mentions of **Enterprise Cloud**, **enterprise integrations**, **advanced compliance/audit**, or **GitHub.com repo-aware Chat** point to **Copilot Enterprise**.  
- **Copilot Business** gives org-level controls (policies, usage, **audit logs**) for **Team** and **Enterprise Cloud** orgs, but not the **Enterprise-only** GitHub.com context features.

> [!IMPORTANT]  
> Treat **SSO** as an **Enterprise Cloud organization capability** that **Copilot Enterprise relies on**. Distinguish **Business (admin controls + audit logs)** from **Enterprise (adds enterprise-only integrations and GitHub.com context)**.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)  
[GitHub Copilot Enterprise is now generally available](https://github.blog/news-insights/product-news/github-copilot-enterprise-is-now-generally-available/) (GitHub Blog)

**Question:** [054]  
Which GitHub Copilot plan provides **enterprise proxy support** and **advanced compliance** features, and can be paired with **GitHub Premium Support (SLAs) as a separate purchase**?

**Options:**  
A. GitHub Copilot Business  
B. GitHub Copilot Enterprise  
C. GitHub Copilot Pro  
D. GitHub Copilot Free

**Correct Answer(s):** B

**Explanation:**  
**GitHub Copilot Enterprise** supports **enterprise network/proxy configurations** and provides **enterprise-grade compliance and audit capabilities** for **GitHub Enterprise Cloud** organizations. If SLA-backed response targets are required, **GitHub Premium Support** can be purchased **separately** (it is **not bundled** with any Copilot plan).

**Tips and Tricks:**  
- **Proxy/network controls + enterprise compliance/audit** are strong signals for **Copilot Enterprise**.  
- Keep **support entitlements** (for example, **Premium Support with SLAs**) **separate** from **Copilot plan features**.

> [!IMPORTANT]  
> Treat **identity (SSO)** and **network/proxy** as **Enterprise Cloud org capabilities** that **Copilot Enterprise relies on**. Use **Copilot Enterprise** for **enterprise integrations**, **GitHub.com repository-aware Chat**, and **governance**; add **Premium Support** only if your operations require SLA-backed response times.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[About GitHub Premium Support](https://docs.github.com/en/enterprise-cloud%40latest/support/learning-about-github-support/about-github-premium-support) (GitHub Docs)  
[GitHub Copilot Enterprise is now generally available](https://github.blog/news-insights/product-news/github-copilot-enterprise-is-now-generally-available/) (GitHub Blog)

**Question:** [055]  
Which GitHub Copilot plan enables **organization administrators** to define and enforce **policy settings** for how code suggestions are generated?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B

**Explanation:**  
**GitHub Copilot Business** provides **org-level policy controls** (for example, enabling or disabling features and models, **public code filtering**, and **content/context exclusions**) so administrators can govern how suggestions are generated across the organization. Enterprise Cloud customers can also manage these policies at the **enterprise** scope.

**Tips and Tricks:**  
- Cues like **admin policies**, **model/feature availability**, **exclusions**, **public code filtering** map to **Business**.  
- **Pro** and **Free** have **no** org governance; **Enterprise** orchestrates policies at enterprise scope but the controls originate at the org tier.

> [!IMPORTANT]  
> Standardize Copilot behavior with **central policies** first, then extend to the **enterprise level** if you operate multiple orgs under Enterprise Cloud.

**Source:**  
[Managing policies for Copilot in your organization](https://docs.github.com/copilot/how-tos/administer/organizations/managing-policies-for-copilot-in-your-organization) (GitHub Docs)  
[Copilot policies, concepts](https://docs.github.com/en/copilot/concepts/policies) (GitHub Docs)  
[Manage enterprise policies for Copilot](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)

**Question:** [056]  
Which GitHub Copilot plan provides **organization administrators** with **usage metrics and reports** for members’ Copilot activity?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** B, C

**Explanation:**  
Both **Business** and **Enterprise** expose **usage reporting** so admins can monitor **adoption**, **entitlements**, and **usage trends** (including downloadable activity reports) across teams and organizations.

**Tips and Tricks:**  
- Phrases like **org usage**, **metrics**, **reporting**, **activity report** point to **Business/Enterprise**.  
- **Pro** is individual only; **Free** has no org reporting.

> [!IMPORTANT]  
> Pair **usage reports** with **policy controls** to drive enablement, governance, and cost oversight.

**Source:**  
[Review user activity data (organization)](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-user-activity-data) (GitHub Docs)  
[Download Copilot activity report](https://docs.github.com/en/copilot/how-tos/administer-copilot/download-activity-report) (GitHub Docs)  
[Monitor usage and entitlements](https://docs.github.com/en/copilot/how-tos/manage-and-track-spending/monitor-premium-requests) (GitHub Docs)

**Question:** [057]  
Which GitHub Copilot plan provides **advanced governance** for enterprise-scale organizations (for example, **enterprise integrations** and **GitHub.com repository-aware Copilot Chat**) alongside **audit visibility** and compliance support?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**Copilot Enterprise** adds **enterprise-only integrations** and **GitHub.com repo-aware Copilot Chat** for Enterprise Cloud orgs, on top of org admin features (including **audit logs**) available in Business. This combination supports **enterprise governance** and compliance workflows.

**Tips and Tricks:**  
- “**Enterprise integrations**,” “**GitHub.com repo-aware Chat**,” or “**enterprise governance**” point to **Enterprise**.  
- Remember: **Business also has audit logs**; Enterprise distinguishes itself with **GitHub.com context** and broader integration surfaces.

> [!IMPORTANT]  
> Treat **audit visibility** as an **org capability** present in both Business and Enterprise; choose **Enterprise** when scenarios explicitly require **GitHub.com context** or **enterprise integrations**.

**Source:**  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[Copilot features overview](https://docs.github.com/en/enterprise-cloud%40latest/copilot/get-started/features) (GitHub Docs)  
[Review audit logs for Copilot (Business/Enterprise)](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)

**Question:** [058]  
Which GitHub Copilot plan offers **enterprise-grade integrations** with systems such as **audit visibility**, **SSO (org-configured)**, and **compliance** features?

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free

**Correct Answer(s):** C

**Explanation:**  
**GitHub Copilot Enterprise** adds **enterprise integrations** and **GitHub.com repository-aware Copilot Chat** for **Enterprise Cloud** orgs, on top of org-level admin features. **SSO** is configured at the **Enterprise Cloud organization** level; Copilot Enterprise **uses your org’s SSO** rather than bundling SSO in the plan.

**Tips and Tricks:**  
- If you see **enterprise integrations**, **GitHub.com repo-aware Chat**, or **enterprise governance**, select **Copilot Enterprise**.  
- **Business** includes **policy controls**, **usage reporting**, and **audit logs**; **Enterprise** extends this with **enterprise-only integrations** and **GitHub.com context**.

> [!IMPORTANT]  
> Treat **identity (SSO)** as an **Enterprise Cloud org capability**. Distinguish **Business** (admin controls + audit logs) from **Enterprise** (adds **enterprise integrations** and **repo-aware Chat** on GitHub.com).

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choose a Copilot plan for your enterprise](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)  
[GitHub Copilot Enterprise is now generally available](https://github.blog/news-insights/product-news/github-copilot-enterprise-is-now-generally-available/) (GitHub Blog)

**Question:** [059]  
In which environments is **GitHub Copilot Chat** available today? *(Choose all that apply.)*

**Options:**  
A. GitHub.com  
B. Visual Studio Code  
C. Visual Studio  
D. JetBrains IDEs  
E. GitHub Desktop

**Correct Answer(s):** A, B, C, D

**Explanation:**  
**Copilot Chat** is supported on **GitHub.com** and inside major IDEs including **VS Code**, **Visual Studio**, and **JetBrains IDEs**. **GitHub Desktop** is **not** a supported Copilot Chat surface.

**Tips and Tricks:**  
- “Chatting about code in the **browser (GitHub.com)** or in **VS Code / Visual Studio / JetBrains**” means **Copilot Chat**.  
- References to **GitHub Desktop** are distractors.

> [!IMPORTANT]  
> Know the supported **surfaces**: **GitHub.com** and **IDE integrations**. This is a frequent exam discriminator.

**Source:**  
[About GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)  
[Chat with GitHub Copilot in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[What is GitHub Copilot?](https://docs.github.com/en/copilot/get-started/what-is-github-copilot) (GitHub Docs)

**Question:** [060]  
Which GitHub Copilot plan(s) support **centralized seat (license) assignment and management** at the **organization** level? *(Choose all that apply.)*

**Options:**  
A. GitHub Copilot Pro  
B. GitHub Copilot Business  
C. GitHub Copilot Enterprise  
D. GitHub Copilot Free  
E. GitHub Team (non-Copilot plan)

**Correct Answer(s):** B, C

**Explanation:**  
**Copilot Business** and **Copilot Enterprise** are **organization-managed** plans that allow admins to **assign and manage seats**. **Pro** is an **individual** subscription and **cannot** be centrally managed. **Free** has no org licensing.

**Tips and Tricks:**  
- Any mention of **org seat assignment**, **centralized licensing**, or **admin-managed provisioning** means **Business** or **Enterprise**.  
- **GitHub Team** is a base org plan, **not** a Copilot plan.

> [!IMPORTANT]  
> Seat management is an **org capability** that starts at **Copilot Business** and continues in **Copilot Enterprise**.

**Source:**  
[GitHub Copilot licenses](https://docs.github.com/en/billing/concepts/product-billing/github-copilot-licenses) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)