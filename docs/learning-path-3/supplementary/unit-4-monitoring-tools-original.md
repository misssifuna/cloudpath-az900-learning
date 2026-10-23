# Azure Fundamentals — Learning Path 3, Unit 4
## Monitoring tools in Azure

**Exam alignment:** AZ-900 — Describe monitoring tools in Azure, including Azure Advisor, Azure Service Health, Azure Monitor, Log Analytics, Azure Monitor alerts, and Application Insights.

## Learning objectives

By the end of this lesson, you should be able to:
- Explain what Azure Advisor recommends.
- Distinguish Azure Service Health from monitoring an individual resource or application.
- Explain Azure Monitor, metrics, and logs.
- Describe Log Analytics, Azure Monitor alerts, and Application Insights.

## 1. Azure Advisor — “What could I improve?”

Azure Advisor analyzes Azure resource configuration and usage telemetry and provides recommendations to help optimize deployments.

Its five recommendation categories are:
- **Reliability:** improve continuity and resilience.
- **Security:** identify ways to improve security posture.
- **Performance:** improve resource or application performance.
- **Cost:** identify opportunities to reduce Azure spending.
- **Operational excellence:** improve processes, manageability, and deployment practices.

**Example:** GeekHub reviews Advisor recommendations and finds a school's resources may be oversized for their workload. The team investigates whether a smaller suitable configuration could reduce costs.

Advisor provides recommendations; it is not the primary tool for collecting detailed application logs or reporting every live Azure outage.

## 2. Azure Service Health — “Is an Azure service issue affecting us?”

Azure Service Health gives a personalized view of Azure service incidents, planned maintenance, and health advisories relevant to the services, regions, and subscriptions you use. You can configure alerts for relevant events.

**Example:** A school's site hosted in Azure becomes unreachable. Before assuming the school's code is faulty, GeekHub checks Service Health for a service incident or planned maintenance that could affect its resources.

### Service Health vs. Resource Health

- **Service Health:** service-level issues, planned maintenance, and advisories that may affect your Azure environment.
- **Resource Health:** the health status of a particular Azure resource, such as a virtual machine or database.

The public Azure Status page is a global view. Service Health gives a more personalized view relevant to your subscriptions and regions.

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

### Do not confuse these tools

| Tool | Best question it answers |
|---|---|
| Azure Advisor | What improvements does Azure recommend? |
| Azure Service Health | Is an Azure service incident, maintenance event, or advisory relevant to us? |
| Azure Resource Health | What is the health status of this particular resource? |
| Azure Monitor | What is happening across my monitored resources and applications? |
| Log Analytics | What do the collected logs tell us? |
| Azure Monitor alerts | When should someone be notified about a condition? |
| Application Insights | How is my application performing, and where are its failures? |

## Knowledge check

Try answering before checking the answers.

1. Which tool recommends ways to improve cost, reliability, security, and performance?
2. Which tool gives personalized information about Azure service incidents and planned maintenance?
3. What is the difference between metrics and logs?
4. Which tool lets you query Azure Monitor log data using KQL?
5. What is the purpose of Azure Monitor alerts?
6. Which tool helps diagnose slow requests and exceptions in a web application?
7. A specific virtual machine's health status needs checking. Which health experience is most directly relevant?

### Answers

1. Azure Advisor.
2. Azure Service Health.
3. Metrics are numerical measurements over time; logs are timestamped records of events and activity.
4. Log Analytics.
5. To notify people or trigger configured actions when a monitored condition occurs.
6. Application Insights.
7. Azure Resource Health.

## Official Microsoft learning resources

- [AZ-900 exam study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900)
- [Describe monitoring tools in Azure — Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/describe-monitoring-tools-azure/)
- [Azure Monitor overview](https://learn.microsoft.com/en-us/azure/azure-monitor/fundamentals/overview)
- [Azure Monitor Logs overview](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/data-platform-logs)
- [Introduction to Azure Advisor](https://learn.microsoft.com/en-us/azure/advisor/advisor-overview)
- [Azure Service Health documentation](https://learn.microsoft.com/en-us/azure/service-health/)

## Completion checklist

- [ ] I can explain Azure Advisor and its recommendation categories.
- [ ] I can distinguish Service Health from Resource Health.
- [ ] I can explain Azure Monitor, metrics, and logs.
- [ ] I know that Log Analytics uses KQL.
- [ ] I can explain alerts and Application Insights.
- [ ] I can answer the knowledge-check questions without looking.
