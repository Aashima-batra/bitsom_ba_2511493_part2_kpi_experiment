# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and engagement. Users were randomly assigned into two groups:

* Control Group: Existing onboarding experience
* Treatment Group: New onboarding and activation campaign

The objective is to determine whether the new onboarding experience should be rolled out to all users.

---

## Business Problem Statement

The leadership team needs to decide whether the new onboarding campaign should be launched to all users.

This decision impacts:

* Product Team
* Marketing Team
* Customer Success Team
* Revenue Growth Team

The primary objective is to improve paid conversion while maintaining healthy customer experience and revenue quality.

Potential risks include:

* Increased support tickets
* Higher refund rates
* Reduced user satisfaction
* Poor performance within specific customer segments

Evidence required before launch:

* Statistically significant improvement in conversion
* Positive business impact
* No critical deterioration in guardrail metrics

---

## Dataset Description

Dataset: campaign_experiment_data.xlsx

Key Variables:

* Experiment Group
* Region
* Device Type
* Traffic Source
* Plan Type
* Landing Page Visit
* Trial Start
* Onboarding Completion
* Paid Conversion
* Revenue
* Refund Request
* Support Tickets
* Engagement Score
* Days to Convert

Total Users: 1,408

---

## Data Quality Checks

The following checks were performed:

### Missing Values

* device_type: 18 missing
* traffic_source: 24 missing
* engagement_score: 14 missing

### Duplicate Records

* 8 duplicate user IDs identified

### Binary Validation

Binary columns validated:

* visited_landing_page
* started_trial
* completed_onboarding
* converted_to_paid
* refund_requested

No invalid values found.

### Outlier Review

Revenue distribution reviewed for unusual values.

### Segment Validation

Distribution reviewed across:

* Region
* Device Type
* Traffic Source
* Plan Type

---

## North Star Metric

### Paid Conversion Rate

Formula:

Paid Converted Users / Total Users

Why selected:

* Directly linked to subscription revenue
* Reflects onboarding effectiveness
* Supports long-term business growth
* Primary decision metric for launch evaluation

Risk of optimizing blindly:

* Higher support costs
* Increased refunds
* Poor user experience

---

## KPI Tree Summary

North Star Metric:

* Paid Conversion Rate

Primary Drivers:

1. Acquisition Effectiveness
2. Onboarding Effectiveness
3. User Engagement

Guardrail Metrics:

* Refund Rate
* Support Ticket Rate
* Days to Convert

---

## Experiment Analysis Approach

1. Data cleaning
2. Duplicate validation
3. Missing value review
4. Metric comparison between Control and Treatment
5. Hypothesis testing
6. Guardrail evaluation
7. Segment analysis
8. Recommendation development

---

## Hypothesis Test Summary

Test Type:
Two-Proportion Z-Test

Metric Tested:
Paid Conversion Rate

Null Hypothesis:
There is no difference between Control and Treatment conversion rates.

Alternative Hypothesis:
Treatment conversion rate is higher than Control conversion rate.

Significance Level:
0.05

Result:
p-value ≈ 0.00055

Decision:
Reject Null Hypothesis.

Interpretation:
The Treatment experience significantly improves paid conversion.

---

## Guardrail Metrics Considered

1. Refund Rate
2. Support Ticket Rate
3. Days to Convert
4. Engagement Score

Key Finding:
Support tickets increased under Treatment and should be monitored post-launch.

---

## Final Recommendation

Launch the Treatment experience.

Reasoning:

* Significant increase in conversion rate
* Improved engagement score
* Revenue impact is positive
* Refund rate remains low

Monitor support ticket volume after rollout.

---

## Assumptions and Limitations

* Random assignment is assumed valid.
* Dataset represents actual customer behavior.
* Long-term retention data was unavailable.
* Analysis limited to available experiment duration.

---

## Screenshots Included

* summary_metrics.png
* hypothesis_test_output.png
* kpi_tree_preview.png
