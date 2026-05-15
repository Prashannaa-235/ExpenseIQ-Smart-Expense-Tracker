# ExpenseIQ — Smart Expense Tracker

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Apache Tomcat](https://img.shields.io/badge/Apache_Tomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)

> A full-stack web application to track daily expenses, manage budgets, and visualize spending patterns through an interactive analytics dashboard.

---

## Features

- **Secure Authentication** — Register and login with session-based authentication
- **Expense Management** — Add, view, filter, and delete expenses in real time
- **Category Filtering** — Filter expenses by Food, Transport, Entertainment, Education, Utilities
- **Live Statistics** — Monthly total, transaction count, and top spending category
- **Analytics Dashboard** — Interactive Doughnut and Bar charts powered by Chart.js
- **Responsive UI** — Clean dark-themed modern interface built with CSS Grid

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, JavaScript, Chart.js |
| Backend | Java Servlets, JSP |
| Database | MySQL |
| Server | Apache Tomcat 9 |
| Build Tool | Apache Maven |
| IDE | IntelliJ IDEA |

---

## Project Structure

```
ExpenseTrackerMaven/
├── src/
│   └── main/
│       ├── java/com/expense/
│       │   ├── DBConnection.java       # MySQL connection helper
│       │   ├── LoginServlet.java       # Handles user login
│       │   ├── RegisterServlet.java    # Handles user registration
│       │   ├── ExpenseServlet.java     # Add / Delete expenses
│       │   └── LogoutServlet.java      # Session invalidation
│       └── webapp/
│           ├── index.html              # Login & Register page
│           ├── dashboard.jsp           # Main expense dashboard
│           ├── analytics.jsp           # Charts & analytics
│           └── WEB-INF/
│               └── web.xml             # Deployment descriptor
├── database/
│   └── expense_db.sql                  # Database schema + sample data
└── pom.xml                             # Maven dependencies
```

---

## Database Schema

```sql
users (id, name, email, password, created_at)
expenses (id, user_id, title, amount, category, expense_date, note, created_at)
```

---

## Getting Started

### Prerequisites
- Java JDK 11 or above
- Apache Tomcat 9
- MySQL Server
- Apache Maven
- IntelliJ IDEA (Community Edition)

### Setup

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/ExpenseTracker.git
cd ExpenseTracker
```

**2. Setup the database**

Open MySQL Workbench → run `database/expense_db.sql`

Or via CMD:
```bash
mysql -u root -p < database/expense_db.sql
```

**3. Update DB password**

Open `src/main/java/com/expense/DBConnection.java`:
```java
private static final String PASSWORD = "your_mysql_password";
```

**4. Load Maven dependencies**

In IntelliJ: click the 🔄 Maven reload icon on the right panel

**5. Configure Smart Tomcat plugin**
```
Run → Edit Configurations → Smart Tomcat
Deployment Directory: src/main/webapp
Context Path: /ExpenseTracker
Port: 8080
```

**6. Run the project**

Press `Shift + F10` or click ▶

**7. Open in browser**
```
http://localhost:8080/ExpenseTracker/
```

### Demo Login
```
Email:    test@gmail.com
Password: test123
```

---

## Screenshots

> Dashboard — Add expenses, filter by category, view live stats

> Analytics — Doughnut chart (by category) + Bar chart (monthly trend)

---

## Key Concepts Demonstrated

- **MVC Architecture** — Servlets as Controller, JSP as View, MySQL as Model
- **Session Management** — Secure login/logout using HttpSession
- **SQL Injection Prevention** — All queries use PreparedStatement
- **CRUD Operations** — Create, Read, Filter, Delete expenses
- **Data Visualization** — Chart.js integration for spending analytics
- **Responsive Design** — CSS Grid layout with dark theme

---

## Author

**Prashannaa**
- 3rd Year B.Tech — Information Technology
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [yourprofile](https://linkedin.com/in/yourprofile)

---

## License

This project is open source and available under the [MIT License](LICENSE).
