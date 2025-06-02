# 📚 Library Management System

A command-line based **Library Management System** built using **Python** and **MySQL**, designed to manage books, students, and book issuing/returning functionalities efficiently.

---

## 🚀 Features

- ✅ Add, View, Update, and Delete Books  
- 👨‍🎓 Add and View Student Records  
- 📖 Issue Books to Students (only if available)  
- 🔁 Return Issued Books (auto-update quantity)  
- 📋 View All Issued Book Records with Status  
- 🗃️ Structured Database Integration with MySQL  
- ❌ Input validation & error handling  

---

## 🛠️ Tech Stack

| Technology | Description |
|------------|-------------|
| 💻 Python  | Core programming language |
| 🐬 MySQL   | Relational Database for storing books & students |
| 🧠 MySQL Connector | Python-MySQL communication |

---

## 🗃️ Database Structure

### `books` Table
| Field     | Type        |
|-----------|-------------|
| book_id   | INT (Primary Key) |
| title     | VARCHAR     |
| author    | VARCHAR     |
| quantity  | INT         |

### `students` Table
| Field       | Type        |
|-------------|-------------|
| student_id  | INT (Primary Key) |
| name        | VARCHAR     |
| course      | VARCHAR     |

### `issued_books` Table
| Field       | Type        |
|-------------|-------------|
| issue_id    | INT (Primary Key, Auto Increment) |
| student_id  | INT (Foreign Key) |
| book_id     | INT (Foreign Key) |
| issue_date  | DATE        |
| return_date | DATE / NULL |

---

## 🖥️ Setup Instructions

1. **Install MySQL Connector**  
   ```bash
   pip install mysql-connector-python

