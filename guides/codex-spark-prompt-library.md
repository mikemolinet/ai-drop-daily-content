---
title: 15 Copy-Paste Prompts for GPT-5.3 Codex Spark
description: Battle-tested prompts designed for Spark's real-time speed. Scaffolding, refactoring, debugging, testing, and architecture — ready to use.
category: AI Coding
publishedAt: 2026-02-16
---

# 15 Copy-Paste Prompts for GPT-5.3 Codex Spark

*Built for real-time, iterative coding. These prompts are designed to exploit Spark's speed (1,000+ tok/s) — short, precise instructions that get instant results. Use in Codex app, CLI, or VS Code extension.*

---

## 🏗️ Scaffolding & Greenfield

### 1. Full API Endpoint in One Shot
```
Build a complete REST API endpoint for [RESOURCE] (e.g., /api/users, /api/invoices).

Stack: [your stack, e.g., FastAPI + Pydantic / Express + Zod / Rails / Django REST Framework]

I need the FULL implementation — not pseudocode, not stubs. Every file I'd need to make this work:

1. Data model/schema with proper types, validation rules, and field constraints
2. Route handler covering all CRUD operations (GET list with pagination + filtering, GET by ID, POST create, PUT/PATCH update, DELETE)
3. Input validation - reject bad data with clear error messages before it hits the database
4. Error handling - 400 for bad input, 404 for missing resources, 409 for conflicts, 500 with safe error messages (never leak internals)
5. Unit tests - happy path for each operation, edge cases (empty strings, missing required fields, duplicate unique values, invalid IDs), and error cases
6. Request/response types - fully typed, no `any` types anywhere

Constraints:
- Follow RESTful conventions (proper HTTP methods, status codes, resource naming)
- Use proper async/await patterns if the stack supports it
- Include rate limiting middleware if applicable
- Add created_at/updated_at timestamps automatically
- Paginate list endpoints (default 20, max 100)
- Return consistent error format: { "error": { "code": "...", "message": "..." } }
```

**What Spark produces in ~10 seconds:** A complete, runnable endpoint with 5-7 files — model, routes, validation schemas, error handlers, and a full test suite. First-try quality that usually needs only minor tweaks.

### 2. React Component from Description
```
Build a React component: [describe what it does, e.g., "a pricing table with 3 tiers, toggle between monthly/annual, highlight the recommended plan"]

Technical requirements:
- TypeScript with proper types — no `any`, explicit prop types, typed event handlers
- Tailwind CSS for all styling (no inline styles, no CSS modules)
- Mobile-responsive — stack vertically on mobile, grid on desktop
- Loading state with skeleton placeholder (not a spinner)
- Error state with retry button
- Empty state if applicable
- Export as default with named type export for props

UX requirements:
- Smooth transitions/animations for state changes (use Tailwind's transition utilities)
- Accessible — proper aria labels, keyboard navigation, focus states
- Handle rapid clicks/interactions gracefully (debounce where needed)

Structure:
- Main component file with clear sections: types, hooks, sub-components, main render
- Extract any complex logic into a custom hook
- If the component has more than 3 states, use a state machine or reducer pattern
- Keep the component under 200 lines — split into sub-components if it's getting long

Give me something I can drop into my project and have it work immediately. No "TODO" comments. No placeholder content — use realistic dummy data.
```

**What Spark produces in ~8 seconds:** A polished, production-ready component with proper TypeScript, responsive layout, all states handled, and realistic content. Usually needs only design tweaks to match your brand.

### 3. Database Schema + Migrations
```
Design a database schema for: [describe your domain, e.g., "a SaaS project management tool with workspaces, projects, tasks, and team members"]

Database: [Postgres/SQLite/MySQL]

I need the complete schema — think through the relationships, not just the obvious tables:

1. Table definitions:
   - Proper column types (don't use VARCHAR(255) for everything — be specific)
   - NOT NULL constraints on required fields
   - DEFAULT values where sensible (timestamps, status fields, booleans)
   - CHECK constraints for enums and valid ranges
   - Unique constraints on natural keys (email, slug, etc.)

2. Relationships:
   - Foreign keys with proper ON DELETE behavior (CASCADE vs SET NULL vs RESTRICT — think about what makes sense for each relationship)
   - Junction tables for many-to-many relationships
   - Self-referential relationships if needed (e.g., parent tasks, org hierarchies)

3. Indexes:
   - Primary keys (obviously)
   - Foreign key columns
   - Columns commonly used in WHERE clauses and ORDER BY
   - Composite indexes for common query patterns
   - Partial indexes where they make sense (e.g., active users only)

4. Migration file:
   - Single file I can run directly with psql/mysql/sqlite3
   - CREATE TABLE statements in dependency order
   - All constraints inline (not added after)
   - Rollback/down migration at the bottom (commented out)

5. Seed data:
   - 5-10 realistic records per table (real-looking names, emails, dates)
   - Data that's internally consistent (foreign keys match, dates make sense)
   - Include edge cases in seed data (null optional fields, max-length strings, earliest/latest dates)

Think about what I'll need 6 months from now, not just today. Include audit fields (created_at, updated_at, created_by) and soft delete (deleted_at) on tables where it makes sense.
```

