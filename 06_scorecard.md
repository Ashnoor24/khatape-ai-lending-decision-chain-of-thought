# Step 7: Step Audit, Sensitivity Test & Scorecard

**Student:** Ashnoor Kaur (2620992549) | **Tool:** Gemini AI

## Part A: Check the Working (2 Failed Direct Scenarios: S02 & S06)

| Scenario | Step | AI Result (Step 6) | Spreadsheet Result | Correct? |
| :--- | :--- | :--- | :--- | :---: |
| **S02** | Step 1 | Option A net return = `6.5%` (`26 + 2 − 11.5 − 10`) | `6.5%` | **✔** |
| **S02** | Step 2 | Option A profit = `₹3.90 crore` (`6.5% × 60`) | `₹3.90 crore` | **✔** |
| **S02** | Step 3 | Option B net return = `9.0%`, profit = `₹5.40 crore` | `9.0%`, `₹5.40 crore` | **✔** |
| **S02** | Steps 4–5 | `₹5.40 cr > ₹3.90 cr` → Choose **B** | Choose **B** | **✔** |
| **S06** | Step 1 | Option A net return = `8.5%` (`28.5 + 2 − 11 − 11`) | `8.5%` | **✔** |
| **S06** | Step 2 | Option A profit = `₹6.80 crore` (`8.5% × 80`) | `₹6.80 crore` | **✔** |
| **S06** | Step 3 | Option B net return = `10.0%`, profit = `₹8.00 crore` | `10.0%`, `₹8.00 crore` | **✔** |
| **S06** | Steps 4–5 | `₹8.00 cr > ₹6.80 cr` → Choose **B** | Choose **B** | **✔** |

## Part B: Change One Number Test (In Same Chat)

**Follow-up Prompt Sent:**
> Change only one number: in S01, Option B's expected default is now 8.5%. Recalculate S01 step by step and tell me whether the choice changes.

**AI Output & Verification:**
* **Option A (unchanged):** Net return = `6.0%`, Profit = `₹2.40 crore`.
* **Option B (updated default = 8.5%):** `21.0% + 1.5% − 8.5% − 10.0% = 4.0%` net return → Profit = `4.0% × ₹40 crore = ₹1.60 crore`.
* **Comparison & Choice:** `₹2.40 crore > ₹1.60 crore`, so the choice **changes from B to A**. Verified in Google Sheets.

## Part C: Scorecard & Answers

| What you check | Direct (Step 5) | Step by step (Step 6) |
| :--- | :---: | :---: |
| **Correct choice (out of 8)** | 5 | 8 |
| **Correct profit figure (out of 8)** | 5 | 7 |
| **Trap scenarios correct (out of 3)** | 1 | 3 |
| **Working you could check (yes / no)** | no | yes |

### Reflection Questions (~150 Words)

1. **Where was a direct answer good enough, and why? (Step 4)**  
   A direct answer worked well in Step 4 (`8/8`) when identifying which option had the higher interest rate because comparing two numbers is a single-step lookup requiring no formulas or multi-condition logic.

2. **Which scenarios did step-by-step reasoning fix? Give the scenario IDs.**  
   Chain-of-thought reasoning fixed **S02, S04, and S06**. It prevented Gemini AI from blindly picking higher-interest traps (**S02, S06**) and enforced the lower-default tie-breaker rule (**S04**).

3. **Did step-by-step working make the AI more accurate, or just more convincing? Give one example.**  
   It made the AI **both** more accurate (choices jumped from `5/8` to `8/8`) and easier to audit, though not infallible—in **S08**, clean-looking working still hid a subtraction slip (`20.5 + 1.5 − 4 − 10 = 7.5%` instead of `8.0%`).

4. **Name two things the numbers do not show that KhataPe's CFO should still consider.**  
   The model ignores **collection and recovery operating costs** on higher-default loans and **RBI digital lending guidelines** (such as Key Fact Statement disclosures, cooling-off periods, and fair-practice rate rules).
