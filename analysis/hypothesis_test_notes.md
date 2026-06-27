# Hypothesis Test Notes — Campaign A/B Experiment

## Metric Being Tested
**Paid Conversion Rate** — proportion of users who converted to a paid subscription within 30 days.

## Reason for Choosing This Metric
Paid Conversion Rate is the North Star metric for this experiment. It directly measures whether the new onboarding and activation campaign achieves its stated objective: converting more users to paying customers. All other metrics (trial start rate, onboarding completion, engagement score) are leading indicators — useful, but subordinate. The business decision of "should we launch this campaign?" is ultimately answered by whether it moves paid conversions.

---

## Hypothesis Framing (Task 6)

| Element | Statement |
|---|---|
| **Null Hypothesis (H₀)** | The paid conversion rate for the Treatment group is equal to (or less than) the Control group: p_treatment ≤ p_control |
| **Alternate Hypothesis (H₁)** | The paid conversion rate for the Treatment group is greater than the Control group: p_treatment > p_control |
| **Test Type** | One-tailed (right-sided) — we are specifically testing for improvement, not just difference |
| **Statistical Test** | Two-proportion Z-test |
| **Significance Level (α)** | 0.05 (95% confidence) |

**Connection to business decision**: Rejecting H₀ means there is statistically significant evidence that the new campaign produces a higher conversion rate, which would support a launch recommendation. Failing to reject H₀ would mean the campaign's observed improvement could be due to chance, and a launch would not be justified on this evidence alone.

---

## Test Inputs (Task 7)

| Input | Value |
|---|---|
| Control group size (n₁) | 690 |
| Treatment group size (n₂) | 710 |
| Control conversions | 22 |
| Treatment conversions | 50 |
| Control conversion rate (p̂₁) | 3.19% |
| Treatment conversion rate (p̂₂) | 7.04% |
| Pooled proportion (p̂) | 5.14% |
| Standard Error | 0.01181 |

---

## Test Output

| Output | Value |
|---|---|
| Z-statistic | **3.264** |
| P-value (one-tailed) | **0.0005** |
| Critical value at α = 0.05 | 1.645 |
| Decision rule | Reject H₀ if Z > 1.645 |
| **Decision** | **REJECT H₀** |

**Z-statistic calculation**:  
Z = (p̂₂ − p̂₁) / SE = (0.0704 − 0.0319) / 0.01181 = **3.264**

---

## Interpretation

The Z-statistic of 3.264 falls well beyond the critical value of 1.645. The p-value of 0.0005 means there is only a 0.05% probability of observing this large a difference in conversion rates if the null hypothesis were true.

**Business Interpretation**: The new onboarding and activation campaign (Treatment) produces a statistically significant improvement in paid conversion rate — from 3.19% to 7.04%, a **120.9% relative lift**. This result is highly unlikely to be due to random sampling variation. The evidence strongly supports the campaign's effectiveness at driving paid conversions.

However, statistical significance alone does not mean the campaign should be launched without conditions. The guardrail analysis (Task 8) introduces important caveats that must be considered alongside this finding.

---
