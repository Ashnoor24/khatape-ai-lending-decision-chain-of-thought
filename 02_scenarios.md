# Step 2 & Step 3: Synthetic Lending Scenarios & Spreadsheet Answer Key

**Student:** Ashnoor Kaur (2620992549) | **AI Tool:** Gemini AI

## Step 2: 8 Monthly Decision Scenarios (S01 to S08)

| ID | Budget (₹ crore) | A interest | A fee | A default | A cost of funds | B interest | B fee | B default | B cost of funds |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **S01** | 40 | 17.5% | 1.0% | 3.0% | 9.5% | 21.0% | 1.5% | 4.5% | 10.0% |
| **S02** | 60 | 26.0% | 2.0% | 11.5% | 10.0% | 19.0% | 1.0% | 2.0% | 9.0% |
| **S03** | 30 | 16.0% | 1.5% | 2.5% | 9.0% | 14.5% | 0.5% | 2.0% | 9.0% |
| **S04** | 50 | 22.0% | 2.0% | 6.0% | 10.0% | 19.0% | 1.0% | 2.0% | 10.0% |
| **S05** | 45 | 15.0% | 1.0% | 2.0% | 8.5% | 27.5% | 1.5% | 12.0% | 12.0% |
| **S06** | 80 | 28.5% | 2.0% | 11.0% | 11.0% | 22.0% | 1.0% | 3.5% | 9.5% |
| **S07** | 20 | 24.0% | 2.0% | 5.0% | 10.0% | 18.0% | 1.0% | 3.0% | 9.0% |
| **S08** | 70 | 17.5% | 1.5% | 3.0% | 9.5% | 20.5% | 1.5% | 4.0% | 10.0% |

### Dataset Audit Note (Checked Before Running Decision Prompts)
* **3 Trap Scenarios Included:** **S02** (A has 26% vs 19% interest, but earns ₹3.90 cr vs B's ₹5.40 cr), **S05** (B has 27.5% vs 15% interest, but earns ₹2.25 cr vs A's ₹2.475 cr), and **S06** (A has 28.5% vs 22% interest, but earns ₹6.80 cr vs B's ₹8.00 cr).
* **1 Tie Scenario Included:** **S04** (both Option A and Option B yield 8.0% net return = ₹4.00 crore profit; tie rule selects Option B due to lower expected default of 2.0% vs 6.0%).

---

## Step 3: Spreadsheet Answer Key (Calculated Before Testing AI)

*Spreadsheet formula used:* Net Return = Interest + Fee - Default - Cost_of_Funds | Profit = (Net_Return / 100) * Budget

| ID | A net return % | A profit (₹ cr) | B net return % | B profit (₹ cr) | Correct choice | Scenario Type |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| **S01** | 6.0% | 2.40 | 8.0% | 3.20 | **B** | Standard |
| **S02** | 6.5% | 3.90 | 9.0% | 5.40 | **B** | Trap #1 (A higher rate, lower profit) |
| **S03** | 6.0% | 1.80 | 4.0% | 1.20 | **A** | Standard |
| **S04** | 8.0% | 4.00 | 8.0% | 4.00 | **B** | Tie (B lower default: 2% vs 6%) |
| **S05** | 5.5% | 2.475 *(2.48)* | 5.0% | 2.25 | **A** | Trap #2 (B higher rate, lower profit) |
| **S06** | 8.5% | 6.80 | 10.0% | 8.00 | **B** | Trap #3 (A higher rate, lower profit) |
| **S07** | 11.0% | 2.20 | 7.0% | 1.40 | **A** | Standard |
| **S08** | 6.5% | 4.55 | 8.0% | 5.60 | **B** | Standard |
