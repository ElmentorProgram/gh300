# Raw Practice Test 02 - Answer Sheet

101. Is **Windows Terminal** a supported surface for **Copilot Chat**?  
A. No, terminal isn’t supported  
B. **Yes, Windows Terminal is listed among supported Copilot Chat surfaces**  
C. Yes, but only on GHES  
D. Only if you disable inline suggestions  
**Correct Answer(s):** B  

102. How can Copilot help with **documentation tasks** such as docstrings, README sections, and code comments?  
A. It can only generate code, not docs  
B. **Use Copilot Chat and selection-based prompts to draft docstrings, comments, and README snippets**  
C. Docs are generated automatically on every commit  
D. Only Enterprise plans can generate documentation  
**Correct Answer(s):** B  

103. How can Copilot assist with **debugging and fixing errors**?  
A. It automatically fixes all errors at build time  
B. **Use Copilot Chat to explain error messages/stack traces and propose fixes or refactors**  
C. Errors must be fixed manually; Copilot doesn’t help  
D. Only Enterprise users can use Chat for debugging  
**Correct Answer(s):** B  

104. How can Copilot support a **TDD (red→green→refactor)** workflow?  
A. By auto-approving PRs when tests pass  
B. **By generating test scaffolds/cases from selections and then helping refactor after tests pass**  
C. By disabling tests during development  
D. By replacing the need for assertions  
**Correct Answer(s):** B  

105. What actually happens when you **accept an inline suggestion**?  
A. The code is auto-committed and pushed  
B. **The suggestion is inserted into your editor; you decide whether to keep, edit, or discard**  
C. The change is merged to main if CI passes  
D. An audit log entry is always generated  
**Correct Answer(s):** B  

106. How can Copilot help you **understand an unfamiliar file or component** in your codebase?  
A. It can’t, Copilot only writes code  
B. **Use selection/file prompts in Copilot Chat to summarize purpose, dependencies, and risks**  
C. Only repository-aware chat in Enterprise can explain files  
D. You must upload files to a third-party site  
**Correct Answer(s):** B  

107. Which is the **best-crafted prompt**?  
A. Write a function  
B. **Write a Python function to reverse a string using slicing**  
C. Function in code  
D. Suggest some code  
**Correct Answer(s):** B  

108. How do you improve **ambiguous prompts**?  
A. Use shorter prompts  
B. **Provide more context and details**  
C. Avoid specifying language  
D. Retry without changes  
**Correct Answer(s):** B  

109. Which technique most reliably boosts output quality?  
A. Use vague prompts  
B. **Use detailed instructions with examples**  
C. Avoid comments in code  
D. Skip specifying input or output  
**Correct Answer(s):** B  

110. Why does adding **examples** help?  
A. Examples distract the AI  
B. **They align output with the desired style/pattern**  
C. They reduce Copilot’s ability to generate code  
D. They slow completions  
**Correct Answer(s):** B  

111. Why is **context** crucial in prompts?  
A. It slows responses  
B. **It helps Copilot generate relevant and accurate suggestions**  
C. It prevents completions  
D. It reduces security  
**Correct Answer(s):** B  

112. What should you do if Copilot generates **irrelevant suggestions**?  
A. Stop using Copilot  
B. **Refine or rephrase the prompt with more context**  
C. Use shorter prompts  
D. Disable duplication detection  
**Correct Answer(s):** B  

113. Which practice helps Copilot match **project style**?  
A. Avoid adding comments  
B. **Add snippets and style examples**  
C. Use vague instructions  
D. Skip output format  
**Correct Answer(s):** B  

114. Which statement best describes **what Copilot relies on during inference**?  
A. Runtime execution of your code  
B. **Your prompts, file contents, and surrounding code context**  
C. Web searches via Bing  
D. Pre-stored templates  
**Correct Answer(s):** B  

115. What does **content exclusion** let organizations do (and why is it relevant to prompting)?  
A. Speed up Copilot  
B. **Prevent specified repos/paths/file types/patterns from being used as input context**  
C. Disable Copilot entirely  
D. Publish private code  
**Correct Answer(s):** B  

116. Which **Copilot plans** include **content exclusion**?  
A. Free and Individual  
B. **Business and Enterprise**  
C. Individual only  
D. Free only  
**Correct Answer(s):** B  