**What Spark produces in ~12 seconds:** A complete, well-thought-out schema with 8-15 tables, proper relationships, sensible indexes, a runnable migration file, and realistic seed data. The kind of schema design that normally takes an hour of whiteboarding.

---

## 🔧 Refactoring & Cleanup

### 4. Legacy Code Modernizer
```
Refactor this code to modern [language] standards:

[paste code]

Rules:
- Keep the same behavior — don't change what it does
- Use current idioms and patterns
- Improve naming (make it self-documenting)
- Remove dead code and unnecessary comments
- Add types where missing
Explain each significant change in a brief comment.
```

### 5. Extract and Decompose
```
This function is too long. Break it into smaller, well-named functions:

[paste function]

Rules:
- Each extracted function should do exactly one thing
- Names should make comments unnecessary
- Keep the original function as an orchestrator that calls the new ones
- Don't change behavior
```

### 6. Performance Audit
```
Review this code for performance issues:

[paste code]

Flag:
- N+1 queries or unnecessary DB calls
- Redundant iterations or allocations
- Missing indexes (if DB-related)
- Obvious caching opportunities
For each issue: explain the problem, show the fix, estimate the improvement.
```

---

## 🐛 Debugging & Fixing

### 7. Bug Hunter
```
This code has a bug. Here's the symptom: [describe what's wrong].

[paste code]

Find the bug, explain why it happens, and give me the fix.
If there are multiple possible causes, rank them by likelihood.
```

### 8. Error Handler
```
Add proper error handling to this code:

[paste code]

Requirements:
- Catch specific errors (not generic catch-all)
- Meaningful error messages for each case
- Proper HTTP status codes if it's an API
- Log errors with enough context to debug
- Never swallow errors silently
```

---

## 🧪 Testing

### 9. Test Suite Generator
```
Write a comprehensive test suite for this code:

[paste code]

Include:
- Happy path tests
- Edge cases (empty input, null, boundary values)
- Error cases (what should fail and how)
- Use [Jest/Pytest/Go testing] with descriptive test names
- Each test should be independent — no shared state
Target: 90%+ coverage of meaningful paths.
```

### 10. Test Data Factory
```
Create a test data factory for [your domain]:

Models: [list your models]

Requirements:
- Factory functions that generate realistic fake data
- Override any field easily
- Related records should be consistent (e.g., order.userId matches user.id)
- Include edge case generators (empty strings, max lengths, special characters)
Use [Faker/factory-boy/your preferred lib].
```

---

## 📐 Architecture & Design

### 11. API Design Review
```
Review this API design and suggest improvements:

[paste your routes/endpoints]

Check for:
- RESTful conventions (proper HTTP methods, status codes, resource naming)
- Missing endpoints I probably need
- Pagination, filtering, sorting patterns
- Auth/permission patterns
- Versioning strategy
Give me the improved API spec.
```

### 12. System Design Sketch
```
Design the architecture for: [describe what you're building].

Scale: [expected users/requests].

Include:
- Service boundaries and responsibilities
- Data flow between services
- Database choices with reasoning
- Caching strategy
- What to build now vs. what to defer
Keep it practical — not a whiteboard exercise. What would you actually ship?
```

---

## ⚡ Speed Hacks (Spark-Specific)

### 13. Instant Code Review
```
Review this PR diff. Be direct — what's wrong, what's good, what I missed:

[paste diff]

Format:
🔴 Must fix (bugs, security issues)
🟡 Should fix (code quality, maintainability)
🟢 Nice to have (style, minor improvements)
Skip obvious stuff. Focus on what a senior engineer would catch.
```

### 14. Rapid Prototyper
```
Build a working prototype of [describe feature] in the simplest way possible.

Constraints:
- Single file if possible
- No unnecessary dependencies
- It should actually work — not pseudocode
- Include a brief "how to run it" at the top
I'll refactor later. Right now I need to see if the idea works.
```

### 15. Conversation Debug (Spark's killer feature)
```
I'm working on [describe what you're building]. Here's my current code:

[paste code]

I'm stuck on [describe the problem]. I've tried [what you tried].

Walk me through this interactively — ask me questions if you need more context. Let's figure this out together.
```

---

## How to Use This Library

**Spark vs. regular Codex — when to use which:**

- **Use Spark for:** Quick edits and iterations, debugging conversations, rapid prototyping, code reviews, "what if I tried..." exploration
- **Use regular Codex for:** Multi-file refactors across a codebase, long-running autonomous tasks, complex architectural changes, anything you'd walk away from while it runs

**Tips for getting the most out of Spark:**

1. **Be specific about your stack** — Spark is fast enough that you can iterate, but specific prompts get better first-shot results
2. **Paste actual code** — Don't describe it, show it. Spark's 128k context handles large files
3. **Iterate fast** — Spark's speed means you can have a conversation. "Now make it handle edge case X." "Add caching." "Actually, use a different pattern."
4. **Use it for the back-and-forth** — Spark shines when you're thinking through a problem interactively, not when you're fire-and-forgetting a task
