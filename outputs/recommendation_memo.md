# Recommendation Memo

## Onboarding & Activation Campaign — A/B Experiment Results


## 1. Executive Summary

The new onboarding and activation campaign (Treatment) produced a **120.9% improvement in paid conversion rate** over the existing experience (Control), a result that is statistically significant with p = 0.0005. The campaign also showed improvements across all funnel metrics and drove faster conversions. **However, three guardrail metrics signal meaningful risk**: support ticket volume increased 67.7%, average revenue per converted user dropped 52.7%, and refund requests emerged in the Treatment group (0.42%) versus zero in Control.

**Recommendation**: **Launch with conditions** — proceed with a phased rollout targeting high-performing segments (Referral, Organic traffic; Mobile/Tablet devices; North/East regions), while investigating the root causes of elevated support tickets and lower revenue quality before full launch.

---

## 2. North Star Metric

**Paid Conversion Rate** was selected as the North Star metric because it directly measures whether the campaign achieves its core objective: turning new users into paying customers. This metric connects campaign execution to revenue generation and long-term business growth.

- Control: 3.19% (22 / 690 users)
- Treatment: 7.04% (50 / 710 users)
- **Lift: +120.9% | p-value: 0.0005**

All other funnel metrics (trial start rate, onboarding completion, engagement score) are supporting indicators that explain *how* this improvement was achieved, but the paid conversion rate is the metric that determines whether the campaign is worth launching.

Risk of over-optimizing this metric blindly: the campaign could be attracting price-sensitive or confused users who convert initially but refund, churn, or generate disproportionate support costs — eroding the LTV benefit that justifies the campaign investment.

---

## 3. KPI Tree Explanation

The KPI tree breaks down Paid Conversion Rate into three primary driver areas:

**Acquisition Funnel**: Landing page visit rate (+13.8%), trial start rate (+15.7%), and traffic source effectiveness are the top-of-funnel signals. Treatment significantly out-performed Control on both, particularly for Referral (+345% lift) and Organic (+212%) traffic sources.

**Activation & Engagement**: Onboarding completion rate improved by 35% (15.7% → 21.1%), engagement score rose 10.4% (57.0 → 62.9), and average days to convert fell 27.8% (8.9 → 6.4 days). The campaign is clearly more effective at getting users to activate quickly and deeply.

**Revenue Quality**: This is where the risk signals emerge. Average revenue per converted user fell 52.7% ($1,630 → $770), refund rate shifted from 0% to 0.42%, and support ticket rate increased 67.7%. These suggest the campaign may be converting users who are a weaker fit for the product.

---

## 4. Experiment Result Summary

| Metric | Control | Treatment | Lift | Status |
|---|---|---|---|---|
| User Count | 690 | 710 | — | Balanced |
| Landing Page Visit Rate | 63.6% | 72.4% | +13.8% | ✓ |
| Trial Start Rate | 25.1% | 29.0% | +15.7% | ✓ |
| Onboarding Completion Rate | 15.7% | 21.1% | +34.9% | ✓ |
| **Paid Conversion Rate** | **3.19%** | **7.04%** | **+120.9%** | **✓ (p<0.001)** |
| Avg Revenue per User | $51.97 | $54.25 | +4.4% | ✓ |
| Avg Revenue per Converted User | $1,630 | $770 | -52.7% | ⚠ |
| Refund Rate | 0.00% | 0.42% | New | ⚠ |
| Support Ticket Rate | 14.8% | 24.8% | +67.7% | ✗ |
| Avg Engagement Score | 57.0 | 62.9 | +10.4% | ✓ |
| Avg Days to Convert | 8.9 | 6.4 | -27.8% | ✓ |

---

## 5. Hypothesis Test Interpretation

**Test**: Two-proportion Z-test (one-tailed) on Paid Conversion Rate  
**H₀**: p_treatment ≤ p_control | **H₁**: p_treatment > p_control  
**Z-statistic**: 3.264 | **P-value**: 0.0005 | **α**: 0.05  
**Result**: Reject H₀ — the Treatment conversion rate is significantly higher.

The result is not a borderline finding. A Z-score of 3.264 is 2× the critical threshold of 1.645, meaning this level of difference would occur by chance less than 1-in-2000 times if the campaign had no real effect. The evidence that the campaign works is strong.

---

## 6. Guardrail Analysis

Three guardrail metrics raise concern and must be evaluated before full launch:

**Guardrail 1 — Support Ticket Rate (+67.7%)**  
Support ticket rate rose from 14.8% in Control to 24.8% in Treatment - a statistically significant increase (t-test p < 0.001). For every 1,000 users launched under the new campaign, approximately 100 additional support tickets would be generated. This adds cost, strains customer success capacity, and suggests the new onboarding experience may be creating confusion or unmet expectations. **Risk level: High.**

