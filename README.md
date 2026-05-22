# PL/SQL Automated Sales Commission Engine

An enterprise-grade database automation solution and backend engine built using **Oracle PL/SQL**. The system automatically generates IDs using dynamic triggers and sequences, handles large transaction data using PL/SQL cursors, and processes multi-tier sales commissions dynamically based on customizable metadata rules.

---

## 🏗️ Database Architecture & Schema

The system consists of 4 relational tables structured as follows:

1. **`EMP_EMPLOYEES`**: Stores employee master data (Names, Emails, and Base Salaries).
2. **`EMP_SALES`**: Tracks daily sales transactions linked to the employees.
3. **`EMP_COMM_RULES`**: Contains metadata config for tiered rewards (Min/Max sales limits and percentages).
4. **`EMP_CALCULATED_COMMISSIONS`**: The ultimate audit table storing computed monthly payouts.

---

## ⚡ Core Features & Automation

* **Dynamic ID Generation**: Uses a powerful script that scans database dictionary views (`ALL_OBJECTS`, `all_cons_columns`) to dynamically build sequences and `BEFORE INSERT` triggers for all primary keys.
* **Cursor-Based Processing**: Employs efficient explicit PL/SQL cursors to process row-by-row aggregation without overloading the server memory.
* **Robust Exception Handling**: Handles edge cases seamlessly (e.g., zero sales or numbers falling outside rule boundaries).

---

## 🚀 How to Deploy & Test

Execute the script files in your Oracle SQL Developer in the following sequential order:

1. Run **`1_database_schema.sql`** to create the structural tables.
2. Run **`2_automation_script.sql`** to activate the automated sequences and triggers.
3. Insert testing records via **`3_test_data.sql`**.
4. Compile the stored procedure inside **`4_commission_engine.sql`** and run it using:
   ```sql
   EXEC CALCULATE_SALES_COMMISSIONS;

## 👤 Author

**Mahmooood**
Data & Analytics Engineer
PL/SQL| Oracle Sql Developer
GitHub: [MahmoooOod](https://github.com/MahmoooOod)

---

## ✅ Project Status

🎉 **Project Fully Completed & Delivered**


  
