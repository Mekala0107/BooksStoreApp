# 📚 Bookstore Management System

A Java Swing desktop application that allows customers to place book orders and administrators to manage them effectively. This system features a user-friendly interface and a robust MySQL database backend, making it ideal for learning full-stack desktop application development.

---

## 🚀 Features

### 👥 Customer Panel

- 🧾 View Available Books  
  Easily browse the book list fetched from the database.

- 🛍️ Place Orders  
  Enter your name, address, and select a book to place an order.

- 🔄 Update Orders  
  Modify existing orders by updating personal or order details.

### 🛠️ Admin Panel

- 📋 Manage Orders  
  View all customer orders in a sortable, editable table.

- 📅 Update Delivery Dates  
  Use a date picker (JDateChooser) to assign delivery dates to orders.

---

## 💻 Technologies Used

| Technology     | Purpose                                       |
|----------------|-----------------------------------------------|
| Java           | Core application logic                        |
| Java Swing     | Graphical User Interface                      |
| MySQL          | Backend relational database                   |
| JDBC           | Java Database Connectivity                    |
| JDateChooser   | Swing-based date picker for Java              |

---

## 🖼️ User Interface

- Developed with Java Swing for a responsive, desktop-based experience.
- Includes clear navigation between Customer and Admin panels.
- Admin interface uses a table view for easy data handling.
- Date picker integrated for easy delivery scheduling.

---

## 📂 Project Structure

BookStoreApp/
├── src/
│ └── com/
│ └── company/
│ ├── Main.java # Entry point
│ ├── BookStore.java # Base UI layout
│ ├── Admin.java # Admin functionalities
│ └── Customer.java # Customer functionalities
├── README.md # Project documentation
├── .gitignore # Git ignore rules
└── BookStoreApp.iml # IntelliJ IDEA project file

---

## 🛠️ Setup Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/BookStoreApp.git
cd BookStoreApp
```

2️⃣ Open in IDE
Use IntelliJ IDEA or another Java IDE of your choice. Import the project as a Maven or Java project.

3️⃣ Configure the MySQL Database
Start your MySQL server.

Create a database named intern.

Create the necessary tables:

```sql
CREATE TABLE booksPresent (
  BOOK_NAME VARCHAR(255),
  PRICE DECIMAL(10,2)
);

CREATE TABLE purchasedBooks (
  NAME VARCHAR(255),
  ADDRESS VARCHAR(255),
  BOOK_NAME VARCHAR(255),
  PRICE DECIMAL(10,2),
  DELIVERY_DATE DATE
);
```

4️⃣ Update Your Database Credentials
In both Admin.java and Customer.java, update the MySQL connection line:

```java
Connection connection = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/intern", "root", "your_password");
```

Replace "your_password" with your actual MySQL root password.

5️⃣ Run the Application
Run Main.java from your IDE to launch the application.

👨‍💻 Usage Guide
🧑‍💼 For Customers:
Click the "CUSTOMER" button.

View available books.

Fill in your name, address, and select a book.

Click "ADD RECORD" to place an order.

To update, re-enter your name and click "UPDATE RECORD".

👩‍💼 For Admins:
Click the "ADMIN" button.

All customer orders will be displayed in a table.

Select a row, pick a new delivery date using the calendar.

Click "UPDATE RECORD" to apply changes.

🖼️ Screenshots


![image](https://github.com/user-attachments/assets/5b54f098-e9fb-49ba-8b5f-bf38c76c2df8)

![Customer Panel]!
![image](https://github.com/user-attachments/assets/ce7c8018-c123-4512-a585-ad56a93c587b)

![Admin Panel]!
![image](https://github.com/user-attachments/assets/3290e495-ad5c-4660-98c0-33e9b6446cff)

❗ Troubleshooting
❌ Can't connect to MySQL:

Ensure your MySQL server is running.

Verify root credentials and DB/table names.

⚠️ Date Picker not working:

Confirm jcalendar-1.4.jar is added correctly to classpath.






