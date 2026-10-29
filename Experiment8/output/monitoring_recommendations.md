# Monitoring and Recommendation Report

## Executive summary

The supplied Global Superstore workbook contains order data for 2014-2017. Using the latest available year (2017) against 2016, sales increased by **26.3%**, while returned orders increased by **21.3%**. The global 2017 profit margin was approximately **11.7%**, above the 10% threshold, but **9 of 23 regions** were below that target. The returns rule is therefore the global year-over-year exception, while the regional margin view identifies localized profitability risks.

These are historical calculations from the supplied workbook, not live Power BI Service notifications.

## Monitoring results

| KPI | 2017 result | Rule | Assessment |
|---|---:|---|---|
| Sales year-over-year | +26.3% | Alert below -15% | No global sales-decline alert |
| Returned orders year-over-year | +21.3% | Alert above +20% | **Threshold exceeded** |
| Global profit margin | 11.7% | Alert below 10% | Above target |
| Regional profit margin | 9 of 23 regions below 10% | Alert below 10% | **Investigate affected regions** |

The lowest 2017 regional margins include Central Asia (**-25.8%**), Western Africa (**-14.8%**), and Western Asia (**-10.6%**). These are investigation priorities, not proof of a specific cause.

## Recommended response

1. **Detect and assign:** Notify each Regional Head and the Finance Manager when regional margin is below 10%; notify Operations and Customer Service when returns exceed the 20% year-over-year threshold.
2. **Validate the signal:** Confirm the selected period, returned-order definition, regional mapping, and refresh timestamp before escalating.
3. **Diagnose drivers:** Drill into state/city, category/sub-category, discount, shipping cost, and product-level profit. Compare affected segments with profitable peers.
4. **Take controlled action:** Assign owners to review pricing, discount exceptions, freight costs, and product quality. Avoid broad changes until the drivers are evidenced.
5. **Verify and close:** Review the next weekly profit report and returns monitor. Close an issue only after the metric recovers and the owner records the corrective action.

## Operational recommendations

- Preserve the defined 06:00 refresh-before-delivery sequence and monitor refresh failures before sending scheduled reports.
- Test subscriptions and alert rules with named recipients in the target Power BI Service workspace.
- Restrict report access by business role and confirm that exported PDF/Excel files follow the organization's sharing policy.
- Review thresholds and recipient ownership periodically; document alert acknowledgement and resolution.
- The workbook name suggests 2018, but its latest order year is 2017. Confirm whether a newer source file is expected before relying on this analysis operationally.

## Conclusion

The model provides the required monitoring blueprint and usable historical exception analysis. The next step is publishing and validating the workflow in Power BI Service; the images in this folder are static previews and do not represent active alerting or report delivery.
