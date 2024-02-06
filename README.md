## Banking System
This project introduces a Java-based banking system, employing Object-Oriented Programming (OOP) principles. 

## Overview

This project implements a simple banking system with two classes: Account and SavingsAccount. The Account class serves as the superclass, while the SavingsAccount class is a subclass of Account. The classes demonstrate encapsulation, polymorphism, and proper use of superclass-subclass relationships.

## Table of Contents

- [1. Account Class in Banking System](#AccountClassinBankingSystem)
- [2. SavingAccount Class in Banking](#SavingAccountClassinBanking)
- [3. Banking System](#BankingSystem)
- [4. User Interface](#UserInterface)
- [5. View Account Interface](#ViewAccountInterface)
## 1. Account Class in Banking System

- **Account class (superclass):**
The Account class manages standard bank accounts, including deposits, withdrawals, and information retrieval. It's a flexible base for general-purpose accounts and a superclass for the specialized SavingsAccount class, handling interest rates and penalties.

  - Fields:
    - accountNumber: String
    - accountHolder: String
    - balance: double

  - Constructors:
    - `Account(accountNumber: String, accountHolder: String, balance: double)`

  - Methods:
    - `getAccountNumber(): String`:Unique identifier for each account.
    - `getAccountHolder(): String`: Name of the account holder.
    - `getBalance(): double`: Current balance in the account.
    - `deposit(amount: double): void`: Deposits the specified amount into the account.
    - `withdraw(amount: double): void`: Withdraws the specified amount from the account. If the withdrawal exceeds the account balance, a penalty is applied.
## 2. SavingAccount Class in Banking

- **SavingAccount (subclass):**
  - Fields:
    - Inherits from the "Account" class.
    - Additional Fields:
    - interestRate: double

  - Constructors:
    - `SavingAccount(accountNumber: String, accountHolder: String, balance: double, interestRate: double)`

  - Methods:
    - `getInterestRate(): double`: Interest rate for the savings account.
    - `setInterestRate(interestRate: double): void`
    - `withdraw(amount: double): void` (Overridden to include penalty)
    - `calculateInterest(): void`: Calculates and adds interest to the account balance based on the interest rate.

## 3. Banking System
### Inheritance
### Encapsulation
### Polymorphism
### Class diagram
### User case diagram

- Demonstrates encapsulation by encapsulating fields within classes.
- Achieves polymorphism through the overridden `withdraw` method in the "SavingAccount" class.
- Establishes a proper superclass-subclass relationship with "SavingAccount" inheriting from the "Account" class.
  
## 4. User Interface
- **1. CreateAccount:**

When the user selects "CreateAccount" (option 1), the system prompts the user to input `AccountNumber`, `AccountHolder` and `PIN`(digits only). The user information is stored in a text file named `Userinfo.txt` 
- Example:
- 00410053/Munny/123
- Account created successfully.

- **2. Account**

When the user selects "Account" (option 2), the system prompts the user to input `AccountNumber`, `AccountHolder` and `PIN`(digits only).The system checks if the user input matches the information in `Userinfo.txt`

- If the information is incorrect:
 - `Account not found. Please create an account.`
- The system then gives the option to create an account (option 1).
- If the information is correct:
 - The system proceeds to the `viewAccount`viewAccount interface.

## 5. View Account Interface
- **a. Setbalance**
- **b. DepositMoney**
- **c. WithdrawMoney**
- **d. SavingAccount**


- Setbalance
    The user can set their balance, for example, balance: 1000$. The system displays the updated balance.

- DepositMoney
    The user can deposit money, for example, DepositMoney: 300$. The system displays the updated balance.

- WithdrawMoney
    The user can withdraw money, for example, WithdrawMoney: 200$. The system displays the updated balance.

- SavingAccount
        Set InterestRate
        The user can set the interest rate, for example, Interest Rate: 0.53$. The system calculates and adds interest to the balance using the calculateInterest method.
        Check Balance
        The system displays the updated balance after adding interest.
-updated
    AccountNumber: 00310053
    AccountHolder: Munny
    Balance: 1100.54$

After this, the system closes.






