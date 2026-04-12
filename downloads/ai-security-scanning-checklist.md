# AI Security Scanning Checklist
## 53 Things to Test + 15 Prompts for Security Scanning with Claude

> **📥 [Download this guide as Markdown](/api/guides/ai-security-scanning-checklist/download)** — save it, share it, drop it in your team's repo.

As AI-generated code becomes the norm, automated security scanning becomes essential. Most developers using AI to write code aren't security experts. These tools close that gap.

---

## 🎯 WHERE AI SCANNING ADDS THE MOST VALUE

Traditional static analysis tools are great at pattern-matching known vulnerability signatures. AI scanning shines where they can't — understanding how your code actually works:

| AI Scanning Sweet Spot | What It Catches |
|---|---|
| **Business logic flaws** | Race conditions, state transition bypasses, duplicate processing bugs |
| **Broken access control** | Horizontal privilege escalation, IDOR, authorization gaps across components |
| **Complex data flow issues** | Tracing untrusted input across multiple files and trust boundaries |
| **Cross-component interaction bugs** | Vulnerabilities that only appear when you understand how pieces connect |

If you're short on time, focus your AI scanning here. These are the vulnerabilities that slip past traditional tools and human code review.

---

## ⚡ QUICKSTART — 30 MINUTES, 3 PROMPTS

Don't have time for the full guide? Run these 3 in order:

| Step | Prompt | Time | Why First |
|------|--------|------|-----------|
| 1 | **Secrets Scan** (Prompt 6) | ~5 min | Almost always finds something |
| 2 | **API Endpoint Audit** (Prompt 5) | ~10 min/service | Finds auth and validation gaps |
| 3 | **Auth Deep Dive** (Prompt 4) | ~15 min | Your highest-value attack surface |

Once you've fixed what these find, come back and work through the full checklist.

---

## SECTION 1: THE 53-POINT CHECKLIST

### 🔴 Business Logic & Access Control — AI's Sweet Spot

| # | Check |
|---|-------|
| 1 | Race conditions in payment or inventory flows |
| 2 | Business logic bypass (skipping steps in multi-step processes) |
| 3 | Integer overflow in quantity or pricing calculations |
| 4 | Time-of-check to time-of-use (TOCTOU) bugs (value changes between validation and use) |
| 5 | Insufficient validation of state transitions |
| 6 | Duplicate transaction processing |
| 7 | Role-based access control bypass (horizontal privilege escalation) |
| 8 | Broken object-level authorization (IDOR) |

### 🟠 Authentication & Session Management

| # | Check |
|---|-------|
| 9 | SQL injection in login forms (parameterized queries?) |
| 10 | Brute force protection on auth endpoints |
| 11 | Session token entropy and expiration |
| 12 | Password reset flow vulnerabilities (token reuse, email enumeration) |
| 13 | JWT validation (signature verification, algorithm confusion) |
| 14 | OAuth redirect URI validation |
| 15 | API key exposure in client-side code or logs |

### 🟡 Input Validation & Injection

| # | Check |
|---|-------|
| 16 | Cross-site scripting (XSS) in all user inputs |
| 17 | Stored XSS in database-rendered fields |
| 18 | SQL injection in search, filter, and sort parameters |
| 19 | Command injection in file upload handlers |
| 20 | Path traversal in file access endpoints |
| 21 | Server-side request forgery (SSRF) in URL parameters |
| 22 | XML external entity (XXE) in parsers |
| 23 | Template injection in server-side rendering |

### 🔵 API Security

| # | Check |
|---|-------|
| 24 | Missing rate limiting on sensitive endpoints |
| 25 | Mass assignment vulnerabilities (extra fields in POST/PUT) |
| 26 | Verbose error messages leaking stack traces |
| 27 | Missing input validation on API parameters |
| 28 | GraphQL introspection enabled in production |
| 29 | Unauthenticated endpoints exposing data |

### 🟣 Data Handling

| # | Check |
|---|-------|
| 30 | Secrets hardcoded in source code |
| 31 | PII stored unencrypted in database |
| 32 | Sensitive data in URL parameters (logged by proxies) |
| 33 | Missing encryption in transit (HTTP endpoints) |
| 34 | Insecure deserialization |
| 35 | Database credentials in config files committed to git |

### ⚙️ Infrastructure & Config

| # | Check |
|---|-------|
| 36 | Debug mode enabled in production |
| 37 | Default credentials on admin panels |
| 38 | Missing security headers (CORS, CSP, HSTS) |
| 39 | Exposed admin or monitoring endpoints |
| 40 | Outdated dependencies with known CVEs |
| 41 | Docker container running as root |

### 📁 File Uploads & Storage

