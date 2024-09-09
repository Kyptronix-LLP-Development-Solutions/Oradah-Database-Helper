# Dummy Data for Oradah Software

## Users Collection

`users` collection with the three users:

| UserID     | Username         | PasswordHash                          | CreatedAt  | UpdatedAt  |
|------------|------------------|---------------------------------------|------------|------------|
| JohnDoe    | john.doe@email.com | $2y$10$U8A4D23Bz8XeI7sk1IH2LO7Pf2J.8FoS6Ih5X1t9GxV8hfrcIX2VFG | 2024-01-01 | 2024-09-08 |
| JaneSmith  | jane.smith@email.com | $2y$10$Bz8Rf1OJ9tr7HpE8v3uqfOIsPlA9rKXg6O9oN0kZ0u8CQJuq8mQ1Ha | 2024-02-01 | 2024-09-08 |
| AlexBrown  | alex.brown@email.com | $2y$10$V7j5d1V5J2TxC3Y2XaKfZeXJk4c5RzZbHi95zD7iBt95GJlTz6zd. | 2024-03-01 | 2024-09-08 |

- **Username**: Email addresses for the users.
- **PasswordHash**: Placeholder hashed passwords.
- **CreatedAt**: Account creation date.
- **UpdatedAt**: Last update date.

## Category Collection

`category` collection with 8 different `categories -> subcategory`

| UserID     | CategoryID | Category  | Subcategory         | Type     |
|------------|------------|-----------|---------------------|----------|
| JohnDoe    | cat001     | Revenue   | Sales               | Income   |
| JohnDoe    | cat002     | Revenue   | Service Income      | Income   |
| JohnDoe    | cat003     | Expense   | Office Supplies     | Expense  |
| JohnDoe    | cat004     | Expense   | Rent                | Expense  |
| JohnDoe    | cat005     | Expense   | Utilities           | Expense  |
| JohnDoe    | cat006     | Revenue   | Product Sales       | Income   |
| JohnDoe    | cat007     | Expense   | Marketing           | Expense  |
| JohnDoe    | cat008     | Revenue   | Consulting Fees     | Income   |
| JaneSmith  | cat009     | Revenue   | Consulting Fees     | Income   |
| JaneSmith  | cat010     | Expense   | Travel              | Expense  |
| JaneSmith  | cat011     | Expense   | Insurance           | Expense  |
| JaneSmith  | cat012     | Revenue   | Rental Income       | Income   |
| JaneSmith  | cat013     | Expense   | IT Services         | Expense  |
| JaneSmith  | cat014     | Expense   | Legal Fees          | Expense  |
| JaneSmith  | cat015     | Revenue   | Interest Income     | Income   |
| JaneSmith  | cat016     | Expense   | Employee Salaries   | Expense  |
| AlexBrown  | cat017     | Revenue   | Product Sales       | Income   |
| AlexBrown  | cat018     | Expense   | Advertising         | Expense  |
| AlexBrown  | cat019     | Revenue   | Royalties           | Income   |
| AlexBrown  | cat020     | Expense   | Equipment Purchase  | Expense  |
| AlexBrown  | cat021     | Revenue   | Dividend Income     | Income   |
| AlexBrown  | cat022     | Expense   | Office Supplies     | Expense  |
| AlexBrown  | cat023     | Revenue   | Asset Sale Proceeds | Income   |
| AlexBrown  | cat024     | Expense   | Employee Salaries   | Expense  |

## Accounts collection

`accounts` collection for the 3 users, each with different bank accounts, credit cards, and other accounts:


