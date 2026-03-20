# Detailed Practice Test 05 - Answer Sheet & Explanation

**Question:** [121]  
Which instruction most improves **SQL** prompts?

**Options:**  
A. “PostgreSQL 14; given schema (tables/columns below); return top 5 customers by revenue last 30 days; output columns: id, name, revenue.”  
B. “Given schema (tables/columns below); return top 5 customers by revenue last 30 days; include window fn for rank; output columns: id, name, revenue, rank.”  
C. “Write a SQL query using the schema below to return the top 5 customers by revenue in the last 30 days; choose any appropriate columns.”  
D. **“PostgreSQL 14; given schema (tables/columns below); return top 5 customers by revenue last 30 days; include window fn for rank; output columns: id, name, revenue, rank.”**  

**Correct Answer(s):** D  

**Explanation:**  
Pinning **dialect/version**, **schema**, **time window**, and **required columns** steers Copilot away from generic or wrong SQL and toward a verifiable, project-ready query. High-quality SQL prompts should explicitly name the **SQL dialect and version**, provide the **relevant tables/columns**, describe the **business question and filters**, and specify the **output shape and ordering**, so Copilot generates syntactically correct, planner-friendly SQL for that engine instead of generic guesses.

**Tips and Tricks:**  
- Paste **schema fragments** (tables/columns) into the prompt; avoid making Copilot guess.  
- Use a repeatable pattern: **dialect + schema + business question + constraints (windowing/grouping) + output columns**, for example, “PostgreSQL 14; schema below; top 5 customers by revenue in last 30 days; use a window function for rank; return id, name, revenue, rank ordered by revenue desc.”  
- Specify **filters, aggregations, and window functions** you expect, and only ask for **EXPLAIN** when you plan to act on it.

> [!IMPORTANT]  
> SQL varies by dialect: nail the **dialect + schema + output** or you’ll invite **syntax drift**, wrong date handling, or mismatched columns. In exams, prefer prompts that lock in these details over vague “write a query” options.