117. Which prompt gives Copilot the **clearest output target**?  
A. “Summarize this.”  
B. **“Summarize this function in 3 bullets for junior devs; include inputs, outputs, and one caveat.”**  
C. “Explain code.”  
D. “Write notes.”  
**Correct Answer(s):** B  

118. When asking Copilot to refactor code, which prompt is best?  
A. “Improve this.”  
B. **“Refactor to pure functions; no side effects; keep same public API; add docstrings; return early on invalid input.”**  
C. “Make it cleaner.”  
D. “Rewrite completely.”  
**Correct Answer(s):** B  

119. Which prompt best reduces **hallucinations** when generating API code?  
A. “Use the Foo API.”  
B. **“Use Foo API v3; only endpoints /users/{id}, /users/search; TypeScript; fetch; no undocumented fields; include error handling for 4xx/5xx.”**  
C. “Write users code.”  
D. “Guess the latest endpoints.”  
**Correct Answer(s):** B  

120. You want table-driven unit tests. Which prompt is best?  
A. “Write tests.”  
B. **“Generate table-driven tests in Go for Parse(), covering empty, invalid, edge lengths; include names and wantErr.”**  
C. “Test everything.”  
D. “Add some asserts.”  
**Correct Answer(s):** B  

121. Which instruction most improves **SQL** prompts?  
A. “PostgreSQL 14; given schema (tables/columns below); return top 5 customers by revenue last 30 days; output columns: id, name, revenue.”  
B. “Given schema (tables/columns below); return top 5 customers by revenue last 30 days; include window fn for rank; output columns: id, name, revenue, rank.”  
C. “Write a SQL query using the schema below to return the top 5 customers by revenue in the last 30 days; choose any appropriate columns.”  
D. **“PostgreSQL 14; given schema (tables/columns below); return top 5 customers by revenue last 30 days; include window fn for rank; output columns: id, name, revenue, rank.”**  
**Correct Answer(s):** D  

122. Which prompt best directs Copilot to produce **safe code** for secrets?  
A. “Use an API key from an environment variable; if it’s missing, fall back to a default test key and log the value for debugging.”  
B. “Get the API key from a secrets manager or environment variable; if unavailable, continue with limited functionality and log configuration details.”  
C. **“Read API key from env var; do not hardcode; fail fast if missing; log-safe (no secrets in logs); show minimal example.”**  
D. “Store the API key in a configuration file checked into the repo; document that it should not be shared publicly.”  
**Correct Answer(s):** C  

123. You want Copilot to **explain** a complex file to a new teammate. Best prompt?  
A. “Explain this file in detail: what it does, how it works, and any important parts.”  
B. “Summarize this file for engineers: main purpose, data flows, and dependencies.”  
C. “Create a thorough explanation of this file, including architecture, flows, and risks, with no strict length limit.”  
D. **“Explain this file for a new backend hire: purpose, key data flows, external dependencies, risks; 5 bullets max.”**  
**Correct Answer(s):** D  

124. Which prompt targets a **performance-aware** implementation?  
A. **“Write a streaming JSON parser in Node.js; O(1) extra space; handle 10MB+ inputs; backpressure with streams; include benchmarks stub.”**  
B. “Write a streaming JSON parser in Node.js that can handle 10MB+ inputs and include a simple benchmark.”  
C. “Write a fast JSON parser in Node.js; it should parse 10MB+ inputs and be efficient.”  
D. “Write a JSON parser in any language; prioritize performance and document how to test its speed.”  
**Correct Answer(s):** A  

125. Which prompt best **constrains the output format** so it can be pasted into CI?  
A. “List failing tests with their names and error messages in any readable format.”  
B. **“Output JSON array of failing tests with fields: name, file, line, message no prose.”**  
C. “Return failing tests as JSON with test name and message, plus a short explanation of likely causes.”  
D. “Output a human-readable report of failing tests, grouped by file, suitable for pasting into chat or email.”  
**Correct Answer(s):** B  

126. You need a **migration plan** before code. Best prompt?  
A. “Create a short plan to migrate this service from Flask to FastAPI, focusing on the main steps required to complete the migration.”  
B. “Outline the tasks to move this service from Flask to FastAPI and then implement the new routes in FastAPI.”  
C. **“Create a 5-step plan to migrate Flask → FastAPI; list risks, roll-back steps, and how to keep routes backward-compatible.”**  
D. “Provide FastAPI code that replicates the current Flask service’s behavior, assuming breaking changes are acceptable if they simplify the migration.”  
**Correct Answer(s):** C  

