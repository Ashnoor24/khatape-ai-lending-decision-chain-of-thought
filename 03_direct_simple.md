# Step 4: Direct Prompt on a Simple Question

## Prompt Used
> Here are 8 lending scenarios for KhataPe, a digital lender.
> For each scenario, which option has the higher interest rate? Answer only A or B.
> Output a table: ID | Higher interest rate
> Scenarios: [S01 to S08 from 02_scenarios.md]

## AI Output & Audit

| ID | Higher interest rate | Correct? |
|---|---|---|
| S01 | B | ✔ |
| S02 | A | ✔ |
| S03 | A | ✔ |
| S04 | A | ✔ |
| S05 | B | ✔ |
| S06 | B | ✔ |
| S07 | A | ✔ |
| S08 | A | ✔ |

## Observation
The AI scored 8/8 using a simple direct prompt. Comparing two stated interest rates is a single-step lookup with no arithmetic or branching rules, so step-by-step reasoning is unnecessary here.
