📘 Mini Library Management System
📖 Overview

The Mini Library Management System is a simple Python-based program that manages books, members, and borrowing activities in a small library setup. It’s designed mainly for demonstration and educational purposes — to show how core operations like adding, updating, deleting, borrowing, and returning books can work together in a clean, modular program.

This system works entirely in memory (no external database required), making it lightweight and perfect for classroom learning or quick prototypes.

🧩 System Components
1. operations.py

This is the core logic layer of the system.
It handles:

Adding, updating, and deleting books and members.

Borrowing and returning books.

Searching books by title or author.

Storing user accounts and login authentication.

Tracking borrowing history.

It defines all the main functions such as:

add_book(), update_book(), delete_book()
add_member(), update_member(), delete_member()
borrow_book(), return_book()
search_books(), verify_login()


It also contains global variables for:

Book records

Member data

Borrow history

Login credentials

and constants like:

BORROW_LIMIT = 3
BORROW_DAYS = 7

2. Demo.py

This file acts as the interactive command-line interface (CLI) for the system.

It allows users to log in as:

Admin

Staff

Student

Each role has different privileges:

Admin: Full control over books and members.

Staff: Can borrow or return books for themselves.

Student: Can borrow, return, and view their own history.

It provides clear menu options, input validation, and friendly feedback messages (including emojis and alerts like ✅ or ❌).

3. tests.py

This is a basic testing script using simple Python assert statements.
It checks that the main features in operations.py work as expected, such as:

Adding and rejecting duplicate books.

Borrowing and returning books correctly.

Preventing invalid deletions.

Searching books by title or author.

When tests run successfully, it prints:

Basic tests passed. If you see this message, tests ran without immediate assertion failures.

⚙️ How to Run the Program
Requirements

Python 3.8 or higher

Steps

Open your terminal or command prompt.

Navigate to the folder containing the project files.

Run the demo interface:

python Demo.py


Run the test script:

python tests.py

🧠 System Logic Summary

Every member can borrow up to 3 books for 7 days.

Books cannot be deleted while borrowed.

Members cannot be deleted if they have borrowed books.

All borrowing activity is stored in a global list (borrow_history).

Roles are verified through the verify_login() function before access is granted.

🌟 Key Features

✅ Add, update, delete, search books
✅ Manage members and user authentication
✅ Borrow and return with due date tracking
✅ Role-based permissions (Admin / Staff / Student)
✅ Assertion-based testing for reliability
✅ Fully modular and easy to upgrade

🔮 Future Improvements

If expanded, the system could include:

A database connection (e.g., SQLite, MySQL)

A web interface using Flask or Django

Email reminders for overdue books

Reporting and analytics dashboard

👩🏽‍💻 Author Notes

This project is a clean, beginner-friendly example of Python’s capabilities for structuring logic, handling roles, and ensuring data integrity — all without relying on heavy external tools.