127. Which prompt reduces **overbroad refactors** in large files?  
A. “Refactor the `parseHeader` logic to make it clearer and more robust across the parser code.”  
B. “Update the parser to handle invalid headers better and improve error messages throughout the file.”  
C. “Tidy up `parseHeader` and related helpers, improving structure and naming wherever it seems useful.”  
D. **“Modify only function `parseHeader`; keep public behavior; add bounds checks; return detailed errors.”**  
**Correct Answer(s):** D  

128. How do you prompt for **secure HTTP handling**?  
A. **“Use HTTPS; validate TLS certs; set timeouts and retries; redact secrets in logs; handle 429/5xx with backoff.”**  
B. “Call the API over HTTPS and log the full request and response body for debugging if something goes wrong.”  
C. “Use HTTPS with a reasonable timeout and retry a few times on failure.”  
D. “Call the API with HTTPS but skip strict certificate validation to avoid connection issues.”  
**Correct Answer(s):** A  

129. Which prompt best avoids **unsupported library calls**?  
A. “Use Redis with a standard client library and configure basic connection settings for your environment.”  
B. “Initialize Redis in Python using redis-py and show how to set and get a key for caching.”  
C. “Use Redis for caching in your service and choose any compatible client version that works with your stack.”  
D. **“Python 3.11; redis-py v5 only; use `Redis.from_url`; no deprecated APIs; include connection timeout and health check.”**  
**Correct Answer(s):** D  

130. Best way to ask for a **configurable CLI tool**?  
A. **“Create a Python CLI with `argparse`; flags: `--input`, `--format (json|csv)`, `--verbose`; validate files; exit codes 0/2; examples.”**  
B. “Write a Python CLI that accepts some arguments and prints a result based on the input.”  
C. “Create a CLI script in any language that processes an input file and prints output to the console.”  
D. “Set up a simple command-line entry point without worrying about validation, exit codes, or detailed help text.”  
**Correct Answer(s):** A  

131. How to prompt for a **safe database migration**?  
A. “Add a new `status` column and update the application to start using it, then remove old fields later if needed.”  
B. “Update the schema and data to support a `status` field in a way that works for your database engine.”  
C. **“Add column `status` (ENUM) with default ‘new’; backfill from `state`; online migration (no downtime); include rollback SQL.”**  
D. “Redesign the schema to better model status and deploy the changes during a low-traffic window, accepting some downtime.”  
**Correct Answer(s):** C  

132. Which prompt best constrains **logging** for privacy?  
A. “Add JSON logs with level and message, and include full request and response bodies to simplify debugging.”  
B. “Add structured logs with level, event, and user details; include tokens in debug mode to help trace issues.”  
C. **“Add structured JSON logs: level, event, requestId; no PII; redact tokens; include error stack; single line per event.”**  
D. “Enable verbose logging across the service, capturing all available fields by default and filtering sensitive data later if needed.”  
**Correct Answer(s):** C  

133. Which plan offers **enterprise proxy support** and integration with **advanced compliance** capabilities?  
A. Copilot Free, for individuals without governance or compliance controls  
B. Copilot Individual (Pro/Pro+), with premium personal features only  
C. **Copilot Enterprise**  
D. Copilot Business, with org-level license management and policies but not full enterprise compliance integrations  
**Correct Answer(s):** C  

134. Which plan includes **organization-level** controls like **content exclusion** and **usage visibility**?  
A. Copilot Free  
B. Copilot Individual (Pro/Pro+)  
C. **Copilot Business**  
D. Copilot Enterprise  
**Correct Answer(s):** C  

135. Which plan includes **audit logs** and advanced **compliance** controls?  
A. Copilot Free  
B. Copilot Individual (Pro/Pro+)  
C. Copilot Business  
D. **Copilot Enterprise**  
**Correct Answer(s):** D  

136. What’s the practical difference between **Copilot Edits – Edit mode** and **Agent mode**?  
A. Edit auto-merges; Agent requires reviews  
B. **Edit = user-scoped diffs; Agent = autonomous, multi-step execution that may culminate in a PR**  
C. Edit is IDE-only; Agent is GitHub.com only  
D. Edit reads the repo; Agent can’t  
**Correct Answer(s):** B  

