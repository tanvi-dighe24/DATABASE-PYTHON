✅Connecting to a database in Python typically follows a standardized workflow defined by the Python Database API Specification (PEP 249). The process involves installing a database-specific driver, establishing a connection, and using a cursor to execute SQL commands. 

1. General Connection Workflow:-
Regardless of the database type, the sequence of operations is generally the same:
Import the database-specific module.
Connect using a connect() function with credentials (host, user, password, database).
Create a Cursor object to execute queries.
Execute SQL and fetch results using fetchall() or fetchone().
Commit changes (for INSERT/UPDATE/DELETE) and Close the connection to free resources


2. Connection Examples by Database Type
SQLite (Built-in)
SQLite is the easiest to use because it requires no separate server and is built into the Python standard library. 
Module: sqlite3

-code:
import sqlite3
# Connects to a file-based database
conn = sqlite3.connect('example.db')
cursor = conn.cursor()
cursor.execute("SELECT * FROM users")
print(cursor.fetchall())
conn.close()
