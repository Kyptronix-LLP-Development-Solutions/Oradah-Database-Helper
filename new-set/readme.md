
### 1. **Categories**

| **CategoryID** | **Category**         | **Subcategory**            | **Type** |
| -------------- | --------------------- | -------------------------- | -------- |
| cat001          | Revenue               | Sales                      | Income   |
| cat002          | Revenue               | Service Income             | Income   |
| cat003          | Expense               | Office Supplies            | Expense  |
| cat004          | Expense               | Rent                      | Expense  |
| cat005          | Expense               | Utilities                  | Expense  |
| cat006          | Revenue               | Product Sales              | Income   |
| cat007          | Expense               | Marketing                  | Expense  |
| cat008          | Revenue               | Consulting Fees            | Income   |
| cat009          | COGS                  | Direct Materials           | Expense  |
| cat010          | COGS                  | Direct Labor               | Expense  |
| cat011          | COGS                  | Manufacturing Overhead     | Expense  |
| cat012          | Asset                 | Equipment                  | Asset    |
| cat013          | Liability             | Accounts Payable           | Liability|
| cat014          | Liability             | Short-Term Loans           | Liability|
| cat015          | Equity                | Owner's Capital            | Equity   |
| cat016          | Equity                | Retained Earnings          | Equity   |

### 2. **Accounts**

| **AccountID** | **AccountName**     | **Type**    |
| ------------- | ------------------- | ----------- |
| acc001        | Cash                | Asset       |
| acc002        | Accounts Payable    | Liability   |
| acc003        | Bank Account        | Asset       |
| acc004        | Loan Account        | Liability   |
| acc005        | Owner's Equity      | Equity      |

### 3. **Transactions**

| **UserID** | **TransactionID** | **Date**    | **Description**                  | **CategoryID** | **Amount** | **AccountID** | **TransactionType** | **Notes**                      |
| ---------- | ------------------ | ----------- | -------------------------------- | -------------- | ---------- | ------------- | -------------------- | --------------------------------|
| JohnDoe    | txn001             | 2024-01-05  | Sale of Product A                | cat001         | 5,000.00   | acc001        | Credit               | Revenue from product sales     |
| JohnDoe    | txn002             | 2024-01-10  | Service Income                   | cat002         | 2,000.00   | acc001        | Credit               | Income from consulting services|
| JohnDoe    | txn003             | 2024-01-15  | Office Supplies Purchase         | cat003         | 150.00     | acc003        | Debit                | Office supplies expense        |
| JohnDoe    | txn004             | 2024-02-01  | Rent Payment                     | cat004         | 1,000.00   | acc003        | Debit                | Monthly office rent            |
| JohnDoe    | txn005             | 2024-02-10  | Utility Bill                     | cat005         | 200.00     | acc003        | Debit                | Utilities expense              |
| JohnDoe    | txn006             | 2024-03-01  | Purchase of Raw Materials        | cat009         | 3,000.00   | acc003        | Debit                | Raw materials for production   |
| JohnDoe    | txn007             | 2024-03-05  | Wages for Production Workers     | cat010         | 1,500.00   | acc003        | Debit                | Labor cost                     |
| JohnDoe    | txn008             | 2024-03-10  | Factory Utilities                | cat011         | 500.00     | acc003        | Debit                | Manufacturing overhead         |
| JohnDoe    | txn009             | 2024-03-15  | Payment to Supplier              | cat013         | 2,000.00   | acc003        | Debit                | Accounts payable               |
| JohnDoe    | txn010             | 2024-03-20  | Short-Term Loan Received         | cat014         | 4,000.00   | acc004        | Credit               | Loan received                  |
| JohnDoe    | txn011             | 2024-04-01  | Owner's Capital Investment       | cat015         | 5,000.00   | acc005        | Credit               | Owner's equity                 |
| JohnDoe    | txn012             | 2024-04-15  | Retained Earnings Transfer       | cat016         | 2,000.00   | acc005        | Credit               | Retained earnings adjustment   |

### 4. **Income Statement**

**For the Period: January 1, 2024 – December 31, 2024**

| **Revenue**                     |                          |  
| -------------------------------- | ------------------------ |  
| Sales of Product A               | $5,000                   |  
| Service Income                  | $2,000                   |  
| **Total Revenue**               | **$7,000**              |

---

| **COGS**                        |                          |  
| -------------------------------- | ------------------------ |  
| Purchase of Raw Materials        | $3,000                   |  
| Wages for Production Workers     | $1,500                   |  
| Factory Utilities                | $500                     |  
| **Total COGS**                   | **$5,000**              |

---

| **Gross Profit**                |                          |  
| **Total Revenue - Total COGS**   | **$2,000**              |

---

| **Expenses**                    |                          |  
| -------------------------------- | ------------------------ |  
| Office Supplies Purchase         | $150                     |  
| Rent Payment                    | $1,000                   |  
| Utility Bill                    | $200                     |  
| **Total Expenses**              | **$1,350**              |

---

| **Net Income**                  |                          |  
| **Gross Profit - Total Expenses**| **$650**               |

### 5. **Balance Sheet**

**As of December 31, 2024**

| **Assets**                      |                          |  
| -------------------------------- | ------------------------ |  
| Cash                            | $5,000                   |  
| Bank Account                    | $4,000                   |  
| Equipment                       | $2,500                   |  
| **Total Assets**                | **$11,500**             |

---

| **Liabilities**                 |                          |  
| -------------------------------- | ------------------------ |  
| Accounts Payable                | $2,000                   |  
| Short-Term Loans                | $4,000                   |  
| **Total Liabilities**           | **$6,000**              |

---

| **Equity**                      |                          |  
| -------------------------------- | ------------------------ |  
| Owner's Capital                 | $5,000                   |  
| Retained Earnings               | $2,000                   |  
| **Total Equity**                | **$7,000**              |

---

| **Total Liabilities & Equity**  | **$13,000**             |

This data provides a complete overview for JohnDoe, including categories, transactions, an income statement, and a balance sheet.

----
The income statement focuses on income and expenses. It does not include assets, liabilities, or equity. Here’s a quick breakdown of where each category fits in financial statements:

- **Income Statement**: Shows revenues (income) and expenses. It calculates net income or loss for a specific period.

- **Balance Sheet**: Displays assets, liabilities, and equity at a specific point in time. It provides a snapshot of what the business owns and owes.

- **Cash Flow Statement**: Shows the cash inflows and outflows from operating, investing, and financing activities.

- **Statement of Changes in Equity**: Details the changes in equity over a period, including contributions, distributions, and retained earnings.

So, for the income statement, only the categories with the type "Income" and "Expense" are relevant.