137. What is the **minimum length** Copilot’s duplication-detection filter considers when blocking **exact matches**?  
A. 50 characters  
B. **150 characters**  
C. 500 characters  
D. 1,000 characters  
**Correct Answer(s):** B  

138. Which plan provides **organizational license management** and **usage reporting** **without** enterprise integrations (like audit logs/SSO)?  
A. Copilot Free  
B. Copilot Individual (Pro/Pro+)  
C. **Copilot Business**  
D. Copilot Enterprise  
**Correct Answer(s):** C  

139. Which of the following is an **advanced developer use case** for Copilot?  
A. **Helping explore unfamiliar APIs and libraries**  
B. Automating end-to-end payroll and compliance processing for HR teams  
C. Drafting legally binding corporate contracts without human review  
D. Managing calendar invites, meeting rooms, and company-wide scheduling  
**Correct Answer(s):** A  

140. Which plan provides features like **license management** and **content exclusion** for organizations?  
A. Copilot Individual (Pro/Pro+)  
B. **Copilot Business**  
C. Copilot Enterprise  
D. Copilot Free  
**Correct Answer(s):** B  

141. Which setting governs **similar-but-not-exact** suggestions that resemble public code?  
A. Content exclusion  
B. **Code referencing (matching public code)**  
C. Duplication-detection filter  
D. Usage reporting  
**Correct Answer(s):** B  

142. When **code referencing** is set to **“Allow + show references”**, what should you expect?  
A. Copilot blocks all similar suggestions  
B. **Copilot may show the suggestion with links to public sources**  
C. Duplication filter is disabled  
D. Content exclusion is ignored  
**Correct Answer(s):** B  

143. At what **scopes** can you configure **code referencing** behavior?  
A. Only repository level  
B. **Individual account and org/enterprise policies**  
C. Only enterprise level  
D. Only IDE settings  
**Correct Answer(s):** B  

144. Which statement about **content exclusion** is accurate?  
A. It censors outputs that resemble excluded files  
B. **It prevents excluded repos/paths/types/patterns from being used as input context**  
C. It disables Copilot in the repository  
D. It removes excluded files from Git history  
**Correct Answer(s):** B  

145. Which roles can **manage** content exclusion policies?  
A. Outside collaborators only  
B. People with Maintain role  
C. **Repository administrators, organization owners, and enterprise owners**  
D. Any repository contributor  
**Correct Answer(s):** C  

146. A suggestion exactly matches ~200 characters from a public repo. What happens?  
A. It’s allowed as long as the public code uses a permissive license.  
B. **It is blocked by duplication-detection filters**  
C. It always shows with references instead of being blocked.  
D. It shows or is blocked based solely on the repository’s license file.  
**Correct Answer(s):** B  

147. Which plan enables **repository-aware Copilot Chat on GitHub.com** (chat that can reference repo files and docs)?  
A. Copilot Individual (Pro/Pro+)  
B. Copilot Business  
C. **Copilot Enterprise**  
D. Copilot Free  
**Correct Answer(s):** C  

148. Which statement about **Copilot Knowledge Bases** is accurate?  
A. Available on all plans  
B. Available on Business & Enterprise  
C. **Enterprise-only curated sources for chat grounding (GitHub.com/VS Code)**  
D. Available on Individual Pro/Pro+ only  
**Correct Answer(s):** C  

149. Who manages purchasing and **seat assignment** for **Business vs. Enterprise**?  
A. Developers in the IDE  
B. **Org owners (Business); Enterprise owners (Enterprise)**  
C. Repository admins for both  
D. Any organization member  
**Correct Answer(s):** B  

150. Which capability allows Copilot to perform **multi-step changes** and open a **pull request** for review?  
A. Inline suggestions  
B. **Copilot coding agent (Agent mode)**  
C. Content exclusion  
D. Code referencing  
**Correct Answer(s):** B  

151. On GitHub.com, what do **Copilot code reviews** and **PR summaries** provide?  
A. Automatically approves and merges pull requests without human review.  
B. **AI review suggestions and natural-language summaries of changes**  
C. Formal license validation and legal sign-off for all dependencies.  
D. Only low-level static analysis warnings without any natural-language context.  
**Correct Answer(s):** B  