**Correct and Wrong:**  
The correct prompt is the only one that pins the SQL dialect (PostgreSQL 14), the concrete schema, a precise time window (last 30 days), the required mechanism (a window function for rank), and the exact output shape (`id`, `name`, `revenue`, `rank`). The other options anchor fewer of these details, so the SQL they elicit is more vague, more ambiguous, and weaker compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[Prompt engineering with GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/guides/prompt-engineering-guide) (VS Code Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [122]  
Which prompt best directs Copilot to produce **safe code** for secrets?

**Options:**  
A. “Use an API key from an environment variable; if it’s missing, fall back to a default test key and log the value for debugging.”  
B. “Get the API key from a secrets manager or environment variable; if unavailable, continue with limited functionality and log configuration details.”  
C. **“Read API key from env var; do not hardcode; fail fast if missing; log-safe (no secrets in logs); show minimal example.”**  
D. “Store the API key in a configuration file checked into the repo; document that it should not be shared publicly.”  

**Correct Answer(s):** C  

**Explanation:**  
Security-sensitive prompts should **forbid hardcoding**, require **environment-based or secret-manager configuration**, and mandate **safe logging** and **fail-fast** behavior if configuration is missing. A prompt like “read API key from env var; do not hardcode; fail fast if missing; log-safe (no secrets in logs)” turns security rules into explicit constraints so Copilot proposes patterns that align with secure coding practices instead of convenient but unsafe shortcuts.

**Tips and Tricks:**  
- Say **“no hardcoded secrets”** and require reading from **environment variables or a secrets manager**.  
- Specify **fail-fast** behavior (clear error or exit if the secret is missing or invalid).  
- Add **logging constraints** such as “no secrets in logs” and “redact tokens” and ask for a **minimal, complete example** you can adapt into real code.

> [!IMPORTANT]  
> Security posture is **promptable**: state **non-negotiables** (no hardcoding, env/secret-store usage, safe logs, explicit failure behavior) so Copilot can’t take risky shortcuts. For exam questions, prefer prompts that spell out these rules, not vague “use an API key” or obviously unsafe “store key in source.”

**Correct and Wrong:**  
The correct prompt is the only one that clearly forbids hardcoding, insists on an environment-based secret, enforces fail-fast behavior if it’s missing, and requires log-safe handling with no secrets in logs. The other options relax one or more of these constraints (for example, falling back to default keys, continuing without failing, or logging secrets), so they are more permissive, more ambiguous, and weaker from a security perspective compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[How to write better prompts for GitHub Copilot](https://github.blog/developer-skills/github/how-to-write-better-prompts-for-github-copilot/) (GitHub Blog)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [123]  
You want Copilot to **explain** a complex file to a new teammate. Best prompt?

**Options:**  
A. “Explain this file in detail: what it does, how it works, and any important parts.”  
B. “Summarize this file for engineers: main purpose, data flows, and dependencies.”  
C. “Create a thorough explanation of this file, including architecture, flows, and risks, with no strict length limit.”  
D. **“Explain this file for a new backend hire: purpose, key data flows, external dependencies, risks; 5 bullets max.”**  

**Correct Answer(s):** D  

**Explanation:**  
Defining the **audience**, **sections**, and **length** focuses the explanation on onboarding value rather than arbitrary detail. A prompt like “explain this file for a new backend hire: purpose, key data flows, external dependencies, risks; 5 bullets max” tells Copilot who the explanation is for, which topics to cover, and how concise to be, so the result is structured, skimmable, and useful for ramp-up.

**Tips and Tricks:**  
- Name the **audience level** (for example, “new backend hire,” “SRE on-call,” “product manager”).  
- Specify **sections** (purpose, data flows, external dependencies, risks) and **cap the length** (“5 bullets,” “1 short paragraph”) to force prioritization.  
- Use follow-up prompts like **“now show a sequence diagram of the main flow”** or **“list main failure modes”** if you need deeper dives.

> [!IMPORTANT]  
> Explanations should be **scoped and structured**: the prompt should read like the **outline of the answer** you want. Exam answers that define audience, sections, and length are preferable to vague “explain this” or “long explanation” prompts.

**Correct and Wrong:**  
The correct prompt is the only one that simultaneously fixes the audience (“new backend hire”), prescribes specific sections (purpose, key data flows, external dependencies, risks), and caps the length to 5 bullets for skimmability. The other options are less constrained on audience, structure, or length, so the explanations they elicit are more vague, more open-ended, and less targeted for onboarding compared to the correct prompt.

**Source:**  
[Chat with GitHub Copilot in your IDE](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide) (GitHub Docs)  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [124]  
Which prompt targets a **performance-aware** implementation?

**Options:**  
A. **“Write a streaming JSON parser in Node.js; O(1) extra space; handle 10MB+ inputs; backpressure with streams; include benchmarks stub.”**  
B. “Write a streaming JSON parser in Node.js that can handle 10MB+ inputs and include a simple benchmark.”  
C. “Write a fast JSON parser in Node.js; it should parse 10MB+ inputs and be efficient.”  
D. “Write a JSON parser in any language; prioritize performance and document how to test its speed.”  

**Correct Answer(s):** A  

**Explanation:**  
Performance prompts must specify **language/runtime**, **space/time constraints**, **workload size**, and **mechanisms** (for example, streaming and backpressure) to avoid naive, all-in-memory solutions. A prompt like “Write a streaming JSON parser in Node.js; O(1) extra space; handle 10MB+ inputs; backpressure with streams; include benchmarks stub” fixes the runtime, sets **memory/complexity goals**, describes the **input size**, and names **streaming/backpressure** so Copilot is pushed toward an implementation that can realistically handle large payloads.

**Tips and Tricks:**  
- Declare **complexity targets** (for example, **O(1) extra space** or clear latency goals) and **workload characteristics** (10MB+ inputs, concurrency level).  
- Name the **mechanisms** you want (streams, pooling, batching, backpressure) instead of just saying “fast.”  
- Ask for a **benchmark or test stub** so you can validate performance assumptions with real measurements.

> [!IMPORTANT]  
> Non-functional goals are **first-class prompt constraints**. If you don’t name them, Copilot will optimize for convenience, not performance. In exams, the “performance-aware” option is the one that spells out **runtime, input size, complexity, and mechanisms**, not vague prompts like “fast parser please.”

**Correct and Wrong:**  
The correct prompt is the only one that locks in the runtime (Node.js), a streaming design, strict space constraints (O(1) extra space), a concrete workload size (10MB+ inputs), explicit backpressure with streams, and a benchmark stub. The other options anchor fewer of these performance details, so the implementations they elicit are more vague, more ambiguous, and weaker as performance-aware specifications compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Refactoring for performance optimization with GitHub Copilot Chat](https://docs.github.com/en/copilot/example-prompts-for-github-copilot-chat/refactoring-code/refactoring-for-performance-optimization) (GitHub Docs)  
[Prompt engineering with GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/guides/prompt-engineering-guide) (VS Code Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [125]  
Which prompt best **constrains the output format** so it can be pasted into CI?

**Options:**  
A. “List failing tests with their names and error messages in any readable format.”  
B. **“Output JSON array of failing tests with fields: name, file, line, message no prose.”**  
C. “Return failing tests as JSON with test name and message, plus a short explanation of likely causes.”  
D. “Output a human-readable report of failing tests, grouped by file, suitable for pasting into chat or email.”  

**Correct Answer(s):** B  

**Explanation:**  
Specifying a **serialization format**, the **schema** (field names), and **forbidding extra prose** yields machine-consumable output that CI/CD can parse without post-processing. A prompt like “Output JSON array of failing tests with fields: name, file, line, message no prose” defines the format (**JSON array**), the **fields**, and the constraint **“no prose”**, so you can drop the result directly into a script or pipeline.

**Tips and Tricks:**  
- Name the **format** (JSON/YAML/CSV) and **schema** (exact field names and, if needed, types).  
- Forbid prose explicitly: **“Return ONLY JSON, no explanations or comments.”**  
- If the schema is subtle, include a **tiny example object** in the prompt to lock field names and structure before generating larger outputs.

> [!IMPORTANT]  
> Format constraints convert free-form text into **structured artifacts** you can pipe to tools. More structure and an explicit schema mean **less ambiguity and fewer manual edits**. For CI-ready outputs, exam answers should lock down **format + schema + “no prose”**.

**Correct and Wrong:**  
The correct prompt is the only one that fixes both the machine-readable format (a JSON array) and a precise schema (fields `name`, `file`, `line`, `message`), while explicitly forbidding prose. The other options either leave the format open, omit key fields, or mix JSON with explanatory text, so the outputs they elicit are more vague, more ambiguous, and weaker for direct CI integration compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[GitHub Copilot Chat cookbook](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook) (GitHub Docs)  
[GitHub Copilot Chat cheat sheet](https://docs.github.com/en/copilot/reference/cheat-sheet) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [126]  
You need a **migration plan** before code. Best prompt?

**Options:**  
A. “Create a short plan to migrate this service from Flask to FastAPI, focusing on the main steps required to complete the migration.”  
B. “Outline the tasks to move this service from Flask to FastAPI and then implement the new routes in FastAPI.”  
C. **“Create a 5-step plan to migrate Flask → FastAPI; list risks, roll-back steps, and how to keep routes backward-compatible.”**  
D. “Provide FastAPI code that replicates the current Flask service’s behavior, assuming breaking changes are acceptable if they simplify the migration.”  

**Correct Answer(s):** C  

**Explanation:**  
Requesting a **short, ordered plan** with **risks** and **backward-compatibility** constraints clarifies the path and surfaces blockers before coding. A prompt like “Create a 5-step plan to migrate Flask → FastAPI; list risks, roll-back steps, and how to keep routes backward-compatible” separates **planning** from **implementation**, forces prioritization (5 steps), and ensures you consider **risk and rollback** before touching code.

**Tips and Tricks:**  
- Use a **plan → code** pattern for multi-step work: first ask for an **N-step plan with risks and rollbacks**, then follow with “implement step 1.”  
- Include **compatibility guarantees** (“keep routes backward-compatible,” “no breaking API changes”) and **rollback** expectations (how to revert safely).  
- Limit the number of steps (for example, 5) so Copilot focuses on the **most critical phases** instead of an unstructured checklist.

> [!IMPORTANT]  
> Planning prompts reduce rework: define **sequence, risks, and guardrails** so the follow-up code prompt has a stable target. In migration questions, favor prompts that explicitly mention **steps, risks, rollback, and compatibility** over “rewrite the service” or “just give me FastAPI code.”

**Correct and Wrong:**  
The correct prompt is the only one that demands a fixed-length plan (5 steps), explicitly calls out risks, rollback steps, and backward-compatible routes, and keeps planning separate from implementation. The other options either blur planning with coding, omit risks and rollback, or allow breaking changes, so the migration strategies they elicit are more vague, more ambiguous, and weaker compared to the correct prompt.

**Source:**  
[Using GitHub Copilot to migrate a project](https://docs.github.com/en/copilot/tutorials/migrate-a-project) (GitHub Docs)  
[Plan a project with GitHub Copilot](https://docs.github.com/en/copilot/tutorials/plan-a-project) (GitHub Docs)  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [127]  
Which prompt reduces **overbroad refactors** in large files?

**Options:**  
A. “Refactor the `parseHeader` logic to make it clearer and more robust across the parser code.”  
B. “Update the parser to handle invalid headers better and improve error messages throughout the file.”  
C. “Tidy up `parseHeader` and related helpers, improving structure and naming wherever it seems useful.”  
D. **“Modify only function `parseHeader`; keep public behavior; add bounds checks; return detailed errors.”**  

**Correct Answer(s):** D  

**Explanation:**  
Limiting the **edit scope** to a **named function**, maintaining **behavioral contracts**, and listing **specific changes** helps prevent Copilot from refactoring unrelated parts of a large file. This aligns with refactoring guidance, where the goal is to **change structure without changing behavior**: a prompt like “modify only function `parseHeader`; keep public behavior; add bounds checks; return detailed errors” tells Copilot *where* to work, *what must not change* (public behavior), and *what to improve* (validation and error reporting).

**Tips and Tricks:**  
- Use a pattern like: **“Edit only `<symbol>`; keep its public API and behavior unchanged; apply these specific improvements: …”**  
- Follow up with prompts such as **“show me just the updated `parseHeader` function”** or **“show only the diff for `parseHeader`”** to keep review focused.  
- Avoid vague module-level prompts (“clean up the parser module”) when you only want targeted, low-risk changes.

> [!IMPORTANT]  
> Tight scopes are the best guardrail: **smaller edit surface + explicit invariants (API/behavior)** = safer refactors. In exams, prefer the option that names a specific function/class, preserves behavior, and lists targeted edits over broad “improve/clean up/rewrite” prompts.

**Correct and Wrong:**  
The correct prompt is the only one that constrains edits to a single named function, preserves its public behavior, and specifies concrete improvements (bounds checks and detailed errors). The other options expand the scope to the file or related helpers and omit explicit behavior invariants, so the refactors they elicit are more vague, more ambiguous, and risk overbroad changes compared to the correct prompt.

**Source:**  
[Refactor code with GitHub Copilot](https://docs.github.com/en/copilot/tutorials/refactor-code) (GitHub Docs)  
[Refactor to implement a design pattern](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook/refactor-code/refactor-design-patterns) (GitHub Docs)  
[Best practices for using GitHub Copilot](https://docs.github.com/en/copilot/get-started/best-practices) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [128]  
How do you prompt for **secure HTTP handling**?

**Options:**  
A. **“Use HTTPS; validate TLS certs; set timeouts and retries; redact secrets in logs; handle 429/5xx with backoff.”**  
B. “Call the API over HTTPS and log the full request and response body for debugging if something goes wrong.”  
C. “Use HTTPS with a reasonable timeout and retry a few times on failure.”  
D. “Call the API with HTTPS but skip strict certificate validation to avoid connection issues.”  

**Correct Answer(s):** A  

**Explanation:**  
Security and reliability require explicit **protocol and validation** (**HTTPS** and **TLS cert validation**), **timeouts and retry/backoff behavior**, and **safe logging** that avoids exposing secrets. A prompt like “Use HTTPS; validate TLS certs; set timeouts and retries; redact secrets in logs; handle 429/5xx with backoff” turns these into concrete requirements so Copilot generates code that is both safer and more resilient than a simple “call the API” or “fetch data fast” request.

**Tips and Tricks:**  
- State **non-negotiables** clearly: “**must use HTTPS and validate TLS certificates**.”  
- Require **timeouts**, **retry policy**, and **backoff** for **429/5xx** responses, not just a single HTTP call.  
- Forbid secret logging explicitly: “**never log tokens or secrets; redact sensitive fields**,” and request a **small, focused example** you can adapt to your real HTTP client.

> [!IMPORTANT]  
> Non-functional requirements like **security** and **reliability** must be **prompted**, or the model will optimize for convenience over safety. Exam-wise, pick prompts that treat HTTPS, cert validation, timeouts, backoff, and log redaction as **must-haves**, not optional details.

**Correct and Wrong:**  
The correct prompt is the only one that combines HTTPS, strict TLS certificate validation, explicit timeouts and retries, structured handling for 429/5xx with backoff, and log redaction for secrets. The other options either over-log sensitive data, omit cert validation, or skip backoff and error-handling details, so the HTTP code they elicit is more vague, more ambiguous, and weaker from a secure and reliable perspective compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Network and certificate requirements for GitHub Copilot](https://docs.github.com/en/copilot/concepts/network-settings) (GitHub Docs)  
[Best practices for using GitHub Copilot](https://docs.github.com/en/copilot/get-started/best-practices) (GitHub Docs)  
[HTTP logging in ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/http-logging) (Microsoft Learn)

**Question:** [129]  
Which prompt best avoids **unsupported library calls**?

**Options:**  
A. “Use Redis with a standard client library and configure basic connection settings for your environment.”  
B. “Initialize Redis in Python using redis-py and show how to set and get a key for caching.”  
C. “Use Redis for caching in your service and choose any compatible client version that works with your stack.”  
D. **“Python 3.11; redis-py v5 only; use `Redis.from_url`; no deprecated APIs; include connection timeout and health check.”**  

**Correct Answer(s):** D  

**Explanation:**  
Pinning the **runtime** (Python 3.11), **library and version** (**redis-py v5**), and **allowed constructor** (`Redis.from_url`), plus disallowing deprecated APIs and requiring **timeouts/health checks**, reduces the chance that Copilot will suggest methods that don’t exist or have changed in your chosen version. This turns a vague “use Redis” request into a **version-locked, verifiable stub** that should compile cleanly against your dependency set.

**Tips and Tricks:**  
- Lock **language/runtime** and **library version**, for example, “Python 3.11; redis-py v5 only.”  
- Allowlist specific APIs: “**use `Redis.from_url`; do not use deprecated methods**,” and ask for a **minimal init + usage example** with **connection timeout** and a simple **health check**.  
- Compile immediately after generating code so any hallucinated or deprecated symbols are caught early.

> [!IMPORTANT]  
> To avoid unsupported calls, **version-lock + allowlist** your dependencies in the prompt. In exam questions, the correct answer is the one that **pins runtime, library version, and constructor** and forbids deprecated APIs, not “use Redis” or “any version is fine,” which invite Copilot to guess from mixed-version training data.

**Correct and Wrong:**  
The correct prompt is the only one that pins the runtime (Python 3.11), locks the client version (redis-py v5), specifies the constructor (`Redis.from_url`), forbids deprecated APIs, and requires both timeouts and a health check. The other options anchor fewer of these details, so the Redis code they elicit is more vague, more ambiguous, and weaker at avoiding unsupported or deprecated calls compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Concepts for prompting GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting) (GitHub Docs)  
[Best practices for using GitHub Copilot](https://docs.github.com/en/copilot/get-started/best-practices) (GitHub Docs)  
[GitHub Copilot prompt engineering examples](https://github.com/services/github-copilot-prompt-engineering) (GitHub, docs-linked)  

**Question:** [130]  
Best way to ask for a **configurable CLI tool**?

**Options:**  
A. **“Create a Python CLI with `argparse`; flags: `--input`, `--format (json|csv)`, `--verbose`; validate files; exit codes 0/2; examples.”**  
B. “Write a Python CLI that accepts some arguments and prints a result based on the input.”  
C. “Create a CLI script in any language that processes an input file and prints output to the console.”  
D. “Set up a simple command-line entry point without worrying about validation, exit codes, or detailed help text.”  

**Correct Answer(s):** A  

**Explanation:**  
Specifying **language/library** (`argparse`), **flags and types**, **validation rules**, and **exit codes**, plus asking for **usage examples**, turns a vague “write a CLI” request into a concrete UX and behavior spec that Copilot can implement consistently. The prompt locks in **Python + `argparse`**, enumerates flags and allowed values, requires validation, and defines exit codes and examples, matching guidance to treat **CLI UX and behavior as part of the prompt spec**, not something Copilot invents.

**Tips and Tricks:**  
- Use a template like: **“Create a \<language\> CLI with \<library\>; flags: …; validate …; exit codes …; include usage examples/help text.”**  
- List **flags**, their **types**, and any **allowed values** (for example, `--format (json|csv)`), and define when to return **exit code 0 vs 2**.  
- Ask for **help/usage examples** so you can reuse them in `--help` output or documentation.

> [!IMPORTANT]  
> UX is part of the spec: a **configurable CLI** prompt should read like a mini-spec, covering **language + library + flags/types + validation + exit codes + examples**. That structure distinguishes the correct exam answer from vague “write a CLI” distractors.

**Correct and Wrong:**  
The correct prompt is the only one that fixes the language (Python), library (`argparse`), a concrete flag set (`--input`, `--format (json|csv)`, `--verbose`), validation requirements, specific exit codes (0/2), and usage examples. The other options leave language, flags, validation, or exit behavior under-specified, so the CLIs they elicit are more vague, more ambiguous, and weaker as configurable tools compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Prompt engineering with GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/guides/prompt-engineering-guide) (VS Code Docs)  
[Getting started with prompts for GitHub Copilot Chat](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/get-started-with-chat) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)  

**Question:** [131]  
How to prompt for a **safe database migration**?

**Options:**  
A. “Add a new `status` column and update the application to start using it, then remove old fields later if needed.”  
B. “Update the schema and data to support a `status` field in a way that works for your database engine.”  
C. **“Add column `status` (ENUM) with default ‘new’; backfill from `state`; online migration (no downtime); include rollback SQL.”**  
D. “Redesign the schema to better model status and deploy the changes during a low-traffic window, accepting some downtime.”  

**Correct Answer(s):** C  

**Explanation:**  
Migrations need **exact DDL**, **backfill rules**, an **online strategy** (no downtime), and a clear **rollback** path so changes can ship safely without blocking deploys or corrupting data. A prompt like “Add column `status` (ENUM) with default ‘new’; backfill from `state`; online migration (no downtime); include rollback SQL” describes the schema change, how to derive values from existing data, and how to **roll back** if needed.

**Tips and Tricks:**  
- Name the **DDL** precisely (new columns, types, defaults), not just “change the schema.”  
- Define **backfill/derivation** rules from existing data (for example, derive `status` from `state`).  
- Require an **online migration strategy** (no downtime) and **rollback SQL** so you have a safe escape hatch in case of issues.

> [!IMPORTANT]  
> Operational prompts should include **safety rails**: explicit **defaults**, **backfill**, **online/no-downtime requirements**, and **rollback**. In exam questions, prefer prompts that treat migrations as production operations with guardrails, not “make DB updates” or “rewrite tables.”

**Correct and Wrong:**  
The correct prompt is the only one that pins the exact DDL (ENUM column with default ‘new’), specifies how to backfill from existing `state`, requires an online migration with no downtime, and demands rollback SQL. The other options are looser on defaults, backfill rules, downtime, or rollback, so the migrations they elicit are more vague, more ambiguous, and weaker from a safety and operability perspective compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Plan a project with GitHub Copilot](https://docs.github.com/en/copilot/tutorials/plan-a-project) (GitHub Docs)  
[Using GitHub Copilot to migrate a project](https://docs.github.com/en/copilot/tutorials/migrate-a-project) (GitHub Docs)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)  

**Question:** [132]  
Which prompt best constrains **logging** for privacy?

**Options:**  
A. “Add JSON logs with level and message, and include full request and response bodies to simplify debugging.”  
B. “Add structured logs with level, event, and user details; include tokens in debug mode to help trace issues.”  
C. **“Add structured JSON logs: level, event, requestId; no PII; redact tokens; include error stack; single line per event.”**  
D. “Enable verbose logging across the service, capturing all available fields by default and filtering sensitive data later if needed.”  

**Correct Answer(s):** C  

**Explanation:**  
Privacy-aware logging specifies **structure**, **fields**, and **redaction rules** so logs stay machine-parsable and do not leak secrets or PII. A prompt like “Add structured JSON logs: level, event, requestId; no PII; redact tokens; include error stack; single line per event” defines the log **schema**, **correlation IDs**, **redaction behavior**, and **one-event-per-line** constraint.

**Tips and Tricks:**  
- Define a **schema** (fields like `level`, `event`, `requestId`, `error`) and require **single-line events** for log shipping.  
- Forbid **PII and secrets** explicitly (“no PII; redact tokens”) and require **redaction** or omission of sensitive fields.  
- Include **correlation IDs** (for example, `requestId`, `traceId`) so you can follow a request through distributed systems.

> [!IMPORTANT]  
> Structured, redacted logs are both **safer** and **easier to analyze**. Make privacy constraints explicit in the prompt (“no PII; redact tokens; structured JSON”) so Copilot doesn’t default to dumping raw objects or secrets. Exam questions favor prompts that encode **structure + privacy rules**, not “verbose logs” or “log everything.”

**Correct and Wrong:**  
The correct prompt is the only one that fixes a structured JSON format, a clear schema (`level`, `event`, `requestId`, error stack), and strict privacy rules (no PII, redacted tokens, single line per event). The other options either over-log sensitive data (full bodies, user details, tokens), lack a precise schema, or rely on filtering later, so the logs they elicit are more vague, more ambiguous, and weaker from a privacy-preserving perspective compared to the correct prompt.

**Source:**  
[Prompt engineering for GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering) (GitHub Docs)  
[Best practices for using GitHub Copilot](https://docs.github.com/en/copilot/get-started/best-practices) (GitHub Docs)  
[HTTP logging in ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/http-logging) (Microsoft Learn)  
[Introduction to prompt engineering with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) (Microsoft Learn)

**Question:** [133]  
Which plan offers **enterprise proxy support** and integration with **advanced compliance** capabilities?

**Options:**  
A. Copilot Free, for individuals without governance or compliance controls  
B. Copilot Individual (Pro/Pro+), with premium personal features only  
C. **Copilot Enterprise**  
D. Copilot Business, with org-level license management and policies but not full enterprise compliance integrations  

**Correct Answer(s):** C  

**Explanation:**  
**Copilot Enterprise** is the **enterprise-tier** plan for GitHub Enterprise Cloud organizations. It includes all **Copilot Business** capabilities (centralized management, org policies, content exclusion, Copilot audit logs) and adds **enterprise-grade features** such as deeper integration with **enterprise identity and governance**, **advanced compliance support**, and enterprise-level network controls like subscription-based routing and **proxy/allowlisting** configuration at the enterprise scope.

**Tips and Tricks:**  
- Treat **Business** as providing **org governance** (seat management, policies, content exclusion, Copilot audit logs), and **Enterprise** as extending this with **enterprise identity, compliance, and advanced network routing controls**.  
- If the stem mentions **enterprise-wide proxy or network routing controls** plus **advanced compliance/audit posture**, choose **Copilot Enterprise** over Business or Individual tiers.

> [!IMPORTANT]  
> **Copilot Enterprise** builds on **Copilot Business** by combining org-level controls (policies, content exclusion, audit logs) with **enterprise integrations** for identity, compliance, and **network access controls** (for example, subscription-based network routing and proxy/allowlisting), which are not available on Individual/Free tiers.

**Correct and Wrong:**  
The correct option is the only one that combines **enterprise-grade network access controls and identity/compliance integrations** via **Copilot Enterprise**, while Copilot Business stops at **org-level governance**, and Individual/Free plans provide **no enterprise network or compliance integration**.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Setting up GitHub Copilot for your enterprise](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/set-up/set-up-for-enterprise) (GitHub Docs)  
[Manage Copilot access to your enterprise’s network](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-access/manage-network-access) (GitHub Docs)  
[Manage Copilot access to your organization’s network](https://docs.github.com/en/enterprise-cloud%40latest/copilot/how-tos/administer-copilot/manage-for-organization/manage-access/manage-network-access) (GitHub Docs)

**Question:** [134]  
Which plan includes **organization-level** controls like **content exclusion** and **usage visibility**?

**Options:**  
A. Copilot Free  
B. Copilot Individual (Pro/Pro+)  
C. **Copilot Business**  
D. Copilot Enterprise  

**Correct Answer(s):** C  

**Explanation:**  
**Copilot Business** is the first **organization-level** Copilot plan that introduces **admin controls** such as **content exclusion** and **usage visibility/reporting**. Org and enterprise admins on Business can configure content exclusion to prevent Copilot from accessing specific repositories or paths, and they can review activity and usage data for members who have Business seats. **Copilot Enterprise** includes all Copilot Business capabilities (so it also has these controls) but adds extra enterprise-grade features; however, when an exam question asks which plan includes **org-level controls like content exclusion and usage visibility**, the intended “nearest” answer is the **Business** plan, not Free or Individual.  

**Tips and Tricks:**  
- Treat **“content exclusion + org usage/entitlement visibility + license/seat management”** as a strong signal for **Copilot Business** (and remember that **Enterprise inherits these**).  
- If a question mentions **organization admins**, **org-wide policies**, or **reviewing Copilot usage for members**, think **Business/Enterprise**, not Free or Individual.  
- Remember: **Free** and **Individual (Pro/Pro+)** are **developer-focused** plans with no shared admin governance—no org content exclusion, no org usage reports, and no org policy surface.  

> [!IMPORTANT]  
> **Org-level governance features (content exclusion, usage visibility, license management) start with Copilot Business and carry into Copilot Enterprise.** These features let admins restrict which repositories/paths Copilot can use as context and review how Copilot is being used across the org. When exam stems emphasize **“organization-level controls,” “content exclusion,” or “usage reports for members,”** they are pointing you away from Free/Individual and toward **Copilot Business as the baseline plan**.

**Correct and Wrong:**  
**Copilot Business** is the best answer because it’s the first Copilot plan that introduces **organization-level admin controls**, including content exclusion and usage visibility, while Free and Individual plans have no shared governance surface at all. Copilot Enterprise also includes these controls but is primarily differentiated by additional **enterprise-grade compliance, identity, and network features**, so for stems targeting org-level content exclusion and usage visibility, **Business** is the intended and nearest correct choice.

**Source:**  
[Content exclusion for GitHub Copilot](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Configure and audit content exclusion](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion) (GitHub Docs)  
[Monitoring your GitHub Copilot usage and entitlements](https://docs.github.com/en/copilot/how-tos/manage-and-track-spending/monitor-premium-requests) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Managing GitHub Copilot in your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization) (GitHub Docs)

**Question:** [135]  
Which plan includes **audit logs** and advanced **compliance** controls?

**Options:**  
A. Copilot Free  
B. Copilot Individual (Pro/Pro+)  
C. Copilot Business  
D. **Copilot Enterprise**

**Correct Answer(s):** D  

**Explanation:**  
**Copilot Enterprise** is designed for **GitHub Enterprise Cloud** customers who need **advanced compliance and governance** on top of org-level controls. It includes all **Copilot Business** capabilities (centralized license management, policies, content exclusion, and Copilot audit logs) and adds **enterprise-grade features** such as deeper integration with **enterprise identity and governance**, **advanced compliance support**, and **enterprise-level network controls** like proxy/allowlisting and network routing.

**Tips and Tricks:**  
- Treat **audit logs + enterprise identity + advanced compliance** as strong signals for **Copilot Enterprise** rather than Business.  
- Remember that **Copilot Business** already provides **org governance** (content exclusion, license management, usage visibility) but not the same depth of **enterprise compliance integrations**.  
- If a stem explicitly calls out **enterprise-wide governance, compliance posture, or enterprise network controls**, choose **Copilot Enterprise** over Business, Individual, or Free.

> [!IMPORTANT]  
> **Audit logs alone are not exclusive to Copilot Enterprise**, Copilot Business also exposes Copilot-specific audit events. Exam questions that stress **advanced compliance, enterprise identity, or enterprise network controls** are pointing you to **Copilot Enterprise**, not just any plan with basic auditing.

**Correct and Wrong:**  
**Copilot Enterprise** is the best answer because it combines all org-level capabilities from Copilot Business, including audit logs, with additional **enterprise identity, compliance, and network controls** required in regulated environments. Copilot Business offers governance and auditing but doesn’t extend as far into enterprise compliance integrations, while Individual and Free plans lack any organizational or enterprise-level compliance or audit features.

**Source:**  
[Reviewing audit logs for GitHub Copilot Business](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Choosing your enterprise's plan for GitHub Copilot](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  
[Security and compliance](https://docs.github.com/en/enterprise-cloud@latest/admin/concepts/security-and-compliance) (GitHub Docs)  
[About GitHub Copilot Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/set-up/set-up-for-enterprise) (GitHub Docs)

**Question:** [136]  
What’s the practical difference between **Copilot Edits – Edit mode** and **Agent mode**?

**Options:**  
A. Edit auto-merges; Agent requires reviews  
B. **Edit = user-scoped diffs; Agent = autonomous, multi-step execution that may culminate in a PR**  
C. Edit is IDE-only; Agent is GitHub.com only  
D. Edit reads the repo; Agent can’t  

**Correct Answer(s):** B  

**Explanation:**  
With **Copilot Edits – Edit mode**, you keep tight control: you pick which files Copilot may change, review the proposed diffs, and apply them incrementally. With **Agent mode**, Copilot can **plan and execute a multi-step workflow**—it can inspect the broader project, choose relevant files, run tools or commands, and iterate until the task is complete. The practical difference is **scope and autonomy**: Edit mode is **user-scoped diffs**, while Agent mode is **autonomous orchestration** across files and tools, which in practice often feeds into changes that eventually end up in a pull request for review.

**Tips and Tricks:**  
- Use **Edit mode** for **surgical changes** where you want to tightly control which files are touched and inspect every diff.  
- Use **Agent mode** when you need **multi-step automation** across files, tests, and tooling (for example, refactors plus test updates plus build fixes).  
- Keep **branch protections and code reviews** in place; even with Agent mode, Copilot does not auto-merge or bypass your approval process.

> [!IMPORTANT]  
> Think **control vs autonomy**: **Edit mode** = you pick files and apply diffs; **Agent mode** = Copilot picks files, runs tools, and orchestrates multi-step work. Exams usually reward answers that highlight this difference in **scope and autonomy**, not claims about auto-merging or GitHub.com vs IDE.

**Correct and Wrong:**  
The correct option is the only one that captures **Edit mode** as **user-scoped diffs** and **Agent mode** as **autonomous, multi-step orchestration**. The other options incorrectly claim auto-merging behavior, pretend Agent mode is limited to GitHub.com, or assert that Agent cannot read the repo, none of which matches the documented behavior.

**Source:**  
[GitHub Copilot features (Edits & modes)](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Copilot ask, edit, and agent modes: what they do and when to use them](https://github.blog/ai-and-ml/github-copilot/copilot-ask-edit-and-agent-modes-what-they-do-and-when-to-use-them/) (GitHub Blog)  
[Agent mode 101: all about GitHub Copilot’s powerful mode](https://github.blog/ai-and-ml/github-copilot/agent-mode-101-all-about-github-copilots-powerful-mode/) (GitHub Blog)  
[Introducing Copilot agent mode in VS Code](https://code.visualstudio.com/blogs/2025/02/24/introducing-copilot-agent-mode) (Microsoft/VS Code Blog)  

**Question:** [137]  
What is the **minimum length** Copilot’s duplication-detection filter considers when blocking **exact matches**?

**Options:**  
A. 50 characters  
B. **150 characters**  
C. 500 characters  
D. 1,000 characters  

**Correct Answer(s):** B  

**Explanation:**  
Copilot’s duplication-detection behavior (surfaced through **“suggestions matching public code”** and code referencing) uses a window of about **150 characters** of surrounding code to detect matches against public GitHub repositories. When suggestions of roughly **150 characters or more** match public code and blocking is enabled, Copilot can suppress those suggestions instead of showing them. This threshold helps avoid generating long verbatim sequences while still allowing shorter or more original suggestions.

**Tips and Tricks:**  
- Remember **150 characters** as the key length where Copilot’s public-code matching starts treating suggestions as “long segments” that may be blocked.  
- The mechanism is **pattern/length-based**, not a legal engine; it doesn’t interpret licenses, it just detects and handles long matches to public repositories.  
- Use **code referencing** to allow similar code with references, and use the **block** posture when your policy forbids matching public code at all.

> [!IMPORTANT]  
> For exam purposes, associate **“long exact match”** and **“≈150 characters or more”** with Copilot’s public-code matching safeguards. If a stem asks for the **minimum length** at which Copilot starts treating an exact match as “long,” the expected answer is **150 characters**, not larger thresholds like 500 or 1,000.

**Correct and Wrong:**  
The correct option is the only one that reflects the documented **150-character** behavior used in Copilot’s public-code matching. The other thresholds are either unrealistically small (50) or large (500, 1,000) and don’t align with how GitHub describes when Copilot starts handling long exact matches differently.

**Source:**  
[Introducing code referencing for GitHub Copilot](https://github.blog/news-insights/product-news/introducing-code-referencing-for-github-copilot/) (GitHub Blog)  
[Code referencing now GA in GitHub Copilot with Azure AI](https://github.blog/news-insights/product-news/code-referencing-now-generally-available-in-github-copilot-and-with-microsoft-azure-ai/) (GitHub Blog)  
[Managing GitHub Copilot policies as an individual subscriber](https://docs.github.com/en/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)  
[Finding public code that matches GitHub Copilot suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  

**Question:** [138]  
Which plan provides **organizational license management** and **usage reporting** **without** enterprise integrations (like audit logs/SSO)?

**Options:**  
A. Copilot Free  
B. Copilot Individual (Pro/Pro+)  
C. **Copilot Business**  
D. Copilot Enterprise  

**Correct Answer(s):** C  

**Explanation:**  
**Copilot Business** is the first plan that provides **organization-level license management and usage reporting**, along with policy controls such as content exclusion. Organization and enterprise owners on Business can assign Copilot seats, download detailed **activity and usage reports**, and configure policies for their members. **Copilot Enterprise** includes all of these capabilities and adds deeper **enterprise-grade integrations** for identity, compliance, and governance. For exam purposes, when a stem asks for organizational license management and usage reporting **without** the full set of enterprise compliance and identity integrations, **Copilot Business** is the intended answer.

**Tips and Tricks:**  
- Map **“license management + usage/activity reporting + content exclusion”** to **Copilot Business** as the baseline org-governance plan.  
- Reach for **Copilot Enterprise** when the stem stresses **enterprise identity, advanced compliance posture, or enterprise-level network controls**, not just license/usage.  
- **Free** and **Individual (Pro/Pro+)** subscriptions are **self-managed**; they do not expose an org admin surface for central seat assignment, org usage reporting, or content exclusion.

> [!IMPORTANT]  
> Think in terms of a **governance staircase**: Free/Individual have no org governance, **Business** adds organizational seat management, usage reporting, and policies, and **Enterprise** layers on additional **enterprise identity, compliance, and network controls**. When the question highlights **license management and usage reporting** but not advanced enterprise compliance integrations, **Copilot Business** is the closest fit.

**Correct and Wrong:**  
**Copilot Business** is correct because it’s the first plan that introduces **centralized license management and usage reporting** for organizations. Copilot Enterprise also includes these features but is primarily chosen when a question emphasizes **enterprise-wide identity, compliance, or network controls**. Copilot Free and Individual plans don’t provide any org-level license management or usage reporting, so they cannot satisfy the stem.

**Source:**  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[Downloading a GitHub Copilot activity report](https://docs.github.com/en/copilot/how-tos/administer-copilot/download-activity-report) (GitHub Docs)  
[Reviewing audit logs for GitHub Copilot Business](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-organization/review-activity/review-audit-logs) (GitHub Docs)  
[Choosing your enterprise's plan for GitHub Copilot](https://docs.github.com/en/copilot/get-started/choose-enterprise-plan) (GitHub Docs)  

**Question:** [139]  
Which of the following is an **advanced developer use case** for Copilot?

**Options:**  
A. **Helping explore unfamiliar APIs and libraries**  
B. Automating end-to-end payroll and compliance processing for HR teams  
C. Drafting legally binding corporate contracts without human review  
D. Managing calendar invites, meeting rooms, and company-wide scheduling  

**Correct Answer(s):** A  

**Explanation:**  
GitHub Copilot and Copilot Chat are designed to act as an **AI pair programmer**, helping you understand and use **new APIs and libraries** by generating example calls, scaffolding common patterns, and explaining code and errors in natural language. When working with an unfamiliar SDK or framework, you can ask Copilot Chat to propose usage examples, explain parameters, and even generate tests, turning exploration of new APIs into an iterative, guided workflow.

**Tips and Tricks:**  
- Use Copilot Chat with **selected code** (for example, using explain/fix-style prompts) to understand what unfamiliar API calls are doing.  
- Ask for **minimal runnable examples** and **unit tests** that exercise specific endpoints or methods, then run them locally to validate behavior.  
- Always cross-check Copilot’s examples against the **official API documentation** and the versions you actually use; include the correct version or package name in your prompts to reduce hallucinations.

> [!IMPORTANT]  
> Exploring new APIs and libraries is a **prime developer use case** for Copilot, unlike automating sensitive business workflows such as payroll or legal contracts. Exams will reward answers that focus on **developer-centric assistance** code, tests, explanations, and scaffolds rather than non-technical business operations.

**Correct and Wrong:**  
The correct option is the only one that reflects a **developer-focused** use case Copilot is explicitly designed for: helping you work effectively with **unfamiliar APIs and libraries**. The other options describe HR, legal, or administrative tasks (payroll, contracts, scheduling) that are outside Copilot’s intended scope as a coding assistant.

**Source:**  
[About GitHub Copilot Chat](https://docs.github.com/en/copilot/concepts/chat) (GitHub Docs)  
[GitHub Copilot code suggestions in your IDE](https://docs.github.com/en/copilot/concepts/completions/code-suggestions) (GitHub Docs)  
[GitHub Copilot Chat cookbook](https://docs.github.com/en/copilot/tutorials/copilot-chat-cookbook) (GitHub Docs)  
[Developer use cases for AI with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/developer-use-cases-for-ai-with-github-copilot/) (Microsoft Learn)

**Question:** [140]  
Which plan provides features like **license management** and **content exclusion** for organizations?

**Options:**  
A. Copilot Individual (Pro/Pro+)  
B. **Copilot Business**  
C. Copilot Enterprise  
D. Copilot Free  

**Correct Answer(s):** B  

**Explanation:**  
**Copilot Business** is the first **organization-level** Copilot plan that enables **centralized license management**, **usage visibility**, and **content exclusion**. Organization owners can assign Copilot seats, download activity and usage reports, and configure content exclusion rules so Copilot cannot use specific repositories, paths, file types, or patterns as context. **Copilot Enterprise** also includes these capabilities, but adds further enterprise-level identity, compliance, and network controls. For stems that mention **license management and content exclusion for organizations**, **Business** is the closest fit beyond Free or Individual.

**Tips and Tricks:**  
- Associate **“license/seat management + usage visibility + content exclusion”** with **Copilot Business** (and remember **Enterprise inherits** these).  
- If the stem only mentions **org-admin controls** like seats, usage, and exclusions, choose **Business** unless it explicitly adds **enterprise identity/compliance/network** requirements.  
- **Free/Individual** plans are **developer-focused** and don’t expose any org-level admin layer for seat assignment, usage reporting, or content exclusion.  

> [!IMPORTANT]  
> Think of **Copilot Business** as the **org governance starter pack**: license management, usage visibility, and content exclusion. **Copilot Enterprise** adds **enterprise identity, compliance, and network controls**, but does not replace Business for these basics. If a question mentions **“license management + content exclusion for organizations”** without enterprise-specific requirements, **Copilot Business** is the intended answer.

**Correct and Wrong:**  
**Copilot Business** is correct because it is the first plan to give **organization admins** license management, usage visibility, and content exclusion controls. Copilot Enterprise also has these features but is chosen when the stem emphasizes **enterprise identity, compliance, or network controls**, while Individual and Free plans have no org-level governance at all.

**Source:**  
[Excluding content from GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Configure and audit content exclusion](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/configure-content-exclusion) (GitHub Docs)  
[Managing policies and features for GitHub Copilot in your enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Admin controls for GitHub Copilot in Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/visual-studio-github-copilot-admin) (Microsoft Learn)  

**Question:** [141]  
Which setting governs **similar-but-not-exact** suggestions that resemble public code?

**Options:**  
A. Content exclusion  
B. **Code referencing (matching public code)**  
C. Duplication-detection filter  
D. Usage reporting  

**Correct Answer(s):** B  

**Explanation:**  
**Code referencing** is the mechanism Copilot uses when you allow suggestions that **match or resemble public code**. The policy for suggestions that match public code can be set to **block** these suggestions entirely, or **allow them and show references**, in which case Copilot surfaces links to the public repositories where similar code was found. This setting governs how Copilot handles **similar-but-not-exact** public-code matches, whereas long exact matches are controlled by duplication-detection filters, and content exclusion only controls which inputs Copilot can see.

**Tips and Tricks:**  
- Map **“similar public code behavior”** to **code referencing**, configured via the **suggestions matching public code** policies.  
- Reserve **duplication-detection filters** for **long exact or near-exact** matches, and **content exclusion** for limiting the repositories and paths Copilot can use as context.  
- Remember that code referencing policies can be governed at **user, organization, or enterprise** level, with higher-level policies overriding lower ones.  

> [!IMPORTANT]  
> When a stem focuses on **“similar-but-not-exact suggestions that resemble public code”**, it is pointing to **code referencing** and the **suggestions matching public code** policy. Duplication filters handle **long exact matches**, and content exclusion sets **input boundaries**, not output similarity.

**Correct and Wrong:**  
The correct option is the only one that matches how Copilot handles **similar** public-code suggestions: **code referencing** policies decide whether to block them or allow them with references. The other options either handle long exact matches (duplication filter), control what Copilot can see as input (content exclusion), or only provide observability (usage reporting), so they do not directly govern similar-but-not-exact suggestions.

**Source:**  
[About Copilot code referencing](https://docs.github.com/en/copilot/concepts/completions/code-referencing) (GitHub Docs)  
[Finding public code that matches GitHub Copilot suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  
[Managing policies and features for GitHub Copilot in your enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Code referencing now GA in GitHub Copilot and with Azure AI](https://github.blog/news-insights/product-news/code-referencing-now-generally-available-in-github-copilot-and-with-microsoft-azure-ai/) (GitHub Blog)  

**Question:** [142]  
When **code referencing** is set to **“Allow + show references”**, what should you expect?

**Options:**  
A. Copilot blocks all similar suggestions  
B. **Copilot may show the suggestion with links to public sources**  
C. Duplication filter is disabled  
D. Content exclusion is ignored  

**Correct Answer(s):** B  

**Explanation:**  
When **code referencing** is configured to **“Allow + show references”**, Copilot can surface suggestions that **match or resemble public code** and attach **references to public repositories** where similar code appears. This lets developers review the origin of the code and make informed decisions about attribution and licensing before accepting the suggestion. The **duplication-detection filter** still applies to long exact matches, and **content exclusion** still controls which repositories and paths Copilot can use as context.

**Tips and Tricks:**  
- Use **Allow + show references** when your workflow requires **transparency and due diligence** on public-code matches rather than outright blocking.  
- Switch the policy to **Block** if organizational rules prohibit suggestions that match public code.  
- These settings do **not** disable the duplication filter or content exclusion; those mechanisms continue to enforce **long exact-match blocking** and **input boundaries**, respectively.  

> [!IMPORTANT]  
> “**Allow + show references**” is about **visibility**, not automatic legal approval. It helps you see where similar public code comes from, but you still need your normal **review, approval, and licensing checks** in place.

**Correct and Wrong:**  
The correct option is the only one that matches the documented behavior: when code referencing is set to **“Allow + show references”**, Copilot can show the suggestion **with links to public sources**. The other options incorrectly claim that Copilot blocks everything, disables the duplication filter, or ignores content exclusion none of which align with how the feature actually works.

**Source:**  
[Finding public code that matches GitHub Copilot suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  
[About Copilot code referencing](https://docs.github.com/en/copilot/concepts/completions/code-referencing) (GitHub Docs)  
[Managing policies and features for GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-enterprise-policies) (GitHub Docs)  
[Code referencing now GA in GitHub Copilot and with Azure AI](https://github.blog/news-insights/product-news/code-referencing-now-generally-available-in-github-copilot-and-with-microsoft-azure-ai/) (GitHub Blog)

**Question:** [143]  
At what **scopes** can you configure **code referencing** behavior?

**Options:**  
A. Only repository level  
B. **Individual account and org/enterprise policies**  
C. Only enterprise level  
D. Only IDE settings  

**Correct Answer(s):** B  

**Explanation:**  
**Code referencing** and related **“suggestions matching public code”** behavior are controlled by **policies at multiple scopes**. As an individual, you can configure whether to **block** suggestions that match public code or **allow + show references**, unless your setting is overridden by your **organization or enterprise**. Organization and enterprise owners can define policies that apply to all users who receive Copilot seats through them, and these higher-level policies take precedence over individual preferences. Repo-only or IDE-only scopes are not how code referencing is governed in GitHub’s model.

**Tips and Tricks:**  
- Remember the policy stack: **enterprise → organization → individual**; higher levels can enforce stricter behavior for code referencing.  
- Use **individual settings** when working in **personal repos** or when your org/enterprise hasn’t enforced stricter policies.  
- Think of **code referencing** as controlled by **Copilot policies**, not by repository-level toggles or IDE-only switches.  

> [!IMPORTANT]  
> Policy hierarchy matters: **enterprise owners** can enforce code referencing behavior across all orgs, **org owners** can set policies for their org, and **individuals** can only tune settings when higher-level policies allow it. Exam stems that mention **account settings plus org/enterprise policies** are pointing to **multi-scope configuration**, not a single repository or IDE-only setting.

**Correct and Wrong:**  
The correct option is the only one that reflects the real **multi-scope policy model**: individuals plus org/enterprise policies. The other options incorrectly restrict configuration to a single scope (repository-only, enterprise-only, or IDE-only), which does not match how Copilot policies actually work.

**Source:**  
[Managing Copilot policies as an individual subscriber](https://docs.github.com/en/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)  
[Managing policies and features for GitHub Copilot in your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/manage-policies) (GitHub Docs)  
[Enforcing policies for GitHub Copilot in your enterprise](https://docs.github.com/en/enterprise-cloud@latest/admin/enforcing-policies/enforcing-policies-for-github-copilot-in-your-enterprise) (GitHub Docs)  
[GitHub Copilot policies](https://docs.github.com/en/copilot/concepts/policies) (GitHub Docs)  

**Question:** [144]  
Which statement about **content exclusion** is accurate?

**Options:**  
A. It censors outputs that resemble excluded files  
B. **It prevents excluded repos/paths/types/patterns from being used as input context**  
C. It disables Copilot in the repository  
D. It removes excluded files from Git history  

**Correct Answer(s):** B  

**Explanation:**  
**Content exclusion** lets admins specify **which repositories, directories, file types, or patterns Copilot is allowed to access as input context**. For excluded content, Copilot will not provide inline suggestions in those files, and that content will not be used to inform suggestions in other files or in Copilot Chat responses. Content exclusion does **not** modify your Git history, disable Copilot entirely in a repo, or automatically censor outputs that merely resemble excluded code; output similarity is governed separately by **code referencing** and suggestions-matching policies.

**Tips and Tricks:**  
- Use content exclusion to protect **sensitive areas** such as secrets, proprietary algorithms, or regulated data from being used as context.  
- Combine **content exclusion** (input control) with **code referencing/duplication filters** (output control) to build a stronger governance posture.  
- Remember that content exclusion affects suggestions in IDE, GitHub.com, and Chat surfaces where supported, but it doesn’t delete files or rewrite history.  

> [!IMPORTANT]  
> Draw a clear mental line: **content exclusion** defines **what Copilot can see**, not what it can possibly output. For output similarity, you must use **code referencing** and **duplication filters**. Exams often test this **input vs. output** distinction.

**Correct and Wrong:**  
The correct option is the only one that captures content exclusion as an **input-context control**. The other options wrongly suggest output censorship, disabling Copilot entirely, or altering Git history—none of which match the documented behavior.

**Source:**  
[Content exclusion for GitHub Copilot](https://docs.github.com/en/copilot/concepts/context/content-exclusion) (GitHub Docs)  
[Excluding content from GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Configure and audit content exclusion](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/configure-content-exclusion) (GitHub Docs)  
[Copilot in GitHub.com now supports Content Exclusions (Preview)](https://github.blog/changelog/2025-01-23-copilot-in-github-com-now-supports-content-exclusions-preview/) (GitHub Blog)  

**Question:** [145]  
Which roles can **manage** content exclusion policies?

**Options:**  
A. Outside collaborators only  
B. People with Maintain role  
C. **Repository administrators, organization owners, and enterprise owners**  
D. Any repository contributor  

**Correct Answer(s):** C  

**Explanation:**  
**Content exclusion** is an **administrative control**. GitHub Docs state that **repository administrators, organization owners, and enterprise owners** can manage content exclusion settings, while users with the **Maintain** role can only view the configuration for a repository and cannot edit it. Outside collaborators and general contributors do not have permission to change content exclusion settings.

**Tips and Tricks:**  
- Think of content exclusion as controlled by **admins/owners** at repo, org, and enterprise scopes, not by general contributors.  
- Use **enterprise and organization** policies for broad defaults, and **repository admins** for more granular, repo-specific exclusions.  
- Remember: the **Maintain** role is **view-only** for content exclusion; they can inspect but not change the rules.  

> [!IMPORTANT]  
> Editing content exclusion is intentionally limited to **repository admins** and **owners at org/enterprise level** to keep control of sensitive-context boundaries in the hands of administrators, while the **Maintain** role provides visibility without configuration power.

**Correct and Wrong:**  
The correct option is the only one that reflects the documented **permission model**: repo admins, org owners, and enterprise owners manage content exclusion. The other options either give control to roles that are explicitly **view-only** (Maintain) or have no special rights (outside collaborators, any contributor).

**Source:**  
[Excluding content from GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-content-exclusion/exclude-content-from-copilot) (GitHub Docs)  
[Configuring content exclusions for GitHub Copilot (Enterprise Cloud)](https://docs.github.com/enterprise-cloud@latest/copilot/managing-github-copilot-in-your-organization/configuring-content-exclusions-for-github-copilot) (GitHub Docs)  
[Configure and audit content exclusion](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/configure-content-exclusion) (GitHub Docs)

**Question:** [146]  
A suggestion exactly matches ~200 characters from a public repo. What happens?

**Options:**  
A. It’s allowed as long as the public code uses a permissive license.  
B. **It is blocked by duplication-detection filters**  
C. It always shows with references instead of being blocked.  
D. It shows or is blocked based solely on the repository’s license file.  

**Correct Answer(s):** B  

**Explanation:**  
When a Copilot suggestion **exactly matches** a long segment of public code (around **150+ characters**), the **duplication-detection / suggestions matching public code** filter can block that suggestion from being shown if blocking is enabled. This safeguard is based on **exactness and length**, not on the license of the public code, and it exists to reduce the risk of emitting large verbatim segments from public repositories. Similar-but-not-exact suggestions are controlled separately via **code referencing** policies.

**Tips and Tricks:**  
- Treat **“≈150+ characters and exact match to public code”** as a strong signal that the **duplication-detection filter** will block the suggestion when blocking is configured.  
- Remember the filter does **not** perform license analysis; it only detects and handles long exact (or near-exact) matches to public code.  
- Use **code referencing** for **similar-but-not-exact** suggestions and configure it to **Block** if your org forbids matching public code entirely.

> [!IMPORTANT]  
> For exam purposes, when you see “**exactly matches a long (~200 character) segment of public code**,” think **duplication-detection filter blocks it**, regardless of whether the license is permissive and regardless of any “Allow + show references” setting.

**Correct and Wrong:**  
The correct option is the only one that treats a long exact match as **blocked by the duplication-detection filter**, independent of licensing. The other options incorrectly depend on license type or assume it will always show with references, which describes **code referencing**, not the blocking behavior for long exact matches.

**Source:**  
[Finding public code that matches GitHub Copilot suggestions](https://docs.github.com/en/copilot/how-tos/get-code-suggestions/find-matching-code) (GitHub Docs)  
[Managing GitHub Copilot policies as an individual subscriber](https://docs.github.com/en/copilot/how-tos/manage-your-account/manage-policies) (GitHub Docs)  
[Responsible AI with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/responsible-ai-with-github-copilot/) (Microsoft Learn)  

**Question:** [147]  
Which plan enables **repository-aware Copilot Chat on GitHub.com** (chat that can reference repo files and docs)?

**Options:**  
A. Copilot Individual (Pro/Pro+)  
B. Copilot Business  
C. **Copilot Enterprise**  
D. Copilot Free  

**Correct Answer(s):** C  

**Explanation:**  
**Copilot Enterprise** unlocks **repository-aware Copilot Chat on GitHub.com** for **GitHub Enterprise Cloud** organizations. With repo-aware chat, Copilot can use the repository’s files, documentation, and code structure as context when answering questions directly on GitHub.com. This capability is **not** included in Copilot Free, Individual, or Business plans, which focus on IDE chat and more limited GitHub.com experiences. When a stem mentions **chat on GitHub.com that can reference repo files and docs**, the intended answer is **Copilot Enterprise**.

**Tips and Tricks:**  
- Distinguish **IDE chat** (available in more plans) from **repo-aware chat on GitHub.com**, which is tied to **Copilot Enterprise**.  
- Remember that repo-aware chat follows **repository permissions**: Copilot only has access to what the user can see in that org/repo.  
- If the stem explicitly says **“Copilot Chat on GitHub.com that can read repository files/docs,”** choose **Copilot Enterprise**, not Individual or Business.

> [!IMPORTANT]  
> **Copilot Enterprise = repo-aware GitHub.com chat for GHEC orgs.** If the question talks about chat on GitHub.com with full repository context (not just IDE chat), that’s your **Enterprise** signal.

**Correct and Wrong:**  
The correct option is the only one corresponding to **repository-aware chat on GitHub.com**, which is an **Enterprise-only** surface for GHEC customers. Individual and Business plans may provide Copilot Chat in IDEs and some GitHub.com features, but they do not unlock full repo-aware chat on GitHub.com.

**Source:**  
[About GitHub Copilot Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/set-up/set-up-for-enterprise) (GitHub Docs)  
[Plans for GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans) (GitHub Docs)  
[GitHub Copilot features](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  

**Question:** [148]  
Which statement about **Copilot Knowledge Bases** is accurate?

**Options:**  
A. Available on all plans  
B. Available on Business & Enterprise  
C. **Enterprise-only curated sources for chat grounding (GitHub.com/VS Code)**  
D. Available on Individual Pro/Pro+ only  

**Correct Answer(s):** C  

**Explanation:**  
**Copilot Knowledge Bases** are an **Enterprise-only** capability for GitHub Enterprise Cloud organizations using **Copilot Enterprise**. They allow admins to curate **trusted, org-approved sources** (such as internal docs, runbooks, and policies) and use them to **ground Copilot Chat responses** on GitHub.com and in VS Code. This is distinct from generic repo context: you explicitly choose what content to include in the Knowledge Base, giving you tighter control over what Copilot cites and how it answers questions.

**Tips and Tricks:**  
- Use Knowledge Bases for **repeatable, auditable guidance**, such as security policies, onboarding guides, and operational runbooks.  
- Remember that Knowledge Bases are **curated**; you decide which repositories, folders, or docs are used as grounding sources.  
- If a stem mentions **“Knowledge Bases,” “curated org-approved sources,” or “grounded answers on GitHub.com/VS Code,”** the answer is **Copilot Enterprise**, not Individual or Business.

> [!IMPORTANT]  
> Knowledge Bases are part of the **Copilot Enterprise** stack for **GHEC** customers, and they’re specifically about **grounding chat on curated internal content**, not just letting chat see any repo.

**Correct and Wrong:**  
The correct option is the only one that reflects Knowledge Bases as an **Enterprise-only** feature providing curated, org-approved grounding sources for Copilot Chat. The other options either overstate availability (all plans), mis-assign it to Business, or restrict it to Individual plans, none of which is supported by the docs.

**Source:**  
[GitHub Copilot features](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[About GitHub Copilot Enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/set-up/set-up-for-enterprise) (GitHub Docs)  
[GitHub Copilot Enterprise overview](https://docs.github.com/en/enterprise-cloud@latest/copilot/github-copilot-enterprise/overview/about-github-copilot-enterprise) (GitHub Docs)

**Question:** [149]  
Who manages purchasing and **seat assignment** for **Business vs. Enterprise**?

**Options:**  
A. Developers in the IDE  
B. **Org owners (Business); Enterprise owners (Enterprise)**  
C. Repository admins for both  
D. Any organization member  

**Correct Answer(s):** B  

**Explanation:**  
For **Copilot Business**, **organization owners** subscribe to the plan for their organization and manage access by assigning seats to members. For **Copilot Enterprise**, **enterprise owners** subscribe at the **enterprise level**, enable Copilot for one or more organizations, and can grant licenses across the enterprise. While org owners typically handle day-to-day seat assignment, enterprise owners control **enterprise-scope purchasing and enablement**, which is what the stem is contrasting for Business vs Enterprise.

**Tips and Tricks:**  
- Map **Copilot Business** to **organization-level** subscription and seat assignment by **org owners**.  
- Map **Copilot Enterprise** to **enterprise-level** subscription and enablement by **enterprise owners**, who then let org owners assign seats within orgs.  
- Repository admins don’t manage Copilot licensing; they manage repo settings, not plan purchase or seat assignment.

> [!IMPORTANT]  
> For exam questions, remember: **Business → org owners**, **Enterprise → enterprise owners**. Licensing and plan enablement follow this hierarchy, not repo admins or “any member.”

**Correct and Wrong:**  
The correct option is the only one that aligns plan scope with the right administrative role: **org owners** for Copilot Business and **enterprise owners** for Copilot Enterprise. The other options incorrectly give purchasing and seat assignment power to developers, repo admins, or any member, none of whom control Copilot billing or plan-level access.

**Source:**  
[Manage the GitHub Copilot plan for your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/manage-plan) (GitHub Docs)  
[Granting access to GitHub Copilot for members of your organization](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/manage-access/grant-access) (GitHub Docs)  
[Subscribe to GitHub Copilot for your enterprise](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/administer-copilot/manage-for-enterprise/manage-plan/subscribe) (GitHub Docs)  
[Billing for GitHub Copilot in organizations and enterprises](https://docs.github.com/en/copilot/concepts/billing/organizations-and-enterprises) (GitHub Docs)  
[Setting up GitHub Copilot for your enterprise](https://docs.github.com/en/copilot/how-tos/set-up/set-up-for-enterprise) (GitHub Docs)  

**Question:** [150]  
Which capability allows Copilot to perform **multi-step changes** and open a **pull request** for review?

**Options:**  
A. Inline suggestions  
B. **Copilot coding agent (Agent mode)**  
C. Content exclusion  
D. Code referencing  

**Correct Answer(s):** B  

**Explanation:**  
The **Copilot coding agent** is the capability that can take a **high-level task**, plan **multi-step changes** across files, run tools or tests, and then **open or update a pull request** for review when it’s done. This is different from **inline suggestions**, which only complete code at the cursor, and from basic **Copilot Edits**, which apply scoped diffs that you approve in the editor. While “Agent mode” in the editor also plans and runs multi-step actions, the PR-centric workflow described in the stem best matches the **Copilot coding agent** behavior.

**Tips and Tricks:**  
- Use the **Copilot coding agent** when you want an **autonomous workflow** that can implement changes and raise a **draft PR** for review.  
- Use **Copilot Edits / Edit mode** when you want **fine-grained, user-approved diffs** directly in your editor.  
- Inline suggestions are for **small, local completions** and do not plan multi-step work or open pull requests.

> [!IMPORTANT]  
> On exams, phrases like **“multi-step changes”** plus **“opens a pull request for review”** point to the **Copilot coding agent**, not to inline completions or governance features like content exclusion or code referencing.

**Correct and Wrong:**  
The correct option is the only one that aligns with an **autonomous, multi-step agent** that can **open a pull request** for review: the **Copilot coding agent**. Inline suggestions just complete code in place, and content exclusion or code referencing are policy/governance features, not execution engines.

**Source:**  
[About GitHub Copilot coding agent](https://docs.github.com/en/copilot/concepts/agents/coding-agent/about-coding-agent) (GitHub Docs)  
[Ask GitHub Copilot coding agent to create a pull request](https://docs.github.com/en/copilot/how-tos/use-copilot-agents/coding-agent/create-a-pr) (GitHub Docs)  
[Using GitHub Copilot coding agent](https://docs.github.com/en/copilot/tutorials/coding-agent) (GitHub Docs)  
[GitHub Copilot features (Edits & agents)](https://docs.github.com/en/copilot/get-started/features) (GitHub Docs)  
[Copilot ask, edit, and agent modes: what they do and when to use them](https://github.blog/ai-and-ml/github-copilot/copilot-ask-edit-and-agent-modes-what-they-do-and-when-to-use-them/) (GitHub Blog)  