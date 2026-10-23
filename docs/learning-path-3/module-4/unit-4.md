# Learning Path 3 — Module 4, Unit 4: Describe Azure Monitor

**Module:** Describe monitoring tools in Azure  
**Learning goal:** Recognize Azure Monitor and related capabilities including Log Analytics, alerts, and Application Insights.

## 3. Azure Monitor — “What is happening in my resources and applications?”

Azure Monitor is Azure's monitoring and observability service. It collects and analyzes telemetry from Azure and supported hybrid environments so you can understand performance, availability, and reliability.

Telemetry includes metrics, logs, traces, and events.

### Metrics vs. logs

**Metrics** are numerical measurements collected over time, such as CPU percentage, request duration, or the number of requests. They are useful for observing trends and detecting performance changes.

**Logs** are timestamped records of events or activity. They provide detail that can help investigate what happened and why.

**Example:**
- A CPU metric shows that a virtual machine's CPU usage spiked.
- Logs help investigate what events or activity occurred around that time.

Metrics can help you detect a problem quickly; logs often provide more context for troubleshooting.

## 4. Log Analytics

Log Analytics is a tool for querying and analyzing log data collected in a Log Analytics workspace. It uses **Kusto Query Language (KQL)**.

You do not need to master KQL for this introductory lesson. Recognize the association:
- **Logs + querying and investigation = Log Analytics**
- **KQL = the query language used for Azure Monitor Logs**

**Example:** GeekHub investigates why a website generated errors by querying relevant log records around the time of the incident.

## 5. Azure Monitor alerts

Alerts notify you when monitoring data or a configured condition indicates that attention may be needed. Alert rules can be based on metrics, logs, or activity-related signals, depending on the scenario. Rules can trigger notifications or actions.

**Example:** If a school's web application has an unusually high error rate, an alert rule can notify the responsible team so they can investigate.

Remember: an alert detects and notifies; it does not automatically fix every issue. Automated actions require appropriate configuration.

## 6. Application Insights

Application Insights is an application performance monitoring (APM) capability within Azure Monitor. It helps developers observe live application behavior and diagnose issues such as:
- Slow responses and performance bottlenecks.
- Failed requests and exceptions.
- Application usage and request patterns.
- Dependencies and transactions across application components.

**Example:** A school's website loads slowly. Application Insights can help GeekHub investigate request duration, failed requests, and dependency performance.

## Quick knowledge check

**Which service is associated with collecting and analyzing telemetry from Azure resources and applications?**

**Answer:** Azure Monitor, with related capabilities such as Log Analytics, alerts, and Application Insights.

## Official learning resource

[Describe Azure management and governance — Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)