152. How does Copilot handle suggestions that **exactly match** long segments of **public code**?  
A. Blocks any suggestion that resembles public code, regardless of length or settings.  
B. Shows suggestions that match public code but only adds links to the original repositories, without blocking.  
C. **Uses duplication-detection filters to block long exact matches**  
D. Relies solely on manual code review to detect and remove duplicated public code.  
**Correct Answer(s):** C  

153. How can Copilot assist with unit testing?  
A. **By automatically generating test functions from code definitions**  
B. By running your unit test suite automatically in your CI/CD pipeline  
C. By replacing QA engineers and manual testing processes  
D. By creating and managing isolated test environments in the cloud  
**Correct Answer(s):** A  

154. Which Copilot plan provides **enterprise proxy support** for secure environments?  
A. Copilot Free  
B. Copilot Individual  
C. Copilot Business  
D. **Copilot Enterprise**  
**Correct Answer(s):** D  

155. On which **surfaces** is **Copilot Chat** available today? *(Choose all that apply.)*  
A. GitHub.com  
B. Visual Studio Code  
C. Visual Studio  
D. JetBrains IDEs  
E. Eclipse  
F. Xcode  
G. GitHub Mobile  
H. Windows Terminal  
I. GitHub Desktop  
**Correct Answer(s):** A, B, C, D, E, F, G, H  

156. Is GitHub Copilot supported on **GitHub Enterprise Server (GHES)**?  
A. Yes, Copilot runs entirely on-premises inside your GHES instance.  
B. **No, Copilot requires the cloud service; GHES is not supported**  
C. Yes, but only Copilot Chat is supported on GHES.  
D. Yes, with a fully self-hosted Copilot model inside your data center.  
**Correct Answer(s):** B  

157. What can **Copilot Chat in the CLI** help you do?  
A. **Draft and explain shell and Git commands and their flags**  
B. Execute terminal commands automatically without your confirmation  
C. Completely replace the need for shell help and man pages  
D. Automatically provision and configure cloud environments from the CLI  
**Correct Answer(s):** A  

158. Across environments, what’s the right way to think about **inline suggestions vs. Chat**?  
A. Inline runs only in browsers, while Chat runs only inside IDEs.  
B. **Inline = cursor-local completions; Chat = multi-turn reasoning with selectable context (files/regions)**  
C. Chat always writes code straight to the repository without user review.  
D. Inline is deprecated and disabled once Chat is turned on.  
**Correct Answer(s):** B  

159. Do **content exclusion** policies apply **across all Copilot surfaces**?  
A. No, content exclusion only applies when using Copilot in Visual Studio Code.  
B. **Yes, content exclusion defines the input context boundary for Copilot across supported surfaces**  
C. No, it only affects Copilot Chat on GitHub.com, not IDEs.  
D. No, it only applies in JetBrains IDEs and not on other clients.  
**Correct Answer(s):** B  

160. What Copilot plan offers AI-powered code completions for free, but with limited features compared to paid plans?  
A. **Copilot Free**  
B. Copilot Individual (Pro/Pro+), with full paid features for one developer  
C. Copilot Business, with org-level governance and reporting  
D. Copilot Enterprise, with enterprise integrations and network controls  
**Correct Answer(s):** A  

161. Which Copilot plan provides organizational visibility into **usage metrics** but does **not** include enterprise-grade compliance?  
A. Copilot Individual (Pro/Pro+), with no org-wide usage reporting  
B. **Copilot Business**  
C. Copilot Enterprise, with enterprise-grade compliance integrations  
D. Copilot Free, with no admin visibility  
**Correct Answer(s):** B  

162. Which Copilot plan gives **organizations** control over which repositories and code Copilot can access?  
A. Copilot Free, with no org-level repository controls  
B. Copilot Individual (Pro/Pro+), with only personal settings  
C. **Copilot Business**  
D. Copilot Enterprise, which builds on Business with enterprise integrations  
**Correct Answer(s):** C  

163. Which Copilot plan is most appropriate for developers who want **Copilot Chat** and code completion but **no** organizational management features?  
A. Copilot Free, with limited features and no full Chat experience  
B. **Copilot Individual (Pro/Pro+)**  
C. Copilot Business, which adds org-level management and reporting  
D. Copilot Enterprise, which adds enterprise identity and compliance  
**Correct Answer(s):** B  