| UserID    | AccountID | AccountName          | AccountType  | OpeningBalance | DepreciationMethod          | PurchaseDate | UsefulLife | SalvageValue | AccumulatedDepreciation | RemainingUsefulLife | TotalUnitsExpected | UnitsProduced |
|-----------|-----------|----------------------|--------------|----------------|----------------------------|--------------|------------|--------------|------------------------|---------------------|-------------------|--------------|
| JohnDoe   | acc001    | Chase Checking        | Bank         | 10000.00       |                            |              |            |              |                        |                     |                   |              |
| JohnDoe   | acc002    | Chase Credit Card     | Credit Card  | 2000.00        |                            |              |            |              |                        |                     |                   |              |
| JohnDoe   | acc003    | PayPal                | Bank         | 3000.00        |                            |              |            |              |                        |                     |                   |              |
| JohnDoe   | acc004    | Investment Account    | Asset        | 5000.00        | Straight-Line               | 2015-01-10   | 10         | 500.00       | 3500.00                | 1                   |                   |              |
| JohnDoe   | acc005    | Savings Account       | Bank         | 1500.00        |                            |              |            |              |                        |                     |                   |              |
| JohnDoe   | acc006    | Business Credit Card  | Credit Card  | 500.00         |                            |              |            |              |                        |                     |                   |              |
| JohnDoe   | acc007    | Cash                  | Asset        | 2000.00        |                            |              |            |              |                        |                     |                   |              |
| JohnDoe   | acc008    | Travel Expenses       | Liability    |                |                            |              |            |              |                        |                     |                   |              |
| JaneSmith | acc009    | Wells Fargo Checking  | Bank         | 5000.00        |                            |              |            |              |                        |                     |                   |              |
| JaneSmith | acc010    | Wells Fargo Credit    | Credit Card  | 1500.00        |                            |              |            |              |                        |                     |                   |              |
| JaneSmith | acc011    | American Express      | Credit Card  | 1200.00        |                            |              |            |              |                        |                     |                   |              |
| JaneSmith | acc012    | Business Account      | Bank         | 2000.00        |                            |              |            |              |                        |                     |                   |              |
| JaneSmith | acc013    | Retirement Fund       | Asset        | 3000.00        | Double-Declining Balance    | 2018-07-01   | 15         | 400.00       | 1200.00                | 11                  |                   |              |
| JaneSmith | acc014    | Loan Payable          | Liability    |                |                            |              |            |              |                        |                     |                   |              |
| JaneSmith | acc015    | Petty Cash            | Asset        | 300.00         |                            |              |            |              |                        |                     |                   |              |
| JaneSmith | acc016    | Equipment Lease       | Liability    |                |                            |              |            |              |                        |                     |                   |              |
| AlexBrown | acc017    | Citibank Checking     | Bank         | 2000.00        |                            |              |            |              |                        |                     |                   |              |
| AlexBrown | acc018    | Citibank Credit       | Credit Card  | 1000.00        |                            |              |            |              |                        |                     |                   |              |
| AlexBrown | acc019    | Investment Fund       | Asset        | 3000.00        | Units of Production         | 2020-02-15   | 8          | 300.00       | 750.00                 | 5                   | 100000            | 35000        |
| AlexBrown | acc020    | Loan Receivable       | Asset        | 1500.00        |                            |              |            |              |                        |                     |                   |              |
| AlexBrown | acc021    | Business Loan         | Liability    |                |                            |              |            |              |                        |                     |                   |              |
| AlexBrown | acc022    | Cash                  | Asset        | 500.00         |                            |              |            |              |                        |                     |                   |              |
| AlexBrown | acc023    | Barclays Account      | Bank         | 2500.00        |                            |              |            |              |                        |                     |                   |              |
| AlexBrown | acc024    | Equipment Finance     | Liability    |                |                            |              |            |              |                        |                     |                   |              |
| SarahLee  | acc025    | Vanguard Fund         | Asset        | 10000.00       | Sum of Years Digits         | 2016-05-22   | 12         | 2000.00      | 6600.00                | 3                   |                   |              |
| SarahLee  | acc026    | Schwab Account        | Bank         | 7000.00        |                            |              |            |              |                        |                     |                   |              |
| SarahLee  | acc027    | Office Equipment      | Asset        | 5000.00        | Straight-Line               | 2019-04-01   | 5          | 1000.00      | 3200.00                | 1                   |                   |              |
| SarahLee  | acc028    | Business Savings      | Bank         | 1500.00        |                            |              |            |              |                        |                     |                   |              |
| DavidWong | acc029    | HSBC Checking         | Bank         | 2000.00        |                            |              |            |              |                        |                     |                   |              |
| DavidWong | acc030    | HSBC Credit           | Credit Card  | 3000.00        |                            |              |            |              |                        |                     |                   |              |
| DavidWong | acc031    | Industrial Equipment  | Asset        | 7000.00        | Units of Production         | 2021-08-10   | 6          | 1500.00      | 2200.00                | 4                   | 50000             | 17000        |


