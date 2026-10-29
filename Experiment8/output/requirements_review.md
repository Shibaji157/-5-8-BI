# Experiment 8 - Requirements Review

## Overall assessment

The PBIP contains report pages and semantic-model tables for all four required conduct parts. The design deliverables are substantially complete. The operational requirements are **not yet live**: Power BI Service refresh, subscriptions, workspace access, and alert recipients need to be configured after publishing. A static preview has been added, but a true Power BI screenshot still needs to be captured from Desktop or Service.

## Requirement checklist

| Requirement | Status | Evidence / notes |
|---|---|---|
| Scheduled reporting plan: daily sales, weekly profit, monthly executive dashboard, users, and cadence | Complete | `A. Scheduled Reporting Plan`; `SchedulePlan` includes owners, delivery time, and supporting jobs. |
| Distribution matrix: groups, reports, frequency, and delivery methods | Complete | `B. Distribution Matrix`; includes delivery format and access level. |
| KPI alert conditions, recipients, and actions | Complete as a design | `C. KPI Alert Configuration`; defines margin below 10%, sales decline greater than 15%, and returns increase greater than 20%, plus refresh-failure handling. |
| Regional profitability monitoring scenario | Complete as a design | `D. Monitoring Scenario`; includes detection, diagnosis, escalation, correction, and verification. |
| Dashboard screenshot | Partial | [Dashboard preview](./dashboard_overview.png) and related evidence images are included, but they are generated from workbook data and are not captures of the Power BI report. |
| Monitoring and recommendation report | Complete | [Monitoring recommendations](./monitoring_recommendations.md). |
| Power BI Service scheduling, distribution, and alerts | Pending deployment | The model/report specify a plan; no Service workspace, gateway, credentials, subscription, or notification configuration is available to verify here. |

## Data and portability checks

- The supplied workbook has 51,290 order rows and dates from 2014 through 2017. Despite the workbook filename, the order data does not contain 2018.
- The semantic-model `FilePath` previously referenced `C:\BI_Lab\Exp8\Global_Superstore_2018.xlsx`, which did not match this workspace. It now points to the workbook in the current workspace.
- The corrected path is machine-specific. If the project is moved, update the `FilePath` parameter before refreshing.
- Power BI Desktop was not available in this environment, so the PBIP could not be opened/refreshed and an actual report-page screenshot could not be captured.

## Before submission / production use

1. Open `Experiment8.pbip` in Power BI Desktop and refresh the model; resolve any local parameter or credential prompt.
2. Publish to the intended Power BI Service workspace and configure data-source credentials and the gateway, if required.
3. Configure and test the dataset refresh schedule, report subscriptions, workspace roles, and alert recipients.
4. Validate alert cards and regional results in the published report.
5. Capture a genuine dashboard screenshot from Desktop or Service and include it if the lab specifically requires an application screenshot.

## Result and learning outcomes

The project demonstrates a scheduled-reporting plan, audience-specific distribution, KPI threshold design, and a regional exception-response workflow. It supports the stated learning outcomes around reporting cadence, distribution, monitoring, and business recommendations. These remain a design demonstration until the Service-side automation is activated and tested.