164. Is **Copilot Enterprise** included with GitHub Enterprise Cloud (GHEC) at **no additional cost**?  
A. **No, Copilot Enterprise is a separate paid subscription available to GHEC orgs**  
B. Yes, it’s bundled for free with GHEC  
**Correct Answer(s):** A  

165. Which Copilot feature is particularly useful for exploring **unfamiliar APIs**?  
A. **Copilot Chat for natural-language questions**  
B. Payroll automation workflows  
C. GitHub Actions for CI/CD pipelines  
D. Enterprise proxy configuration for network routing  
**Correct Answer(s):** A  

166. Which Copilot plan integrates with **enterprise authentication and SSO**?  
A. Copilot Free, with no enterprise identity integration  
B. Copilot Individual (Pro/Pro+), with personal GitHub authentication only  
C. Copilot Business, with org governance but no dedicated enterprise identity features  
D. **Copilot Enterprise**  
**Correct Answer(s):** D  

167. Which Copilot plan allows **organization admins** to set **policy** for code suggestions?  
A. Copilot Individual (Pro/Pro+), where only personal preferences apply  
B. **Copilot Business**  
C. Copilot Enterprise, which can enforce or delegate policies across organizations  
D. Copilot Free, with no policy management  
**Correct Answer(s):** B  

168. Which Copilot plan offers **enterprise support SLAs**?  
A. Copilot Free, with community-level help only  
B. Copilot Individual (Pro/Pro+), with standard individual support  
C. Copilot Business, with org controls but no enterprise support program  
D. **Copilot Enterprise**  
**Correct Answer(s):** D  

169. Which Copilot plan is intended for teams that need **usage reporting** and **management** but **not** enterprise integrations?  
A. Copilot Free, with no org reporting or management  
B. Copilot Individual (Pro/Pro+), for single users only  
C. **Copilot Business**  
D. Copilot Enterprise, which adds enterprise identity and compliance integrations  
**Correct Answer(s):** C  

170. Which Copilot plan is designed for **individual developers** who do **not** need organizational features?  
A. Copilot Free, with limited features and no full Pro experience  
B. **Copilot Individual (Pro/Pro+)**  
C. Copilot Business, for organizations that need governance and reporting  
D. Copilot Enterprise, for enterprises with identity and compliance requirements  
**Correct Answer(s):** B  

171. Which Copilot plan allows organizations to configure **repository-level content exclusions**?  
A. Copilot Free, which has no org-level exclusion controls  
B. Copilot Individual (Pro/Pro+), which only has personal settings  
C. **Copilot Business**  
D. Copilot Enterprise, which can also enforce exclusions across organizations  
**Correct Answer(s):** C  

172. Which Copilot plan is ideal for enterprises requiring integration with **enterprise identity providers (SSO)**?  
A. Copilot Free, with no enterprise identity integration  
B. Copilot Individual (Pro/Pro+), with only personal sign-in  
C. Copilot Business, which adds org governance but not enterprise identity providers  
D. **Copilot Enterprise**  
**Correct Answer(s):** D  

173. How does Copilot help increase **developer productivity**?  
A. **By automating repetitive coding tasks and accelerating prototyping**  
B. By managing payroll and HR systems for the organization  
C. By eliminating the need for IDEs and tooling entirely  
D. By automatically generating strategic business plans  
**Correct Answer(s):** A  

174. What can developers use Copilot for when working with **unfamiliar APIs**?  
A. **Generate example code and speed up learning**  
B. Automatically produce complete, authoritative documentation for the entire API  
C. Remove or uninstall APIs from existing projects  
D. Handle licensing or contractual agreements for API usage  
**Correct Answer(s):** A  

175. Why is it important to **validate Copilot’s output** for compliance?  
A. **To ensure code meets organizational and legal requirements**  
B. Because Copilot guarantees that all generated code is fully compliant by default  
C. To eliminate the need for testing frameworks and quality checks  
D. To stop GitHub from training its models on any of your code  
**Correct Answer(s):** A  

176. How can Copilot help developers write repetitive boilerplate code?  
A. **By automatically generating common patterns and structures**  
B. By manually copying boilerplate from documentation into the codebase  
C. By outsourcing repetitive coding tasks to external developers  
D. By skipping the need to write any repetitive code at all  
**Correct Answer(s):** A  

