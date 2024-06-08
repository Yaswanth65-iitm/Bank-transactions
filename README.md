# Bank Transaction Simulator

This project implements a simple bank transaction simulator using C++ and object-oriented programming principles. The simulator allows management and processing of bank accounts and transactions through various operations, including deposits, withdrawals, and balance inquiries.

## Table of Contents
- [Bank Transaction Simulator](#bank-transaction-simulator)
  - [Table of Contents](#table-of-contents)
  - [Files](#files)
  - [Compilation](#compilation)
  - [Execution](#execution)
  - [Program Description](#program-description)
  - [Commands and Operations](#commands-and-operations)
    - [1. Execute Next X Transactions (`F X`):](#1-execute-next-x-transactions-f-x)
    - [2. Revert Y Transactions (`R Y`):](#2-revert-y-transactions-r-y)
    - [3. Add Transaction T After Kth Transaction (`I T K`):](#3-add-transaction-t-after-kth-transaction-i-t-k)
    - [4. Remove Up to M Transactions for Account A (`D A M`):](#4-remove-up-to-m-transactions-for-account-a-d-a-m)
    - [5. Execute All Remaining Transactions (`C`):](#5-execute-all-remaining-transactions-c)
    - [6. Display Transactions for Account Y (`S Y`):](#6-display-transactions-for-account-y-s-y)
    - [7. Count Accounts with Balance ≥ X (`G X`):](#7-count-accounts-with-balance--x-g-x)
    - [8. Display Accounts with Highest Balance (`M`):](#8-display-accounts-with-highest-balance-m)
    - [9. Show Balance for Account X (`V X`):](#9-show-balance-for-account-x-v-x)
  - [Input Structure](#input-structure)
  - [Constraints](#constraints)
  - [Expected Output](#expected-output)

## Files

- `main.cpp`: The main driver file that handles input, processes commands, and interacts with bank accounts and transactions.
- `bank_acc.h`: Defines the `BankAccount` class, which manages account balances and stores transaction history.
- `transactions.h`: Defines the `Transaction` class, which holds information about individual transactions.

## Compilation

To compile the source files, use the following command:
```bash
g++ -o bank_system.out main.cpp bank_acc.cpp transactions.cpp
