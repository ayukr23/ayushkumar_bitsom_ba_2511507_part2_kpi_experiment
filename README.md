# Campaign Experiment Analysis — README

## Business Problem Statement 

### Decision to Be Made
Should the company launch the new onboarding and activation campaign (Treatment) to all users, or maintain the existing onboarding experience (Control)?

### Who the Decision Impacts
- **Product & Growth teams**: Campaign design and prioritization of activation investments
- **Revenue & Finance**: Affects short-term revenue quality and long-term LTV projections
- **Customer Success**: Support load implications from increased ticket volumes
- **Leadership**: Go/no-go call on full rollout vs. phased or conditional launch

### What Metric Should Improve
The **primary metric is Paid Conversion Rate** — the proportion of users who convert from free/trial to a paid subscription within 30 days. This is the most direct indicator of whether the new campaign is generating sustainable business value.

Secondary metrics tracked: trial start rate, onboarding completion rate, engagement score, and revenue per converted user.

### What Risks Must Be Monitored
1. **Revenue quality risk**: Average revenue per converted user dropped 52.7% in Treatment ($1,630 → $770). The campaign may be converting lower-value users.
2. **Support load risk**: Support ticket rate jumped 67.7% in Treatment (14.8% → 24.8%), indicating possible confusion or friction in the new experience.
3. **Refund risk**: Control had zero refunds; Treatment shows a 0.42% refund rate — a new signal worth watching.
4. **Segment-specific decline**: Social media traffic source showed a -21.8% conversion lift in Treatment vs. Control — the campaign may not be performing uniformly.

### What Evidence Is Required Before Making a Recommendation
- Statistically significant improvement in paid conversion rate (confirmed: p < 0.001)
- Evaluation of guardrail metrics for unintended negative side effects
- Segment-level breakdown to identify differential performance
- Hypothesis test result comparing both groups on the North Star metric
- Business interpretation connecting statistical results to real-world trade-offs

---

## Data Cleaning Log 

**Source file**: `analysis/experiment_analysis.xlsx` (uploaded as `campaign_experiment_data.xlsx`)  
**Final clean dataset**: 1,400 users (post dedup)

| Check | Finding | Count | Action Taken |
|---|---|---|---|
| Missing values — `device_type` | 18 users had no device_type recorded | 18 | Retained for primary analysis; excluded from device segment breakdown |
| Missing values — `traffic_source` | 24 users had no traffic_source | 24 | Retained; excluded from traffic source segmentation |
| Missing values — `engagement_score` | 14 users missing engagement scores | 14 | Retained; excluded from engagement averages |
| Missing values — `days_to_convert` | 1,336 users have no value | 1,336 | **Expected** — only users who converted have a days_to_convert value |
| Duplicate `user_id` entries | 8 duplicate user IDs found (4 in Control, 4 in Treatment) | 8 | Removed duplicates, kept first occurrence; final N = 1,400 |
| Invalid binary values | All binary columns (visited_landing_page, started_trial, completed_onboarding, converted_to_paid, refund_requested) contain only 0 or 1 | 0 | No action needed |
| Revenue outliers (>3σ from mean among converters) | 2 users: USR-100106 ($8,611) and USR-100303 ($6,789) | 2 | **Retained** — confirmed as real high-value transactions; flagged in analysis |
| Group balance | Control = 690, Treatment = 710 post dedup | 20 user diff | Acceptable; ~1.4% imbalance, not material to statistical conclusions |
| Segment distribution | Region, device type, traffic source, and plan type all appear balanced across groups | — | No intervention needed |
