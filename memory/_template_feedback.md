---
name: A Lesson Learned
description: Guidance, feedback, or patterns you've confirmed - why and when to apply
type: feedback
---

**The Rule:**
[State the specific guidance or pattern you learned. Be concrete.]

**Why:**
[The reason this matters. What incident or validation confirmed it? What's at stake?]

**How to apply:**
[When/where does this guidance kick in? Edge cases? When does it NOT apply?]

---

**Example:**

**The Rule:**
Integration tests must use a real database, not mocks. Never mock the database.

**Why:**
Last quarter, we shipped a migration that passed all mocked tests but failed in production. A mock-vs-prod divergence in transaction behavior hid the bug. Real databases caught it would have caught it immediately. We lost 2 days to this.

**How to apply:**
Any test that touches database operations (migrations, queries, schema changes) must hit a real test database. This applies even to "simple" unit tests of ORM methods. Edge case: isolated crypto/logic-only tests can use mocks. When in doubt, use a real database.

---

**Another Example:**

**The Rule:**
Stop summarizing what you just did at the end of every response. I can read the diff.

**Why:**
Brevity matters. Summary lines add noise without information.

**How to apply:**
Every response going forward - skip the end-of-turn summary unless the user explicitly asks "what changed?"