### Suggestions for Credit Card Accounts
- **Current Balance:** This is the amount owed on the credit card at the time of starting your records. It reflects the actual debt that the user needs to pay off. This is typically what you want to record as the opening balance.
#### Example
If a credit card account has:

Current Balance: 2000.00 (amount owed)
Credit Limit: 5000.00
You would record the Opening Balance as 2000.00.


### Managing Credit Cards and Bank Accounts
- **Bank**: For bank accounts (e.g., checking, savings).
- **Credit Card**: For credit cards.
- **Asset/Liability**: For other accounts like loans, investments, or receivables. 

## Transaction collection

`transactions` collection for all three users:


| UserID    | TransactionID | Date       | Description              | CategoryID | Amount  | AccountID | TransactionType | Notes                   |
|-----------|---------------|------------|--------------------------|------------|---------|-----------|-----------------|-------------------------|
| JohnDoe   | txn001         | 2024-01-10 | Sale of Product           | cat001     | 5000.00 | acc001    | Credit          | Product sale income     |
| JohnDoe   | txn002         | 2024-01-12 | Office Supplies Purchase  | cat003     | 150.00  | acc001    | Debit           | Office items            |
| JohnDoe   | txn003         | 2024-01-15 | Rent Payment              | cat004     | 1000.00 | acc002    | Debit           | Monthly office rent     |
| JohnDoe   | txn004         | 2024-01-20 | Marketing Expense         | cat007     | 500.00  | acc005    | Debit           | Social media marketing  |
| JohnDoe   | txn005         | 2024-01-25 | Consulting Fees           | cat008     | 2000.00 | acc003    | Credit          | Consulting income       |
| JaneSmith | txn006         | 2024-02-01 | Business Travel           | cat010     | 800.00  | acc009    | Debit           | Flight tickets          |
| JaneSmith | txn007         | 2024-02-05 | Insurance Premium         | cat011     | 1200.00 | acc010    | Debit           | Annual insurance payment|
| JaneSmith | txn008         | 2024-02-08 | Legal Services            | cat014     | 3000.00 | acc013    | Debit           | Legal fees              |
| JaneSmith | txn009         | 2024-02-12 | Interest Income           | cat015     | 500.00  | acc013    | Credit          | Interest from savings   |
| JaneSmith | txn010         | 2024-02-15 | Employee Salaries         | cat016     | 4000.00 | acc014    | Debit           | Payroll expense         |
| AlexBrown | txn011         | 2024-03-01 | Product Sales Revenue     | cat017     | 7000.00 | acc017    | Credit          | Product sale            |
| AlexBrown | txn012         | 2024-03-03 | Equipment Purchase        | cat020     | 4500.00 | acc018    | Debit           | Office equipment        |
| AlexBrown | txn013         | 2024-03-05 | Royalties Received        | cat019     | 600.00  | acc019    | Credit          | Royalties from licensing|
| AlexBrown | txn014         | 2024-03-08 | Dividend Income           | cat021     | 1500.00 | acc017    | Credit          | Investment dividends    |
| AlexBrown | txn015         | 2024-03-10 | Cash Withdrawal           | cat022     | 300.00  | acc022    | Debit           | Office petty cash       |
| JohnDoe   | txn016         | 2024-03-12 | Travel Expense            | cat005     | 250.00  | acc006    | Debit           | Business travel expense |
| JohnDoe   | txn017         | 2024-03-15 | Savings Deposit           | cat002     | 2000.00 | acc005    | Credit          | Moved to savings        |
| JaneSmith | txn018         | 2024-03-18 | IT Services Payment       | cat013     | 1200.00 | acc012    | Debit           | Outsourced IT services  |
| AlexBrown | txn019         | 2024-03-20 | Loan Repayment            | cat021     | 1000.00 | acc023    | Debit           | Loan installment        |
| AlexBrown | txn020         | 2024-03-25 | Advertising Expense       | cat018     | 800.00  | acc024    | Debit           | Google Ads              |


----




