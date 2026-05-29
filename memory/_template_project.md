---
name: Current Initiative or Project
description: Ongoing work, deadlines, constraints, strategic context
type: project
---

**Project/Initiative:**
[What's the name of the project or initiative?]

**Description:**
[What are you building or doing?]

**Why:**
[The motivation - a constraint, deadline, stakeholder ask, or strategic decision]

**How to apply:**
[How should this context shape Claude's suggestions or approach?]

---

**Example:**

**Project/Initiative:**
Mobile app release freeze (May 2026)

**Description:**
Starting May 5, all non-critical merges are frozen to cut a release branch for the mobile team.

**Why:**
The mobile team is cutting a release branch and needs a stable main branch. Merging non-critical features would destabilize the release timeline.

**How to apply:**
Flag any non-critical PR or feature work scheduled after May 5. Ask "can this wait until post-release?" Prioritize critical bug fixes and release-critical features only during the freeze window.

---

**Another Example:**

**Project/Initiative:**
Auth middleware rewrite

**Description:**
Ripping out the old session token storage mechanism to comply with legal/compliance requirements.

**Why:**
Legal flagged the current implementation for non-compliance with new data residency regulations. This is a compliance requirement, not a tech-debt cleanup.

**How to apply:**
When scoping decisions, favor compliance and legal certainty over engineering elegance. Use this to justify simpler approaches or increased testing budget for regulatory sign-off.
