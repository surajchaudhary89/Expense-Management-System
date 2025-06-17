# 💰 Expense Management System

A complete end-to-end **Expense Management System** built using **Python, FastAPI, MySQL, and Streamlit**, with robust **logging**, and **unit testing** using `pytest`.  
It allows users to add, view, delete expenses, manage categories, and analyze spending habits visually.

---

## 📌 Features

- 📂 **Add/View Expense Categories**
- 💸 **Add New Expenses** with category, date, description
- 🪟 **View All Expenses** in a clean table format
- 🛠️ **Delete Expenses** after filtering by date
- 📊 **Analytics** with category-wise summaries using bar and pie charts
- 🧪 **Unit Testing** for backend modules with `pytest`
- 🧾 **Logging** using Python’s logging module for better traceability

---

## 🧱 Tech Stack

| Layer          | Tech Used          |
|----------------|--------------------|
| Backend        | FastAPI + MySQL    |
| Frontend       | Streamlit          |
| Logging        | Python `logging`   |
| Testing        | Pytest             |
| Visualization  | Matplotlib, Pyplot |

---

## 📁 Project Structure

expense_management/                                        
├── backend/                                                
│ ├── api.py # FastAPI endpoints                               
│ └── database.py # All DB queries and connections            
├── frontend/                                                 
│ └── streamlit_app.py # Streamlit UI                                   
├── log_utils/                                                          
│ └── logger.py # Custom logger config                                                   
├── tests/                                                              
│ ├── test_api.py # Unit tests for FastAPI                                     
│ └── test_database.py # Unit tests for DB functions                        
├── screenshots/                                                                                   
└── README.md                                                                              


---
## 🗃️ Database Setup
This project uses MySQL for data storage. To set up the database on your machine, follow these steps:

#### 🔧 Step 1: Create the Database

Open your MySQL terminal or Workbench and create a new database:
```commandline
CREATE DATABASE expense_db;
```
#### 💾 Step 2: Import the SQL Dump

The SQL dump file expense_db_dump.sql contains all the table structures and sample data. You can find it in the database_dump/ folder.
```commandline
mysql -u your_username -p expense_db < database_dump/expense_db_dump.sql
# Replace your_username with your MySQL username. You will be prompted for your password.
```

---

### 🖥️ Using MySQL Workbench:
- Go to Server > Data Import.

- Select Import from Self-Contained File.

- Choose expense_db_dump.sql.

- Select your target schema (e.g., expense_db) or create one.

- Click Start Import.

### 📝 Database Structure

The dump will automatically create and populate the following tables:

- categories – Stores expense categories (e.g., Food, Travel)

- expenses – Stores individual expense entries linked to a category

### 📦 File Location in Repo

```commandline
expense_management/
└── database_dump/
    └── expense_db_dump.sql
```

### 📣 Notes
- If you're running this on a fresh system, ensure MySQL server is installed and running.

- Your backend will connect to the expense_db by default. Update connection details in backend/database.py if needed.


---

## 🚀 How to Run the Project

### 1. ✅ Clone the Repository

```
git clone https://github.com/yourusername/expense-management-system.git
cd expense-management-system
```

### 2. ✅ Create a Virtual Environment

```python -m venv venv
# Activate it:
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate
```

### 3. ✅ Install Requirements

```
pip install -r requirements.txt
```

### 4. ✅ Start the Backend API

```
cd backend
uvicorn api:app --reload
```

### 5. ✅ Start the Frontend UI

```commandline
cd ../frontend
streamlit run streamlit_app.py

```
### 6. ✅ Run Tests

```commandline
pytest tests/

```
---
## 🧪 Unit Testing

#### Written with pytest

- Tests are separated for API and DB logic

#### Basic tests for:

- Adding categories and expenses

- Retrieving and deleting data

- Mocking is avoided to keep tests beginner-friendly and understandable
---
## 📄 Logging

- Centralized logger using log_utils/logger.py

- Logs info, warnings, and errors

- Useful during API errors, DB failures, etc.

- Logs can be directed to console or log files
---
## 📊 Screenshots

![Add Category](screenshots/add_category.png)
![Add Expense](screenshots/add_expense.png)
![View Expenses](screenshots/view_expenses.png)
![Delete Expenses](screenshots/delete_expense.png)
![Analytics](screenshots/analytics.png)

---

## 🌟 Key Highlights
- ✅ Intuitive and clean UI

- ✅ Full backend + frontend separation

- ✅ Tab-based navigation in Streamlit

- ✅ Clean and readable code

- ✅ Designed for beginners and intermediate Python learners

---
## 🚧 Future Improvements
- User Login / Authentication

- Export to Excel or PDF

- Monthly Budget Setting with Alerts

- Date Range Filtering in Analytics

- Recurring Expense Tracking
---
## 🙋‍♂️ Author

**Suraj Chaudhary**

([github link](https://github.com/surajchaudhary89/))

---

## 📜 License

This project is licensed under the MIT License.
