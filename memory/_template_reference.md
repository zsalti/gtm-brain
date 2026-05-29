---
name: External Resource or System
description: Pointer to where information lives outside your project
type: reference
---

**Resource:**
[Name of the system, tool, or location]

**Where to find it:**
[URL, path, or location]

**What's there:**
[What information or functionality lives here?]

**When to check:**
[When is this relevant? What triggers a lookup?]

---

**Example:**

**Resource:**
Pipeline bugs tracker (Linear)

**Where to find it:**
https://linear.com/team/INGEST (linear project "INGEST")

**What's there:**
All pipeline ingestion bugs, blockers, and performance issues. Also contains related feature requests and technical debt for the ingestion layer.

**When to check:**
Whenever touching data pipeline code or investigating ingestion issues. Also check before starting new pipeline work to avoid duplicating open issues.

---

**Another Example:**

**Resource:**
Oncall latency dashboard (Grafana)

**Where to find it:**
grafana.internal/d/api-latency

**What's there:**
Real-time API latency tracking. Oncall watches this dashboard for p99 latency spikes and alerts.

**When to check:**
Before and after any request-path code changes. Use this to verify your change doesn't regress latency. Also check during deploys to catch unexpected performance impacts.
