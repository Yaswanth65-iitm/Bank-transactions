## Execution

1. **Compile the Code:**
   - Compile the source code files using a C++ compiler. For example:
     ```bash
     g++ -o bank_system.out .\main.cpp .\bank_acc.cpp .\transactions.cpp
     ```
2. **Run:**
    - Run the executable or .out file generated after compilation. For example:
    ```
    .\bank_system.out < sample_input.txt
    ```

## Program Description

The program will read the following commands from input and process them as described below:

1. **Process Next X Transactions (F X):**
   - Process the next X transactions after the cursor.
   - If fewer than X transactions remain, the cursor stops at the last transaction.
2. **Undo Y Transactions (R Y):**
   - Reverts Y transactions starting from the cursor.
   - If fewer than Y transactions are available, the cursor stops at the first transaction.

3. **Insert Transaction T After Kth Transaction (I T K):**
   - Inserts a new transaction T after the Kth transaction.
   - Only valid if K is within the transaction list bounds.
   - If K is before the cursor, the new transaction is processed.
   - The cursor position remains unchanged.

4. **Delete Up to M Number of Transactions of Account A (D A M):**
   - Deletes up to M transactions of account A relative to the cursor.
   - Deletes forward if M > 0 and backward if M < 0.
   - Updates the balance of account A accordingly.
   - The cursor position remains unchanged.

5. **Process All Transactions (C):**
   - Processes all transactions from the cursor onward.

6. **Print Processed Transactions of Account Number Y (S Y):**
   - Prints all processed transactions of account Y up to the cursor.
   - No output for invalid account numbers.

7. **Print Count of Accounts with Balance Greater than or Equal to X (G X):**
   - Prints the count of accounts with balances ≥ X, relative to the cursor.

8. **Print Account Number(s) with Highest Balance (M):**
   - Prints the account number(s) with the highest balance.
   - If multiple accounts have the highest balance, prints them all on one line, sorted in ascending order.
9. **Print Balance of Account Number X (V X):**
   - Prints the balance of account X, relative to the cursor.

### Input
The inputs are:
- The first line specifies the number of accounts to be maintained, denoted as C.
- The second line contains C space-separated unsigned integers - each integer denotes an account number.
- The next line specifies the number of transactions to be maintained, denoted as N.
- The next set of N lines: each line denotes either a deposit or withdrawal transaction. (in the format {account_number} {W/D} {amount})
- Inserts only the transactions of valid account numbers to the list, in the same order as in the input file. Invalid account numbers will be ignored.
- Each following line contains a processing directive (as listed above).
- The last line contains only the word END.

### Constraints
- Deposit and Withdrawal amounts will be non-negative integers less than or equal to 50000.

### Output
This will be the output of each query as applicable.
