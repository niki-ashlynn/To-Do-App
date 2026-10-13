# To-Do-App
An Android-based To-Do List application developed using Java, XML, and SQLite, featuring task creation, editing, deletion, categorisation, completion tracking, and offline data storage.
# 📝 To-Do List | Android Application

**A simple, offline Android task management application built using Java, SQLite, and XML.**

## 📌 Project Overview

The To-Do List Android Application is a mobile productivity tool developed to help users organise, manage, and track their daily tasks efficiently.

Originally developed as part of the **COS211 – Development of Mobile Application** module at British United College / TMC Academy in 2025, the project focuses on implementing CRUD operations, local database management, and a user-friendly mobile interface.

The application features a minimal pastel-themed design with straightforward task management functionality, allowing users to manage their responsibilities without requiring an internet connection.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Java | Application logic and task management functionality |
| Android Studio | Development environment |
| SQLite | Local database for persistent task storage |
| XML | User interface layouts and styling |
| Android SDK | Android application development and UI components |

## ✨ Key Features

- **Task Creation:** Add new tasks and assign categories.
- **Task Management:** View, edit, and delete existing tasks.
- **Task Completion:** Mark tasks as completed using checkboxes.
- **Task Categorisation:** Organise tasks into categories.
- **Automatic Sorting:** Display pending tasks before completed tasks.
- **Offline Storage:** Save tasks locally using SQLite without requiring an internet connection.
- **Minimalist Interface:** Pastel colours, rounded elements, and a simple navigation flow.

## 🗄️ Database Design

The application uses SQLite to store task information locally on the Android device.

Database name: `tasks.db`

### Database Structure

| Column | Data Type | Description |
|---|---|---|
| task | TEXT (Primary Key) | Unique task name |
| status | INTEGER | Completion status (0 = Pending, 1 = Completed) |
| category | TEXT | Category assigned to the task |

The database is managed through `DBHelper.java`, which extends Android's `SQLiteOpenHelper` class.

### Database Operations

The application implements CRUD functionality:

- **CREATE:** Insert new tasks into the SQLite database.
- **READ:** Retrieve stored tasks and display them in the application.
- **UPDATE:** Modify task names, categories, and completion statuses.
- **DELETE:** Remove tasks from the database.

Tasks are retrieved using SQL sorting to prioritise incomplete tasks.

```sql
SELECT *
FROM tasks
ORDER BY status ASC, task COLLATE NOCASE ASC;
```

This query displays pending tasks first, followed by completed tasks, with alphabetical sorting within each group.

## 🏗️ Application Architecture

The application separates its functionality into several components.

### 1. MainActivity.java
Handles the main application logic, including navigation, user interactions, task creation, and retrieving data from the database.

### 2. DBHelper.java
Manages SQLite database creation and CRUD operations, including inserting, updating, retrieving, and deleting tasks.

### 3. XML Layout Files
Define the application's visual interface, including the welcome screen, task list, input fields, buttons, and custom backgrounds.

### 4. TaskAdapter
Connects task data to the ListView and supports displaying task information and completion statuses.

## 🧪 Testing and Validation

The application was tested using an Android emulator to verify its main functionality.

| Test Case | Expected Result |
|---|---|
| Add Task | New task is saved and displayed |
| Update Task | Edited task appears in the list |
| Delete Task | Task is removed from the database and interface |
| View Tasks | Saved tasks load after restarting the application |
| Complete Task | Task is marked as completed and moves to the bottom |

Testing demonstrated that the core task management features operated as expected in the emulator environment.

## 🎯 Project Objectives

The project was designed to:

1. Develop a functional Android application using Java.
2. Implement SQLite for persistent local data storage.
3. Apply CRUD operations to manage user-generated tasks.
4. Design a simple and accessible interface using XML.
5. Test the application's functionality through an Android emulator.

## 🚀 Future Improvements

Although the application implements its core features, several improvements could enhance usability and scalability:

- **Responsive UI:** Optimise layouts for tablets and different screen sizes.
- **Dark Mode:** Introduce theme customisation.
- **Input Validation:** Improve handling of empty and duplicate tasks.
- **Task Reminders:** Add notifications and scheduling functionality.
- **Progress Tracking:** Display task completion statistics.
- **Cloud Synchronisation:** Enable backups and access across multiple devices.
- **Security:** Explore authentication and additional local data protection.
- **Deployment:** Conduct real-device testing and prepare a signed APK.

## 💡 Skills Demonstrated

- Android Application Development
- Java Programming
- SQLite Database Management
- SQL and CRUD Operations
- XML Interface Design
- Data Persistence
- Debugging and Functional Testing
- User Interface Design
- Problem-Solving

## 📚 Project Background

**Project:** To-Do List Android Application  
**Year:** 2025  
**Module:** COS211 – Development of Mobile Application  
**Institution:** British United College / TMC Academy  
**Developer:** Thiri Myat Thwe

## 📖 Conclusion

This project provided practical experience in developing a database-driven Android application from design to testing.

By integrating Java application logic, SQLite database operations, and XML interface components, I developed a functional task management system that supports everyday productivity.

The project strengthened my understanding of mobile application architecture, database integration, persistent data storage, and user-focused software development.
