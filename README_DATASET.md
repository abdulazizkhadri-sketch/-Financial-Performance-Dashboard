# Financial Performance Dashboard – Starter Dataset

This project uses a **synthetic practice dataset** (not real company or customer financial records).

## Files
- `financial_transactions.csv`: 2,400 transaction-level records for calendar year 2025.
- `monthly_budget.csv`: monthly revenue and expense budgets by department for 2025.

## Key fields
### financial_transactions.csv
- `transaction_id`: unique transaction identifier
- `date`: transaction date
- `department`, `region`: organizational dimensions
- `transaction_type`: Revenue or Expense
- `category`: transaction category
- `amount`: positive transaction amount; interpret using `transaction_type`
- `payment_method`: payment channel

### monthly_budget.csv
- `month`: first day of the budget month
- `department`: department
- `budget_revenue`, `budget_expenses`: planned monthly values

## Important modelling note
Do not add revenue and expense amounts together as if they were the same type. In Power BI or SQL, calculate them separately using `transaction_type`. Join monthly budgets to monthly actuals by month and department after aggregating transactions to that grain; joining raw transactions directly to monthly budgets can duplicate budget values.

## Suggested first checks
1. Confirm row counts (2,400 transactions and 72 budget rows).
2. Check missing values and duplicate transaction IDs.
3. Confirm dates cover January–December 2025.
4. Summarize revenue and expenses separately.
