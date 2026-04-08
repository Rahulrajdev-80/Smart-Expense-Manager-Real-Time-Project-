# Smart Expense Manager (Real-Time Project)

## Project Objective

The Smart Expense Manager is a Python-based application designed to track, manage, and analyze daily expenses.
It helps users understand their spending patterns and provides insights for better financial decision-making.

---

## Features

### User Management

* Add new users
* View available users

### Expense Tracking

* Add daily expenses
* Categorize spending (Food, Travel, Shopping, etc.)
* Store description and date

### Expense Analysis

* View all expenses using SQL JOIN
* Filter expenses by category and date
* Calculate total expenses using `map()` and `reduce()`
* Category-wise spending summary using dictionary comprehension
* Generate monthly expense reports

### Smart Insights

* Detect highest spending category
* Provide spending alerts
  (e.g., “You are spending too much on Food”)

### Additional Features

* Input validation to prevent runtime errors
* Clean and structured output formatting
* Dynamic user selection (dropdown in web version)

---

## Technologies Used

* Python
* MySQL
* Flask (for web application)
* Visual Studio Code

---

## Concepts Used

### Object-Oriented Programming (OOP)

* Encapsulation
* Inheritance
* Method Overriding
* Abstraction (Abstract Class)

### Functional Programming

* `map()`
* `filter()`
* `reduce()`
* List Comprehension
* Dictionary Comprehension

### Database Concepts

* SQL Queries
* JOIN operations
* Foreign Key relationships

---

## Project Structure

```
expense_manager/
│
├── db_config.py
├── main.py
├── app.py
│
├── models/
│   ├── user.py
│   ├── expense.py
│
├── utils/
│   ├── display.py
│   ├── validator.py
│
├── templates/
│   ├── index.html
│   ├── view.html
│
└── README.md
```

---

## Setup Instructions

### 1. Clone Repository

```
git clone <your-repo-link>
cd expense_manager
```

### 2. Install Dependencies

```
pip install flask
pip install mysql-connector-python
```

### 3. Setup Database (MySQL)

```
CREATE DATABASE expense_db;
USE expense_db;

CREATE TABLE users (
    user_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50)
);

CREATE TABLE expenses (
    exp_id INT PRIMARY KEY AUTO_INCREMENT,
    user_id INT,
    amount FLOAT,
    category VARCHAR(50),
    description VARCHAR(100),
    date DATE,
    FOREIGN KEY (user_id) REFERENCES users(user_id)
);
```

### 4. Update Database Credentials

Edit `db_config.py`:

```
password = "your_password"
```

---

## How to Run

### Run CLI Version

```
python main.py
```

### Run Web Version (Flask)

```
python app.py
```

Open in browser:

```
http://127.0.0.1:5000
```

---

## Sample Output

* Add users and expenses
* View categorized expense records
* Calculate total expenses
* Generate smart insights on spending patterns

---

## Future Enhancements

* Graphical visualization using Matplotlib
* User authentication system
* Budget tracking and alerts
* Responsive web interface

---

## Conclusion

This project demonstrates the application of Python, SQL, and Flask in building a real-world expense management system.
It integrates data storage, processing, and analysis to provide meaningful financial insights.
