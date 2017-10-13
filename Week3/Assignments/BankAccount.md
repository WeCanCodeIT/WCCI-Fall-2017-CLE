# Bank Account Project
## Due: Monday, October 16 at 9:30am
### - [Submission Link](https://docs.google.com/forms/d/e/1FAIpQLScUEvl_ZgH_OgBu0zbg_WIvB6zBSkkXh7wfxqjv4LwLdBDxLg/viewform)

## Overview
You will be designing a console application to manage a client’s bank account. For now, the application will have only one client that is hard-coded into the system. The client has one checking account and one savings account.

## Skills Required
- OOP
- Inheritance & Polymorphism

## Tasks
### Menu Items
- You must include a functional menu that includes the following choices for the user.
```
- [ ] View Client Information
- [ ] View Account Balance
  - [ ] Checking Account Balance
  - [ ] Savings Account Balance
- [ ] Deposit Funds
  - [ ] To Checking Account
  - [ ] To Savings Account
- [ ] Withdraw Funds
  - [ ] From Checking Account
  - [ ] From Savings Account
- [ ] Exit
```
- The menu should display the options as shown in the Details section below.
- In the menu, after a user selects either View Balance, Deposit, or Withdraw, the program should then give the option of selecting which account.

### Required Classes
- [ ] Client Class
  - [ ] 3 properties
  - [ ] 1 constructor
  - [ ] 1 method
  - [ ] Client information should be filled in here
- [ ] Accounts (ALL Accounts should include the following)
  - [ ] An account number
  - [ ] Balance
  - [ ] An account type (savings or checking)
  - [ ] A way to view the current balance
  - [ ] User must be able to deposit money into either account
  - [ ] User must be able to withdraw money from either account
  - [ ] Make sure to include the following Classes
    - [ ] Account Class (base)
    - [ ] Checking Account Class (derived)
      - [ ] 1 constructor
    - [ ] Savings Account Class (derived)
      - Note: Savings Account must include a minimum balance.  User cannot withdraw money if balance will drop below minimum.
      - [ ] 1 property
      - [ ] 1 constructor
- [ ] Program Class
    - [ ] Must instantiate one client object
    - [ ] Must instantiate one checking account object
    - [ ] Must instantiate one savings account object
    - [ ] All menu options listed above must have functionality behind them
    - [ ] Program should run until user selects 'Exit'
### Other Tasks
- [ ] After each transaction, the current balance should be displayed on the screen.
- [ ] Your program should include:
  - [ ] 1 abstract method (at least)
  - [ ] 1 virtual method (at least)
  - [ ] 1 override method (at least)


## Details
When a user launches the program the following menu should be displayed to the screen.
```
1. View Client Information
2. View Account Balance
3. Deposit Funds
4. Withdraw Funds
5. Exit
```

If the user wants to view account balance, deposit funds, or withdraw money, the user should be prompted to select which account.
```
1. View Client Information
2. View Account Balance
3. Deposit Funds
4. Withdraw Funds
5. Exit

2

a. Checking Account
b. Savings Account
```

Be sure the user can continue making selections from the menu until all desired transactions have been completed.

## Stretch Tasks
Right now this program is designed for one user. Giving the ability to enter a user name when the program begins would make the program useful for multiple users. At this point do not worry about trying to add passwords. That is outside of the scope of what we know at this point. Letting the users log in with only their names _is_ less secure, but we're focused on functionality right now.

Find a way for the Client object and the Account objects to interact!
Hint: Don't forget we can pass objects as parameters too. Think about passing a client object to the account classes in order to log in. Be creative!

## Hints
Persistence is not required. Meaning each time you run the program all of the values can reset.

You can choose any starting balance to begin the program.

Think about what data type should be used for dealing with money
