# Expense_Splitter
Java console app for splitting group expenses with MySQL. Add users, log shared expenses, and view net settlements—only the minimum required payment between users is shown. Demonstrates OOP, JDBC, and optimized debt netting.
## Features
- **Add Users:** Register group members for expense tracking.
- **Log Expenses:** Record who paid and who participated.
- **Optimized Settlements:** Nets out mutual debts so only the minimum required payments are shown.
- **Persistent Storage:** All data stored in MySQL.
- **Interactive CLI:** User-friendly menu for all actions.
## How It Works
- Each expense is split equally among selected participants.
- The app calculates all debts, then nets out mutual debts between users to minimize the number of transactions.
- All data is persisted in MySQL, demonstrating real-world backend integration.
## Setup Instructions
1. **Clone the repository:**
2. **Set up the MySQL database:**
- Create a database named `expensesplitter`.
- Run the following SQL to set up tables:
  ```
  CREATE TABLE users (
    id VARCHAR(36) PRIMARY KEY,
    name VARCHAR(50)
  );
  CREATE TABLE expenses (
    id VARCHAR(36) PRIMARY KEY,
    amount DECIMAL(10,2),
    paid_by VARCHAR(36)
  );
  ```
3. **Update database credentials:**
- In `ExpenseSplitterApp.java`, set your MySQL username and password.
4. **Run the application:**
- Open the project in IntelliJ IDEA or your preferred Java IDE.
- Run `ExpenseSplitterApp.java`.
- Use the menu to add users, expenses, and view settlements.
## Why This Project?
This project showcases:
- Java OOP and clean code practices
- Real-world problem solving for group payments
- Database design and JDBC integration
- Debt netting/optimization algorithms
- CLI user experience
