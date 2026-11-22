# Step 1: The KhataPe Case Study

**KhataPe** is a fictional digital lender in Indore that gives small loans to kirana shops and college students through its app. Every month it has a fixed budget to lend and must choose between two loan products, Option A and Option B.

The CFO asks you, a Business Analyst: *"Can AI help us pick the more profitable option every month? Can we trust a quick answer, or must the AI show its working?"*

## KhataPe's Decision Rules

| Rule | Formula / Policy |
| :--- | :--- |
| **Net return** | `Interest rate + Processing fee − Expected default − Cost of funds` (all in % per year) |
| **Profit** | `Net return × Loan budget` |
| **Decision** | Choose the option with the higher profit. If both profits are equal, choose the option with the lower expected default. |
| **Ignore** | Operating costs, taxes and the timing of payments |

**Worked Example:**  
Option A: `22% interest + 2% fee − 6% default − 10% cost of funds = 8% net return`. On a `₹50 crore` budget, `profit = ₹4 crore`.  
Option B: `18% + 1% − 3% − 10% = 6% net return`, `profit = ₹3 crore`. KhataPe chooses **A**.
