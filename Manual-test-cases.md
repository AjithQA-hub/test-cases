# Manual Test Cases – Firefly finance App

**Base URL:**  
[https://finance-app-demo.com](https://demo.firefly-iii.org/login)

## Login Test Data

### Valid Credentials

| Field | Value |
|---------|---------|
| Email | demo@firefly-iii.org |
| Password | demo |

## Module: Transactions

## Test Cases

| TC ID | Test Description | Steps | Test Data | Expected Result | Priority |
|-------|------------------|-------|-----------|-----------------|----------|
| TC_001 | Verify user can add a transaction with valid information | 1. Login to the application.<br/>2. Click the expenses under the transactions and it navigates to the transaction list page.<br/>3. Click the create a new transaction button and it navigates to the Transaction information page.<br/>4. Enter the required fields and other fields.<br/>5. Click the submit button. |  | Transaction is added successfully and appears in transaction history list. | High |
| TC_002 | Verify user can edit the transaction with valid information | 1. Login to the application.<br/>2. Click the expenses under the transactions and it navigates to the transaction list page.<br/>3. Select any expenses and click the edit option under the actions dropdown.<br/>4. Navigates to the Transaction information page and edit the details.<br/>5. Click the submit button. |  | Transaction is updated successfully and the modified details are displayed correctly in the transaction history list. | High |
| TC_003 | Verify the delete expenses from the list page | 1. Login to the application.<br/>2. Click the expenses under the transactions and it navigates to the transaction list page.<br/>3. Select any expenses and click the delete option under the actions dropdown.<br/>4. Navigates to the delete transaction page.<br/>5. Click the Delete permanently button. |  | Transaction is deleted successfully and deleted transaction should not be shown in the transaction history list. | High |
| TC_004 | Verify the transaction convert a withdrawal into a deposit | 1. Login to the application.<br/>2. Click the description text and navigates to the Transaction information page.<br/>3. Select convert to a deposit button under Transaction information Actions dropdown.<br/>4. Navigates to the transaction page and select any source account.<br/>5. Click the convert withdrawal button. |  | Transaction is converted to a deposit and success message should be displayed and type status should be changed into Deposit. | Medium |
| TC_005 | Verify the validation messages is displayed when required fields are left empty | 1. Login to the application.<br/>2. Click the expenses under the transactions and it navigates to the transaction list page.<br/>3. Click the create a new transaction button and it navigates to the Transaction information page.<br/>4. Leave all required fields empty.<br/>5. Click the Submit button. |  | Appropriate validation messages should be displayed for mandatory fields, and the transaction should not be saved. | High |
| TC_006 | Verify the user cannot transfer amount to the same account. | 1. Login to the application.<br/>2. Click the expenses under the transactions and it navigates to the transaction list page.<br/>3. Click the create a new transaction button and it navigates to the Transaction information page.<br/>4. Enter all the required fields and source account & Destination account should be same.<br/>5. Click the submit button. | Source account: Credit card in USD<br/>Destination account: Credit card in USD | Appropriate validation message "Source and destination are the same." should be displayed under the destination account text field. | High |
| TC_007 | Verify the validation message user enter amount with the invalid currency id. | 1. Login to the application.<br/>2. Click the expenses under the transactions and it navigates to the transaction list page.<br/>3. Click the create a new transaction button and it navigates to the Transaction information page.<br/>4. Enter all the required fields and select the Source account and Destination account should be mention in Test Data.<br/>5. Click the submit button. | Source account: Checking Account<br/>Destination account: Starbucks<br/>Currency id should be None | Appropriate validation message "The selected transactions.0.foreign_currency_id is invalid." should be displayed under the Foreign amount. | High |
| TC_008 | Verify transaction amount validation message when user entered above the boundary values. | 1. Login to the application.<br/>2. Click the expenses under the transactions and it navigates to the transaction list page.<br/>3. Click the create a new transaction button and it navigates to the Transaction information page.<br/>4. Enter all the required fields and enter the Amount field should be above the boundary value 10019092020.<br/>5. Click the submit button. | Amount: 4561456454584 | Appropriate validation messages should be displayed under the Amount text box field. | High |

---

## Coverage Summary

### Positive Test Cases
- TC_001
- TC_002
- TC_003
- TC_004

### Negative Test Cases
- TC_005
- TC_006
- TC_007

### Boundary Value Test Case
- TC_008
