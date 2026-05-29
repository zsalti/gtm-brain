# Custom Rule Template

Use this structure to create custom rules beyond brand-voice and strategy-guard.

---

## [Rule Name]

**When to activate:** [When should Claude apply this rule? What triggers it?]

**Core principle:** [What's the essence of this rule?]

## [Section 1: The Pattern or Framework]

[Explain the key concepts]

**Red flags / Anti-patterns:**
- [What should Claude watch for?]
- [What should trigger this rule?]

**Green light / Pro patterns:**
- [What should Claude reinforce?]

## [Section 2: Decision Framework or Checklist]

[Provide a decision framework, checklist, or specific guidance]

1. [First step/question]
2. [Second step/question]
3. [Third step/question]

## Examples

**When this rule applies:**
[Concrete example 1]
[Concrete example 2]

**When this rule does NOT apply:**
[Edge case or exception]

## Intervention Style

[How should Claude apply this rule? Direct? Gentle? Ask questions?]

---

**Example: A rule about testing strategy**

## Testing Standards - Real Databases Over Mocks

**When to activate:** Whenever discussing testing strategy, test implementation, or test coverage

**Core principle:** Real databases catch prod issues that mocks hide

## The Pattern

Integration tests that touch the database should always use a real test database, not mocks. Mocks create false confidence by hiding prod/test divergence.

**Red flags:**
- "Let's mock the database for speed"
- "These unit tests don't need a real DB"
- Any suggestion to skip the database in tests that touch it

**Green light:**
- "Integration test suite uses real Postgres"
- "We caught this in pre-prod with a real database"

## Decision Framework

1. Does this test touch database operations? (migrations, queries, schema changes)
2. If yes, use a real test database
3. Edge case: pure logic/crypto tests can use mocks
4. When in doubt, use a real database

## Intervention Style

Direct. "This test needs a real database" not "consider using a real database." The rule is binary.

---

When you create a custom rule, add it to `.claude/rules/` and it will auto-load with your project.
