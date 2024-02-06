## Banking System
This project introduces a Java-based banking system, employing Object-Oriented Programming (OOP) principles. 

## Overview

This project implements a simple banking system with two classes: Account and SavingsAccount. The Account class serves as the superclass, while the SavingsAccount class is a subclass of Account. The classes demonstrate encapsulation, polymorphism, and proper use of superclass-subclass relationships.

## Table of Contents

- [1. Class in Banking System](#AccountClassinBankingsystem)
- [2. User Interface](#UserInterface)
- [3. View Account Interface](#ViewAccountInterface)
- [4. Saving Account](#SavingAccount)
  
## 1. Classes in Banking System
### 1. Account Class in Banking System

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
### 2. SavingAccount Class in Banking

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

### 3. Banking System

**Class diagram:**
![image](https://github.com/MunnyRochom2023/BankingSystem/assets/151621221/584140b6-a646-448f-83f2-53d840432647)

**User case diagram:**
![image](https://github.com/MunnyRochom2023/BankingSystem/assets/151621221/d324d227-8e3c-43cb-9cc0-99c09874ece7)

 **Inheritance:** 
    - Account Class (superclass):
        - The SavingAccount class is a subclass of the Account class.
        - SavingAccount inherits the fields (accountNumber, accountHolder, balance) and methods (getAccountNumber, getAccountHolder, getBalance, deposit, withdraw) from the Account class.
**Encapsulation:**
    - Account Class (superclass):
        - The fields (accountNumber, accountHolder, balance) are declared as private, encapsulating the internal state of the class.
       -  Access to these fields is provided through public getter methods (getAccountNumber, getAccountHolder, getBalance).
        - The deposit and withdraw methods encapsulate the logic for updating the balance, ensuring that the internal state is modified in a controlled manner.
    - SavingAccount Class (subclass):
        - The SavingAccount class encapsulates additional functionality related to savings accounts, such as interest rates.
        - The interestRate field is encapsulated within the class, and access is provided through getter and setter methods (getInterestRate, setInterestRate).
**Polymorphism:**
    - Account Class (superclass):
        - Polymorphism is evident in the withdraw method, which is overridden in the SavingAccount subclass. The SavingAccount version of the method includes penalty logic in addition to the standard withdrawal functionality.
    - SavingAccount Class (subclass):
        - The withdraw method is overridden in the SavingAccount class, demonstrating polymorphism by providing a specialized implementation of the method in the subclass.
        
## 2. User Interface
### 1. CreateAccount
- When the user selects "CreateAccount" (option 1), the system prompts the user to input `AccountNumber`, `AccountHolder` and `PIN`(digits only). The user information is stored in a text file named `Userinfo.txt` 
- Example:
- 00410053/Munny/123
  
  ### 2. Account
When the user selects "Account" (option 2), the system prompts the user to input `AccountNumber`, `AccountHolder` and `PIN`(digits only).The system checks if the user input matches the information in `Userinfo.txt`

- If the information is incorrect:
 - `Account not found. Please create an account.`
- The system then gives the option to create an account (option 1).
- If the information is correct:
 - The system proceeds to the `viewAccount` viewAccount interface.

## 3. View Account Interface

### a. Setbalance
**Setbalance**
The user can set their balance.
      - for example, balance: 1000$. The system displays the updated balance.
### b. DepositMoney
**DepositMoney**
    The user can deposit money.
      - for example, DepositMoney: 300$. The system displays the updated balance.
### c. WithdrawMoney
**WithdrawMoney**
    The user can withdraw money.
      - for example, WithdrawMoney: 200$. The system displays the updated balance.
      
## 4. Saving Account 
### SavingAccount

**Set InterestRate**
    The user can set the interest rate.
        - for example, Interest Rate: 0.53$. The system calculates and adds interest to the balance using the calculateInterest method.
    Check Balance
        - The system displays the updated balance after adding interest.
**updated** 
    AccountNumber: 00310053
    AccountHolder: Munny
    Balance: 1100.54$

**the system closes.**