177. How does Copilot assist with learning new frameworks or languages?  
A. By providing fully curated tutorials and long-form documentation for every framework  
B. **By generating code snippets and examples in real time**  
C. By automatically installing and configuring all required dependencies  
D. By blocking unsupported frameworks so you cannot use them  
**Correct Answer(s):** B  

178. Which scenario demonstrates Copilot helping with testing?  
A. **Copilot generates boilerplate unit tests from function definitions or selected code**  
B. Copilot deploys application code straight to production environments  
C. Copilot replaces manual QA by executing exploratory tests on its own  
D. Copilot reviews legal contracts for licensing and compliance  
**Correct Answer(s):** A  

179. Which of the following is NOT a Copilot developer use case?  
A. Generating code snippets and helper functions in your editor  
B. Writing inline documentation comments and basic explanations for code  
C. **Producing marketing slogans and non-technical advertising copy**  
D. Assisting with unit tests and simple test scaffolds  
**Correct Answer(s):** C  

180. Which of the following is a limitation of using Copilot for testing?  
A. Copilot cannot generate any unit test or test-related code at all  
B. **Generated tests may require developer review and validation**  
C. Copilot always produces perfectly correct tests with complete coverage  
D. Copilot can only write documentation and is unable to assist with tests  
**Correct Answer(s):** B  

181. How does Copilot help in test-driven development (TDD)?  
A. **By generating test templates and stubs before the implementation code is written**  
B. By eliminating the need to write or run tests altogether  
C. By deploying unfinished features directly to production environments  
D. By authoring business documentation instead of tests  
**Correct Answer(s):** A  

182. How does Copilot improve developer productivity in testing?  
A. **By suggesting boilerplate test structures, fixtures, and assertion scaffolds quickly**  
B. By removing the need to create or run any tests at all  
C. By guaranteeing that all tests always pass without failures  
D. By automatically deploying test results and code changes to production  
**Correct Answer(s):** A  

183. Which scenario shows Copilot helping developers quickly prototype ideas?  
A. **Generating quick code drafts for new features or experiments**  
B. Running payroll operations and financial processing  
C. Writing business contracts and legal agreements  
D. Performing manual QA testing in staging environments  
**Correct Answer(s):** A  

184. Which of the following demonstrates Copilot’s role in boosting developer productivity for testing?  
A. **Writing unit test templates**  
B. Drafting business proposals and product strategy documents  
C. Running HR payroll and back-office operations  
D. Designing marketing ads and campaign slogans  
**Correct Answer(s):** A  

185. Which kinds of tests can Copilot generate or scaffold?  
A. Only end-to-end tests for full production environments  
B. Only performance and load tests for benchmarking  
C. **Unit tests and integration test scaffolding**  
D. Legal compliance tests and regulatory assessments  
**Correct Answer(s):** C  

186. What should developers do **after** Copilot generates test cases?  
A. Deploy the generated tests directly to production without any review  
B. **Validate and refine the generated tests**  
C. Assume that Copilot has achieved 100% functional and edge-case coverage  
D. Ignore the generated tests entirely and always rewrite them from scratch  
**Correct Answer(s):** B  

187. Which of the following is **NOT** a valid way Copilot helps with testing?  
A. Generating test templates and boilerplate test methods  
B. Suggesting assertions and example inputs for tests  
C. **Running test frameworks automatically and reporting pass/fail status**  
D. Assisting in TDD by helping you write tests before implementation  
**Correct Answer(s):** C  

188. How can Copilot help speed up debugging?  
A. By rewriting entire projects automatically without developer input  
B. **By suggesting potential fixes or alternative implementations**  
C. By replacing QA teams and eliminating the need for testing  
D. By automatically executing all test suites and deployment pipelines  
**Correct Answer(s):** B  

189. What is an example of Copilot supporting secure coding practices?  
A. Suggesting hard-coded passwords, API keys, or secrets directly in source  
B. **Generating code that follows best practices like input validation**  
C. Writing vague, incomplete, or ambiguous code with no validation  
D. Bypassing established security libraries and controls  
**Correct Answer(s):** B  

190. How can Copilot support productivity in large projects?  
A. By automatically breaking down all large tasks into perfect sub-tasks with no input  
B. **By generating code suggestions across multiple files using workspace context**  
C. By running full project deployments and infrastructure changes  
D. By replacing all human developers on the project  
**Correct Answer(s):** B  

