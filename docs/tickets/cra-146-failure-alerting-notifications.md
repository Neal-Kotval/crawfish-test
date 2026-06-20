# Failure alerting / notifications

> Auto-drafted by crawfish for Linear issue **CRA-146**.

**Goal:** tell a human when something needs attention — "the nightly batch failed," "a budget tripped," "dead-letter is filling up."

- [ ] Notification channels (Slack / email / webhook)
- [ ] Triggers: batch/pipeline failure, budget breach, dead-letter threshold, anomaly auto-halt
- [ ] Configurable per pipeline

**Acceptance:** a failed scheduled batch posts an alert with a link to the run inspector.

**Relates:** [CRA-121](https://linear.app/crawfish/issue/CRA-121/23-cost-preview-budgets) (budgets), [CRA-122](https://linear.app/crawfish/issue/CRA-122/24-retries-backoff-dead-letter-and-replay) (dead-letter), [CRA-110](https://linear.app/crawfish/issue/CRA-110/10-metrics-rubrics-and-benchmarks-the-improvement-loop) (anomaly halt).
