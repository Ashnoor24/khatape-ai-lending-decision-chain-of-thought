# Step 6: Chain-of-Thought on the Same Decision (Step-by-Step Working)

**Tool:** Gemini AI

## Prompt Used
```text
You are a financial analyst at KhataPe, a digital lender.
For each scenario below, decide which option KhataPe should choose to earn the higher profit.
Rules:
Net return = Interest rate + Processing fee − Expected default − Cost of funds
Profit = Net return × Loan budget
If both profits are equal, choose the option with the lower expected default.
Think step by step. For each scenario:
Step 1: Write the four numbers for Option A and calculate its net return.
Step 2: Calculate Option A's profit in ₹ crore.
Step 3: Repeat Steps 1 and 2 for Option B.
Step 4: Compare the two profits and apply the tie rule if needed.
Step 5: State the choice.
Show your working for every scenario, then give a final summary table: ID | A profit (₹ crore) | B profit (₹ crore) | Choice
Scenarios: [S01 to S08 pasted]
```

## AI Step-by-Step Working (Key Scenarios)

### S02 (Trap Scenario #1)
* **Step 1:** Option A: `26.0% + 2.0% − 11.5% − 10.0% = 6.5%` net return.
* **Step 2:** Option A profit: `6.5% × ₹60 crore = ₹3.90 crore`.
* **Step 3:** Option B: `19.0% + 1.0% − 2.0% − 9.0% = 9.0%` net return. Profit: `9.0% × ₹60 crore = ₹5.40 crore`.
* **Step 4:** ₹5.40 crore > ₹3.90 crore. No tie.
* **Step 5:** Choose **B**.

### S04 (Tie Scenario)
* **Step 1:** Option A: `22.0% + 2.0% − 6.0% − 10.0% = 8.0%` net return.
* **Step 2:** Option A profit: `8.0% × ₹50 crore = ₹4.00 crore`.
* **Step 3:** Option B: `19.0% + 1.0% − 2.0% − 10.0% = 8.0%` net return. Profit: `8.0% × ₹50 crore = ₹4.00 crore`.
* **Step 4:** Both profits equal ₹4.00 crore; apply tie rule: Option B has lower expected default (`2.0%` vs `6.0%`).
* **Step 5:** Choose **B**.

### S08 (Arithmetic Slip Example)
* **Step 1:** Option A: `17.5% + 1.5% − 3.0% − 9.5% = 6.5%` net return.
* **Step 2:** Option A profit: `6.5% × ₹70 crore = ₹4.55 crore`.
* **Step 3:** Option B: `20.5% + 1.5% − 4.0% − 10.0% = 7.5%` *(Error: actual is 8.0%)*. Profit: `7.5% × ₹70 crore = ₹5.25 crore` *(Actual: ₹5.60 crore)*.
* **Step 4:** ₹5.25 crore > ₹4.55 crore.
* **Step 5:** Choose **B**.

---

## AI Final Summary Table & Evaluation Against Answer Key

| ID | A profit (₹ cr) | B profit (₹ cr) | AI Choice | Choice Mark | Profit Mark | Comparison vs. Direct |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| **S01** | 2.40 | 3.20 | B | ✔ | ✔ | Maintained accuracy. |
| **S02** | 3.90 | 5.40 | B | ✔ | ✔ | **FIXED (Trap #1):** Step-by-step subtraction caught high default on A. |
| **S03** | 1.80 | 1.20 | A | ✔ | ✔ | Maintained accuracy. |
| **S04** | 4.00 | 4.00 | B | ✔ | ✔ | **FIXED (Tie Rule):** Explicit comparison triggered lower-default rule. |
| **S05** | 2.475 | 2.25 | A | ✔ | ✔ | Maintained accuracy. |
| **S06** | 6.80 | 8.00 | B | ✔ | ✔ | **FIXED (Trap #3):** Calculated B's higher net return accurately. |
| **S07** | 2.20 | 1.40 | A | ✔ | ✔ | Maintained accuracy. |
| **S08** | 4.55 | **5.25** *(5.60)* | B | ✔ | **✘** | Right choice, but neat working hid a subtraction slip (`7.5%` vs `8.0%`). |

### Step 6 Totals
* **Correct choice:** 8 / 8
* **Correct profit figure:** 7 / 8
* **Trap scenarios correct:** 3 / 3
* **Working I could check:** Yes