| # | Check |
|---|-------|
| 42 | Content-type validation (don't trust client-provided MIME types) |
| 43 | Filename sanitization (path traversal via crafted filenames) |
| 44 | File size limits and zip bomb protection |
| 45 | Storage permissions (uploaded files shouldn't be publicly executable) |

### 🖥️ Frontend Security

| # | Check |
|---|-------|
| 46 | Dangerous rendering patterns (React's dangerouslySetInnerHTML, Vue's v-html) |
| 47 | Sensitive data in client-side state or localStorage |
| 48 | Client-side routing auth bypasses |

### 📦 Supply Chain & Dependencies

| # | Check |
|---|-------|
| 49 | Dependency confusion (private vs public package names) |
| 50 | Typosquatting risk in package imports |
| 51 | Pinned vs floating dependency versions |
| 52 | Build pipeline injection points |
| 53 | Third-party script integrity (SRI hashes) |

---

## SECTION 2: 15 COPY-PASTE PROMPTS

Each prompt is in a code block — copy it directly into Claude Code, ChatGPT, or your AI tool of choice.

### Prompt 1: Full Codebase Investigation

```
Investigate this codebase for security vulnerabilities. Start by mapping the
architecture and data flows, then systematically examine each attack surface.
For complex findings, trace the full exploitation path from entry point to
impact. Prioritize vulnerabilities that are difficult for static analysis
tools to catch — business logic flaws, race conditions, and cross-component
interaction bugs. For each finding: explain the attack vector in plain
English, rate severity (critical/high/medium/low), and provide a specific
code fix.
```

> **💡 Tip:** For large codebases, this broad prompt can produce noisy results. Break it down — scan by module, service, or file group instead. For smaller codebases (<5K lines), running it all at once works well.


### Prompt 2: Data Flow Tracing

```
Trace all data flows from user input to database and output in this codebase.
Identify every point where untrusted data crosses a trust boundary without
proper validation or sanitization. Map the complete attack surface. Show me
the path each type of user input takes through the system, and flag anywhere
it's used without being properly escaped or validated.
```


### Prompt 3: False Positive Verification

```
For each vulnerability you identified, attempt to disprove it. Could this be
a false positive? What conditions would need to be true for this to actually
be exploitable? Are there mitigating controls elsewhere in the codebase that
prevent exploitation? Re-examine each finding and drop anything you can't
confidently confirm is a real, exploitable issue.
```


### Prompt 4: Authentication Deep Dive

```
Focus specifically on authentication and authorization in this codebase.
Check for: SQL injection in login, session management issues, JWT validation
problems, password reset vulnerabilities, and any way to escalate privileges.
Trace the complete auth flow from login to session creation to permission
checks.
```


### Prompt 5: API Endpoint Audit

```
Review every API endpoint in this codebase. For each one, check: is it
authenticated? Is there rate limiting? Are inputs validated? Can an attacker
access other users' data by changing IDs? List every endpoint with its
security status.
```


### Prompt 6: Secrets and Credential Scan

```
Search this entire codebase for hardcoded secrets, API keys, passwords,
tokens, and credentials. Check source code, config files, environment
templates, and comments. Flag anything that should be in environment
variables instead.
```


### Prompt 7: Input Validation Sweep

```
Find every place in this codebase where user input is processed. For each
one, check: is it sanitized? Could it be used for XSS, SQL injection,
command injection, or path traversal? Provide the specific fix for each
vulnerability found.
```


### Prompt 8: Race Condition Hunter

```
Analyze this codebase for race conditions, especially in: payment processing,
inventory management, account balance updates, file operations, and any
shared resource access. Explain each race condition with a concrete attack
scenario. Note: static analysis has a high false positive rate for race
conditions — flag only cases where you can demonstrate a realistic
exploitation path, not every non-atomic operation.
```


### Prompt 9: Payment & Billing Security

```
Review all payment-related code in this codebase. Check for: webhook
signature verification, price manipulation in client-to-server flows (can a
user modify the amount sent to the payment processor?), idempotency key
handling, proper error handling for failed charges, and secure storage of
payment-related data. Verify that pricing logic lives server-side, not
client-side.
```


### Prompt 10: Dependency Risk Review

```
Review all dependencies in this project. Check for: dependency confusion
risks (private package names that could be squatted), packages that should be
pinned to specific versions, unmaintained packages, and any unusual or
unnecessary dependencies that increase attack surface. Prioritize by risk.
```

> **⚠️ Important:** For actual CVE scanning, use dedicated tools like `npm audit`, `pip-audit`, Trivy, or Snyk. AI models have a training data cutoff and cannot reliably identify recently published vulnerabilities. Use this prompt for structural dependency risks, not CVE lookups.


### Prompt 11: Before-Deploy Checklist

```
I am about to deploy this to production. Run a pre-deployment security check.
Verify: debug mode is off, error messages don't leak internals, security
headers are set, admin endpoints are protected, and no test credentials
remain. Give me a go/no-go.
```


### Prompt 12: Patch Writer

```
For each vulnerability you found, write the exact code patch I need to apply.
Include the file path, the current vulnerable code, and the fixed version.
Make each patch minimal and targeted so I can review and apply them one at a
time.
```


### Prompt 13: Attack Scenario Generator

```
For the top 5 most critical vulnerabilities in this codebase, write a
detailed attack scenario. How would an attacker find it? What would they do?
What data could they access? What is the business impact? This helps me
prioritize fixes.
```


### Prompt 14: Delta Scan (Changes Since Last Review)

```
Review the codebase focusing only on changes made since [date/commit hash].
Identify any new vulnerabilities introduced and verify whether previously
identified issues in [list areas] have been resolved. If using Claude Code,
it can access git history directly. Otherwise, provide the relevant diff or
changed files for context.
```


### Prompt 15: Security Review for New PR

```
Review this pull request diff for security implications. Check for: new
vulnerabilities introduced, security best practices violations, missing input
validation, and any changes to authentication or authorization logic. Approve
or flag specific concerns.
```

---

## ⚠️ LIMITATIONS — WHAT AI SCANNING CAN'T DO

Be honest about the boundaries:

| Limitation | Details |
|---|---|
| **Not a replacement for penetration testing** | AI scans code, not running systems. It can't test actual network configs, firewall rules, or real-world attack chains. |
| **Runtime vulnerabilities need running code** | CSRF token handling, actual session behavior, and environment-specific issues require dynamic testing tools. |
| **AI can hallucinate vulnerabilities** | Always verify findings before acting. Use Prompt 3 to filter noise. |
| **Environment-specific issues are out of scope** | Misconfigured cloud IAM, firewall rules, and infrastructure settings need dedicated tools. |
| **Compiled dependencies can't be analyzed** | AI can only review code it can read. |
| **Context window limits are real** | Large codebases (50K+ lines) won't fit in one scan. Break into modules. Findings may miss cross-module vulnerabilities. |
| **Results vary between runs** | Same prompt, same code, different findings. Run critical scans more than once. |
| **Language and framework bias** | Stronger at Python/JS/TypeScript than Rust/Go/C++. Adjust trust accordingly. |
| **AI augments, doesn't replace expertise** | Human researchers are still better at sophisticated, multi-step vulnerability chains. |

---

## 🗺️ HOW TO USE THIS

### For a focused security review (highest ROI first):

| Step | Action | Why |
|------|--------|-----|
| 1 | **Prompt 6** — Secrets scan | Quick wins, almost always finds something |
| 2 | **Prompt 5** — API audit (one service at a time) | Find obvious auth and validation holes |
| 3 | **Prompt 4** — Auth deep dive | Your most critical attack surface |
| 4 | **Prompt 8** — Race conditions (scoped to payments) | Biggest business risk |
| 5 | **Prompt 2** — Data flow tracing | Trace specific flows you're worried about |
| 6 | **Checklist** — Verify coverage | Did you miss anything? |
| 7 | **Prompt 3** — False positive verification | Filter noise from findings |
| 8 | **Prompt 12** — Patches | Generate fixes for confirmed vulnerabilities |

### For ongoing security hygiene:

| When | Action |
|------|--------|
| Every PR | **Prompt 15** — PR security review. This is where the daily value lives. |
| Every deploy | **Prompt 11** — Pre-deploy checklist. |
| Every sprint | **Prompt 14** — Delta scan on what changed since last review. |

### Scoping tips for large codebases:

- Don't scan everything at once. Break it down by service, module, or domain boundary.
- Start with your highest-risk surfaces: auth, payments, file uploads, admin endpoints.
- Scan one chunk, fix what you find, move to the next. Don't try to boil the ocean.

---

## TOOL LANDSCAPE

Claude Code Security isn't the only AI scanning tool. OpenAI's Aardvark (launched October 2025) offers similar capabilities with sandboxed exploit validation. GitHub's CodeQL and Copilot Autofix are widely adopted for AI-assisted security in CI/CD pipelines. Traditional tools like Snyk, SonarQube, and Semgrep remain valuable for pattern-matching known vulnerabilities at scale. The best security setup combines AI scanning (for logic flaws and complex bugs) with traditional tools (for known CVE patterns and dependency checks).

---

*v1.0 — February 2026*

Free to share. Built by Mike Molinet — with AI, of course.

- Substack: mikemolinet.substack.com
- LinkedIn: linkedin.com/in/mikemolinet
- GitHub: github.com/mikemolinet
- Twitter: @mikemolinet
