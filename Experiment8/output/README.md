# Experiment 8 - Output Evidence

These files are supplementary evidence for the PBIP report:

- [Dashboard overview](./dashboard_overview.png) - static KPI and trend preview calculated from the supplied workbook.
- [Reporting operations design](./automation_design.png) - schedule and distribution tables read from the semantic model.
- [Regional monitoring scenario](./monitoring_scenario.png) - latest-year regional alert analysis and response playbook.
- [Requirements review](./requirements_review.md) - requirement-by-requirement assessment and remaining steps.
- [Monitoring recommendations](./monitoring_recommendations.md) - data-backed scenario findings and recommended actions.

The PNGs are generated previews, not screenshots captured from Power BI Desktop or Power BI Service. They do not prove that subscriptions, refresh schedules, or notifications are active.

The source workbook currently contains order dates from 2014 through 2017. Its filename includes "2018", but 2018 is not present in the order data. The semantic-model `FilePath` parameter points to the workbook at its current workspace location; update that parameter if the project is moved.