191. Which of the following is an example of Copilot assisting in rapid prototyping?  
A. **Generating quick code drafts for new features**  
B. Running production deployments and release pipelines  
C. Writing legal contracts and compliance documents  
D. Organizing payroll and HR operations  
**Correct Answer(s):** A  

192. Why should developers still perform **code reviews** when using Copilot?  
A. **Copilot code may include errors or insecure practices**  
B. Copilot prevents collaboration between team members  
C. Code reviews are always legally required in all jurisdictions  
D. Copilot does not work in team or organization settings  
**Correct Answer(s):** A  

193. A team wants to use GitHub Copilot to speed up development. Which practice best aligns with **responsible AI use**?  
A. Accept Copilot suggestions and commit directly to `main` without any human review or automated checks.  
B. **Treat Copilot suggestions as drafts, then review, test, and run security scans before merging**  
C. Disable unit tests and static analysis to avoid “false positives” on Copilot-generated code.  
D. Assume Copilot guarantees all generated code is secure and production-ready if you are using an Enterprise plan.  
**Correct Answer(s):** B  

194. A developer asks: “If we enable GitHub Copilot, will our **private code** be used to **train** Copilot models?” What is the correct response?  
A. Yes, all private code is automatically used to train Copilot models.  
B. Yes, but only for Enterprise organizations.  
C. Only if telemetry is turned on.  
D. **No, GitHub states that Copilot does not use your private code to train its models**  
**Correct Answer(s):** D  

195. Your organization is worried that **secrets and proprietary logic** might be sent to Copilot’s service as context. Which control most directly reduces this risk?  
A. Disable unit tests in sensitive repositories so less code is executed during CI.  
B. **Configuring content (context) exclusion for sensitive repos/paths/file types**  
C. Turning off Copilot Chat but leaving inline suggestions on.  
D. Enabling code referencing / matching public code with “Allow + show references.”  
**Correct Answer(s):** B  

196. A team wants to adopt GitHub Copilot and asks, “Can we skip code review if Copilot wrote the code?” What is the **responsible** answer?  
A. Yes, Copilot-generated code is high quality by default and can be merged without review.  
B. Yes, but only for test code, because tests are less critical than production code.  
C. **No, all Copilot-generated code must go through the same reviews, tests, and checks as human-written code**  
D. No, but only security teams need to review Copilot-generated changes; other reviewers are optional.  
**Correct Answer(s):** C  

197. A security lead worries that Copilot might accidentally reproduce **public open-source code** verbatim. Which control directly addresses this concern?  
A. Enabling content exclusion on all repositories.  
B. **Using Copilot’s duplication-detection / matching-public-code controls to block or flag similar public code**  
C. Disabling Copilot Chat but leaving inline suggestions enabled.  
D. Turning off telemetry and usage metrics.  
**Correct Answer(s):** B  

198. Which statement best reflects **responsible communication** about Copilot’s limitations to non-technical stakeholders?  
A. Copilot guarantees bug-free and secure code in all supported languages.  
B. Copilot replaces the need for unit tests, security review, and other quality checks.  
C. **Copilot accelerates development but does not guarantee correctness or security; teams remain accountable for testing and compliance**  
D. Copilot removes the need for experienced engineers, allowing teams to rely on AI alone.  
**Correct Answer(s):** C  

199. A team is worried that Copilot might reinforce **biases** (for example, biased examples in documentation or comments). Which is the most responsible action?  
A. Assume Copilot outputs are inherently neutral and adopt them without review.  
B. **Review Copilot suggestions for biased language or patterns and adjust team guidelines and prompts to encourage inclusive, policy-aligned code and docs**  
C. Disable all documentation and comment generation so Copilot only writes low-level code.  
D. Ignore potential bias concerns because they do not apply to technical artifacts like code and comments.  
**Correct Answer(s):** B  

200. Which scenario best demonstrates **responsible governance** when rolling out Copilot in an organization?  
A. Enable Copilot Enterprise for all repositories immediately, with no policies, documentation, or training.  
B. **Pilot Copilot with a small group, define acceptable-use and review guidelines, configure content exclusion and code-referencing policies, then expand based on feedback and metrics**  
C. Allow every user to define their own Copilot policies independently of enterprise governance.  
D. Disable all logging and metrics so usage remains completely anonymous and unmonitored.  
**Correct Answer(s):** B  