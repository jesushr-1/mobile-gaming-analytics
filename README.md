# Mobile Gaming Analytics: Player Retention & A/B Testing

This project analyzes player behavior in a mobile game, focusing on two key areas: **player retention** and **monetization**.

Using registration, login activity, and A/B test data, the analysis measures exact-day retention at D1, D7, D14, and D30 and evaluates the performance of two promotional offers using **Conversion Rate, ARPU, and ARPPU**.

Statistical hypothesis testing is used to determine whether the differences between the control and test groups provide sufficient evidence to support a change in promotional strategy.

## Business Problem

Mobile games depend on both **player engagement** and **monetization** for long-term performance. Understanding whether players return after registration and how they respond to promotional offers can help guide product and marketing decisions.

This project addresses two main business questions:

1. **Player Retention:** How many players return to the game after 1, 7, 14, and 30 days from registration?

2. **Promotional Offer Performance:** Does the new promotional offer (Group B) improve monetization compared with the existing offer (Group A) without negatively affecting the proportion of players who make a purchase?

The goal is to translate player activity and revenue data into actionable insights that can support retention and monetization decisions.

## Dataset

The analysis uses three datasets from the **Gamelytics Mobile Analytics Challenge**:

- **`reg_data.csv`** — Registration data for 1,000,000 players, including the user ID (`uid`) and registration timestamp (`reg_ts`).

- **`auth_data.csv`** — More than 9.6 million player login records, containing the user ID (`uid`) and authentication timestamp (`auth_ts`).

- **`ab_test.csv`** — A/B test data for 404,770 players, including the user ID (`user_id`), revenue generated (`revenue`), and experimental group (`testgroup`).

The registration and authentication datasets are used to analyze player retention, while the A/B test dataset is used to evaluate the impact of different promotional offers on monetization.

## Key Findings

- Exact-day retention was highest at D7 (5.88%) among the analyzed checkpoints.
- Group B increased observed ARPU by 5.3% and ARPPU by 12.7%, but neither increase was statistically significant.
- Group B showed a statistically significant decrease in conversion rate.
- Based on the results, the analysis does not support replacing promotional offer A with offer B.
