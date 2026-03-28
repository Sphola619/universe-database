# 🌌 Universe Database Project (PostgreSQL)

## 📖 Overview

This project is a simple relational database built using **PostgreSQL** as part of a FreeCodeCamp database exercise. The goal was to model celestial bodies—such as galaxies, stars, planets, and moons—using structured tables, primary keys, and (conceptually) foreign key relationships.

Although the current schema focuses on table creation and primary keys, it lays the groundwork for a fully relational universe database where entities can be linked together (e.g., planets belonging to stars, moons orbiting planets).

---

## 🛠️ Technologies Used

* PostgreSQL (v12.22)
* SQL (DDL – Data Definition Language)

---

## 🗂️ Database Structure

The database is named:

```
universe
```

It contains four main tables:

### 1. Galaxy Table

Stores information about galaxies.

| Column | Type         | Description        |
| ------ | ------------ | ------------------ |
| id     | integer      | Primary key        |
| name   | varchar(100) | Name of the galaxy |

---

### 2. Star Table

Stores stars that exist within galaxies.

| Column | Type         | Description      |
| ------ | ------------ | ---------------- |
| id     | integer      | Primary key      |
| name   | varchar(100) | Name of the star |

---

### 3. Planet Table

Stores planets that orbit stars.

| Column | Type         | Description        |
| ------ | ------------ | ------------------ |
| id     | integer      | Primary key        |
| name   | varchar(100) | Name of the planet |

---

### 4. Moon Table

Stores moons that orbit planets.

| Column | Type         | Description      |
| ------ | ------------ | ---------------- |
| id     | integer      | Primary key      |
| name   | varchar(100) | Name of the moon |

---

## 🔑 Key Features

* **Primary Keys**

  * Each table uses an `id` column as its primary key to uniquely identify records.

* **Scalable Design**

  * The schema is structured to allow future relationships via foreign keys (e.g., linking planets to stars).

* **Clean Initialization**

  * Includes a full database setup:

    * Drops existing database (if exists)
    * Creates a fresh database
    * Defines tables and constraints

---

## 🚀 How to Run

1. Make sure PostgreSQL is installed and running.
2. Open your terminal or psql shell.
3. Run the SQL dump file:

```bash
psql -U your_username -f universe.sql
```

4. Connect to the database:

```sql
\connect universe
```

---

## 📌 Future Improvements

* Add **foreign key relationships**:

  * `star → galaxy`
  * `planet → star`
  * `moon → planet`

* Insert real or sample astronomical data

* Add additional attributes:

  * Mass, size, distance, composition, etc.

* Create queries to explore relationships:

  * Example: “List all planets in a specific galaxy”

---

## 🎯 Learning Outcomes

Through this project, I learned:

* How to create and manage databases in PostgreSQL
* How to define tables using SQL
* How to use **primary keys** for unique identification
* The importance of **relational structure** in database design
* How database schemas can scale with added relationships

---

## 📬 Notes

This project is part of my journey into full-stack development and database design. It reflects foundational knowledge that can be expanded into more complex systems.

---

⭐ *Built as part of FreeCodeCamp's PostgreSQL curriculum*