**Guardrail 2 — Revenue per Converted User (-52.7%)**  
Despite a higher volume of conversions, average revenue per converted user dropped from $1,630 to $770. While this may reflect a different mix of plan types among converters, it could also indicate that the new campaign is attracting lower-intent users who select lower-tier plans or convert on promotional terms. If this persists at scale, the LTV impact of the campaign may not justify its investment. **Risk level: High — requires root cause investigation.**

**Guardrail 3 — Refund Rate (0% → 0.42%)**  
Control had zero refund requests; Treatment had 3 users request refunds out of 710. While statistically small, the emergence of refunds in a group that previously had none is a signal worth monitoring. If the refund rate grows post-full-launch, it suggests the campaign is generating conversions that don't stick. **Risk level: Medium — monitor closely.**

**Guardrail 4 — Segment-Level Decline (Social Traffic: -21.8%)**  
Social media traffic source showed a *lower* conversion rate in Treatment vs. Control (6.06% vs. 7.75%). While not all segments need to improve, this reversal suggests the campaign may not be well-suited for social acquisition contexts, possibly due to different user intent or messaging mismatch. **Risk level: Medium.**

---

## 7. Segment-Level Insights

**Strongest performing segments in Treatment**:
- **Referral traffic**: +344.9% conversion lift (10.99% vs. 2.47%)
- **Paid Search traffic**: +384.5% lift (6.25% vs. 1.29%)
- **Organic traffic**: +211.8% lift (6.33% vs. 2.03%)
- **Tablet devices**: +292.3% lift
- **Mobile devices**: +187.2% lift
- **North region**: +155.5% lift | **East region**: +153.7% lift
- **Free plan type**: +203.6% lift — campaign strongly resonates with free users

**Underperforming segment**:
- **Social media traffic**: -21.8% — Treatment performs worse than Control; campaign likely mismatched with social user intent
- **Basic plan type**: +7.2% — minimal improvement; lowest lift across plan types

---

## 8. Final Recommendation: Launch for Selected Segments

**Recommendation**: **Conditional/Phased Launch**

Do not do a full immediate rollout. Instead:

1. **Launch to high-performing segments now**: Referral, Organic, and Paid Search traffic; Mobile and Tablet devices; North and East regions; Free plan users. These segments show strong, consistent lift with acceptable risk profiles.

2. **Exclude Social traffic** from the initial rollout until the campaign messaging is adapted to better match social user intent.

3. **Investigate revenue quality decline** before expanding: Analyze whether the drop in revenue per converted user is due to plan mix shift, discount abuse, or genuinely lower-value users. If plan mix explains it, this may be acceptable; if it signals lower LTV, the campaign economics need to be re-evaluated.

4. **Monitor guardrails weekly** for the first 4 weeks post-launch: track support ticket rate (target: below 20%), refund rate (target: below 0.5%), and revenue per converted user (target: above $1,000).

5. **Full launch decision**: Re-evaluate at 30-day post-launch checkpoint with updated guardrail data.

---

## 9. Risks and Limitations

- **Revenue quality risk** is the most significant unknown. A 52.7% drop in revenue per converted user at scale could undermine the campaign's ROI even if conversion volume doubles.
- **Support cost risk**: Each support ticket has an operational cost. At +67.7% ticket rate, the incremental cost per additional conversion must be factored into campaign economics.
- **Experiment duration**: The window of observation is 30 days. Long-term retention and churn effects are not captured. Users who converted in Treatment may exhibit higher early churn.
- **Novelty effect**: Some of the Treatment lift could be attributable to the novelty of a new onboarding experience. Performance may moderate over time.
- **Segment interactions**: Segment-level analysis is descriptive, not causal. Sub-group effects should be validated in follow-up targeted experiments before making segment-specific launch decisions.

---

## 10. Next Steps

| Action | Owner | Timeline |
|---|---|---|
| Launch campaign to approved high-performing segments | Product / Engineering | Week 1 |
| Investigate root cause of revenue quality decline | Analytics / Finance | Week 1-2 |
| Adapt campaign messaging for Social traffic | Growth / Marketing | Week 2-3 |
| Weekly guardrail monitoring dashboard | Analytics | Ongoing from launch |
| 30-day post-launch review with updated data | Business Analyst / Leadership | Day 30 |
| Full-launch or continued phased decision | Leadership | Day 30-35 |
| Follow-up A/B test targeting Social segment fix | Product | Week 4-6 |

---
