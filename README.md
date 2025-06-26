# 🎓 College Event Management System

This project is a Database Management System (DBMS) designed to manage and streamline the organization of college-level events. It handles student registrations, event planning, team participation, venue allocation, and results declaration.

---

## 🗂️ Database Overview

The system consists of **7 interrelated tables**:

1. **Student**
2. **Organizer**
3. **Venue**
4. **Event**
5. **Team**
6. **Participation**
7. **Result**

---

## 🛠️ Technologies Used

- **Database**: MySQL
- **Schema Design Tool**: [dbdiagram.io](https://dbdiagram.io)
- **Language**: SQL

---

## 🧩 Table Structure

### `Student`
| Column      | Type         | Description            |
|-------------|--------------|------------------------|
| student_id  | INT (PK)     | Unique student ID      |
| name        | VARCHAR(100) | Student name           |
| email       | VARCHAR(100) | Student email (unique) |
| dept        | VARCHAR(50)  | Department name        |
| year        | INT          | Year of study          |

### `Organizer`
| Column       | Type         | Description             |
|--------------|--------------|-------------------------|
| organizer_id | INT (PK)     | Unique organizer ID     |
| name         | VARCHAR(100) | Organizer name          |
| contact      | VARCHAR(15)  | Contact number          |
| department   | VARCHAR(50)  | Department              |

### `Venue`
| Column     | Type         | Description       |
|------------|--------------|-------------------|
| venue_id   | INT (PK)     | Venue ID          |
| venue_name | VARCHAR(100) | Name of venue     |
| location   | VARCHAR(100) | Venue location    |
| capacity   | INT          | Maximum capacity  |

### `Event`
| Column       | Type         | Description                |
|--------------|--------------|----------------------------|
| event_id     | INT (PK)     | Unique event ID            |
| event_name   | VARCHAR(100) | Name of the event          |
| event_type   | VARCHAR(50)  | Type (Technical/Cultural)  |
| date         | DATE         | Date of event              |
| venue_id     | INT (FK)     | Refers to Venue            |
| organizer_id | INT (FK)     | Refers to Organizer        |

### `Team`
| Column     | Type         | Description                |
|------------|--------------|----------------------------|
| team_id    | INT (PK)     | Unique team ID             |
| team_name  | VARCHAR(100) | Name of the team           |
| leader_id  | INT (FK)     | Refers to student leader   |

### `Participation`
| Column         | Type         | Description              |
|----------------|--------------|--------------------------|
| participation_id | INT (PK)   | Participation ID         |
| team_id        | INT (FK)     | Refers to Team           |
| event_id       | INT (FK)     | Refers to Event          |
| status         | VARCHAR(50)  | Registration status      |

### `Result`
| Column     | Type         | Description              |
|------------|--------------|--------------------------|
| result_id  | INT (PK)     | Result ID                |
| event_id   | INT (FK)     | Refers to Event          |
| team_id    | INT (FK)     | Refers to Team           |
| position   | VARCHAR(10)  | e.g., "1st", "2nd"       |

---

## 🔗 ER Diagram

You can visualize the schema using **dbdiagram.io**:
- Paste this code: [Click to view DBML code](#)

---

## ✅ Features

- Student registration and team formation  
- Event creation and venue assignment  
- Organizer management  
- Participation tracking and result declaration  
- Simple and scalable schema  

---

## 🚀 How to Run
Open MySQL Workbench or any SQL IDE.

Copy and paste the above SQL schema.

Execute to create the database CollegeEventDB and all 7 related tables.

----

## 📦 Author

Devu S

Intern - SQL Developer


