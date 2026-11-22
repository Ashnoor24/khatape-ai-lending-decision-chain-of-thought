# Step 6: Chain-of-Thought Prompt on the Real Lending Decision

## Prompt Used
> You are a financial analyst at KhataPe, a digital lender.
> For each scenario below, decide which option KhataPe should choose to earn the higher profit.
>
> Rules:
> Net return = Interest rate + Processing fee − Expected default − Cost of funds
> Profit = Net return × Loan budget
> If both profits are equal, choose the option with the lower expected default.
>
> Think step by step. For each scenario:
> Step 1: Write the four numbers for Option A and calculate its net return.
> Step 2: Calculate Option A's profit in ₹ crore.
> Step 3: Repeat Steps 1 and 2 for Option B.
> Step 4: Compare the two profits and apply the tie rule if needed.
> Step 5: State the choice.
>
> Show your working for every scenario, then give a final summary table: ID | A profit (₹ crore) | B profit (₹ crore) | Choice
> Scenarios: [Same S01 to S08 from 02_scenarios.md]

## Step-by-Step AI Working

### S01 (Budget: ₹50 crore)
- **Step 1 (Option A):** 18.0% + 1.5% − 3.5% − 10.0% = 6.0%
- **Step 2 (A Profit):** 6.0% × ₹50 cr = ₹3.00 crore
- **Step 3 (Option B):** 21.0% + 2.0% − 4.0% − 10.0% = 9.0% → 9.0% × ₹50 cr = ₹4.50 crore
- **Step 4 (Compare):** ₹4.50 cr > ₹3.00 cr
- **Step 5 (Choice):** **B**

### S02 (Budget: ₹60 crore)
- **Step 1 (Option A):** 26.0% + 2.0% − 11.0% − 10.0% = 7.0%
- **Step 2 (A Profit):** 7.0% × ₹60 cr = ₹4.20 crore
- **Step 3 (Option B):** 20.0% + 1.5% − 3.5% − 9.5% = 8.5% → 8.5% × ₹60 cr = ₹5.10 crore
- **Step 4 (Compare):** ₹5.10 cr > ₹4.20 cr
- **Step 5 (Choice):** **B**

### S03 (Budget: ₹30 crore)
- **Step 1 (Option A):** 20.0% + 2.0% − 3.0% − 9.0% = 10.0%
- **Step 2 (A Profit):** 10.0% × ₹30 cr = ₹3.00 crore
- **Step 3 (Option B):** 16.0% + 1.0% − 2.0% − 9.0% = 6.0% → 6.0% × ₹30 cr = ₹1.80 crore
- **Step 4 (Compare):** ₹3.00 cr > ₹1.80 cr
- **Step 5 (Choice):** **A**

### S04 (Budget: ₹80 crore)
- **Step 1 (Option A):** 22.0% + 2.0% − 6.0% − 10.0% = 8.0%
- **Step 2 (A Profit):** 8.0% × ₹80 cr = ₹6.40 crore
- **Step 3 (Option B):** 19.0% + 1.5% − 3.5% − 9.0% = 8.0% → 8.0% × ₹80 cr = ₹6.40 crore
- **Step 4 (Compare):** Equal profit (₹6.40 cr each). Tie rule: B has lower expected default (3.5% vs 6.0%).
- **Step 5 (Choice):** **B**

### S05 (Budget: ₹75 crore)
- **Step 1 (Option A):** 18.0% + 1.0% − 2.0% − 9.0% = 8.0%
- **Step 2 (A Profit):** 8.0% × ₹75 cr = ₹6.00 crore
- **Step 3 (Option B):** 28.0% + 2.5% − 12.0% − 11.5% = 7.0% → 7.0% × ₹75 cr = ₹5.25 crore
- **Step 4 (Compare):** ₹6.00 cr > ₹5.25 cr
- **Step 5 (Choice):** **A**

### S06 (Budget: ₹25 crore)
- **Step 1 (Option A):** 15.0% + 1.0% − 2.5% − 8.5% = 5.0%
- **Step 2 (A Profit):** 5.0% × ₹25 cr = ₹1.25 crore
- **Step 3 (Option B):** 21.0% + 1.5% − 4.5% − 10.0% = 8.0% → 8.0% × ₹25 cr = ₹2.00 crore
- **Step 4 (Compare):** ₹2.00 cr > ₹1.25 cr
- **Step 5 (Choice):** **B**

### S07 (Budget: ₹90 crore)
- **Step 1 (Option A):** 27.0% + 3.0% − 11.5% − 11.5% = 7.0%
- **Step 2 (A Profit):** 7.0% × ₹90 cr = ₹6.30 crore
- **Step 3 (Option B):** 19.5% + 1.5% − 2.5% − 10.5% = 8.0% → 8.0% × ₹90 cr = ₹7.20 crore
- **Step 4 (Compare):** ₹7.20 cr > ₹6.30 cr
- **Step 5 (Choice):** **B**

### S08 (Budget: ₹40 crore)
- **Step 1 (Option A):** 23.0% + 2.5% − 5.0% − 10.5% = 10.0%
- **Step 2 (A Profit):** 10.0% × ₹40 cr = ₹4.00 crore
- **Step 3 (Option B):** 17.0% + 1.0% − 2.0% − 9.5% = 6.5% → 6.5% × ₹40 cr = ₹2.60 crore
- **Step 4 (Compare):** ₹4.00 cr > ₹2.60 cr
- **Step 5 (Choice):** **A**

---

## Final Summary Table & Audit

| ID | A profit (₹ crore) | B profit (₹ crore) | Choice | Audit (Choice & Profit) |
|---|---|---|---|---|
| S01 | ₹3.00 | ₹4.50 | B | ✔ / ✔ |
| S02 | ₹4.20 | ₹5.10 | B | ✔ / ✔ |
| S03 | ₹3.00 | ₹1.80 | A | ✔ / ✔ |
| S04 | ₹6.40 | ₹6.40 | B | ✔ / ✔ |
| S05 | ₹6.00 | ₹5.25 | A | ✔ / ✔ |
| S06 | ₹1.25 | ₹2.00 | B | ✔ / ✔ |
| S07 | ₹6.30 | ₹7.20 | B | ✔ / ✔ |
| S08 | ₹4.00 | ₹2.60 | A | ✔ / ✔ |

## Step 6 Score Summary
- **Correct choice:** 8 / 8
- **Correct profit figure:** 8 / 8
- **Trap scenarios correct:** 3 / 3
- **Working you could check:** Yes
