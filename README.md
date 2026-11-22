# KhataPe Lending Decisions: Direct Answers vs Chain-of-Thought Prompting

**A FinTech case study on when AI can give a quick answer and when it must show its working.**

Author: Ashnoor Kaur (2620992549) · BBA (FinTech), Chitkara Business School · Tool: Gemini AI · November 2026

## The case
**KhataPe** (fictional) is a digital lender in Indore that lends to kirana shops and students. Every month it must choose between two loan products with different interest rates, fees and default risk. As a Business Analyst, I tested whether AI can pick the more profitable option, and whether asking it to reason step by step makes it more reliable.

## The data
8 synthetic monthly scenarios created with Gemini AI, including 3 "trap" scenarios where the higher interest rate makes less profit and 1 tie. I calculated the correct answers myself in a spreadsheet before testing.

## Decision rule
Net return = Interest rate + Processing fee − Expected default − Cost of funds  
Profit = Net return × Loan budget

## Approach
| Step | Prompt type | Task |
|---|---|---|
| 1 | Direct | Which option has the higher interest rate? |
| 2 | Direct | Which option makes more profit? (final answer only) |
| 3 | Chain-of-thought | Same decision, solved step by step |
| 4 | Chain-of-thought | One number changed: does the AI update every step? |

## Results
| Metric | Direct | Step by step |
|---|---|---|
| Correct choice (/8) | 5 | 8 |
| Correct profit figure (/8) | 5 | 7 |
| Trap scenarios correct (/3) | 1 | 3 |
| Working I could check | No | Yes |

## Key learnings
1. **A direct answer is enough for one-step questions:** Comparing interest rates across all 8 scenarios scored 8/8 without needing step-by-step instructions.
2. **Step-by-step reasoning helps multi-step decisions:** Chain-of-thought fixed S02, S04, and S06—catching both high-default traps and applying the tie-breaker rule.
3. **Convincing is not the same as correct:** In S08, Gemini AI wrote neat, confident steps but miscalculated `20.5 + 1.5 − 4 − 10` as `7.5%` instead of `8.0%` (`₹5.25 cr` vs `₹5.60 cr`).
4. **What the numbers do not show:** Recovery/collection costs for defaulted loans and RBI digital lending compliance rules.

## My recommendation to KhataPe
KhataPe should always use the **chain-of-thought prompt** (never final-answer-only prompts) for monthly product selection, and an analyst must verify every intermediate step in a spreadsheet before the CFO signs off. Following the direct prompt would have cost KhataPe ₹2.70 crore in lost profit across S02 and S06 alone.

## Skills shown
Prompt engineering · Chain-of-thought prompting · Synthetic data creation · Spreadsheet financial analysis · AI output verification · Lending business basics

## What I learned
- A direct prompt works well for simple, one-step questions.
- Chain-of-thought prompting makes AI show each step, so I can check its working instead of trusting one number.
- Step-by-step working can look convincing and still contain a wrong number, so every step must be checked.
- How to create synthetic business scenarios with AI, including deliberate "trap" cases.
- Why I calculate my own answer key in a spreadsheet before testing AI.
- Changing one number is a quick test of whether AI really reasons or just repeats.
- Numbers alone do not make a lending decision; risk and regulation matter too.

*KhataPe and all data in this project are fictional and created for learning.*
