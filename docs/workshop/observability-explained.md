# What is Observability
What is observability and why should you care? When we say observability we mean trying to understand the internal system state via measuring data available to the outside. Typically, we do this to be able to act upon it.

**System**: Short for System Under Observation (SUO).

This is the cloud native platform (and applications running on it) you care about and are responsible for.

**Signals**: Information observable from the outside of a system. 

There are different signal types (most common ones are **logs**, **metrics**, and **traces**) and they originate at sources.

**Sources**: Are part of the infrastructure and application layer such as a microservice, a device, or the operating system. They typically have to be instrumented to emit signals.

**Agents**: Responsible for signal collection and routing.

**Destinations**: Where you consume signals, for different reasons and use cases, it includes visualizations (dashboards for example), alerting, long term storage (for regulatory purposes), analytics (finding new usages for an app).

**Telemetry**: The process of collecting signals from sources, routing/pre-processing via agents, and ingestion to destinations.

---
Observability in this sense represents, in essence, a feedback loop. A human user might, for example, restart a service based on the gathered information. In the case of an app, this could be a cluster autoscaler that adds worker nodes based on the system utilization measured.

The important aspect of observability is actionable insights. Simply providing an error message in a log line or having a dashboard with fancy graphics is not sufficient.