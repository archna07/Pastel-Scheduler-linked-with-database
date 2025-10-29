# 🎨 Pastel Student Scheduler

## 📘 Introduction
The **Pastel Student Scheduler** is a full-stack Python desktop application designed to help students structure their study sessions, manage time efficiently, and stay focused.

It combines proven productivity techniques—like the **Pomodoro Technique** and **Time-Boxing**—with real-time timers, automatic break scheduling, and visual analytics.

The app’s **pastel-themed, minimal design** creates a calm environment, helping students manage workloads without stress. It supports both planning and execution phases of study, turning abstract productivity theories into a hands-on, supportive tool.

---

## 🎯 Project Objectives

The project was developed with the following key goals:

### 🕒 Implement Time-Boxing and Flow Scheduling
Allow users to define study sessions and built-in breaks (e.g., Water/Food).  
The app calculates accurate start and end times, creating a realistic daily flow.

### ⏱️ Provide Real-Time Focus Tools (Timer & Alarms)
Includes a background **multi-threaded timer system** that runs independently, helping users focus and automatically alerting them when sessions end.

### 📊 Generate Study Analytics
Dynamically visualize schedules using **Matplotlib**, with:
- A **Time Distribution Pie Chart**
- A **Daily Schedule Bar Chart (Gantt-style)**

### 💪 Enhance Motivation & Accountability
Displays **motivational quotes** and a **progress bar** that tracks total committed time against a daily study goal.

### 🪄 Modern GUI Design
Built with **Tkinter**, providing a clean, responsive, pastel-themed interface that promotes calm focus and sustained use.

---

## ⚙️ Input and Output Discussion

### 🧾 Input
Users interact with the system through **Tkinter** input fields and buttons in two main sections — *Input Frame* and *Timer & Alarms*.

#### Session Details (for Schedule)
- **Subject/Task:** e.g., “Organic Chemistry”, “Practice Coding”
- **Duration (min):** e.g., 45, 90
- **Priority:** High / Medium / Low

#### Break Triggers (Predefined)
- **Water Break:** 5 minutes  
- **Food Break:** 30 minutes  

#### Timer Input
Separate focus timer (in minutes) for individual study sessions.

---

### 🧩 Output
The system provides **real-time and historical feedback** in several forms:

#### Scheduled Output (Treeview)
A live-updated schedule table with:
- Start Time  
- Task Name  
- Duration  
- Priority  

Automatically appends new tasks after existing ones to create a **continuous daily flow**.

#### Visualization Output (Matplotlib)
- **Time Distribution Pie Chart:**  
  Displays proportions of Study, Water Break, and Food Break.  
- **Daily Schedule Bar Chart (Gantt-style):**  
  Visualizes the full-day timeline for all tasks.

#### Real-Time & Motivational Output
- **Timer Display:** Countdown for focus sessions  
- **Progress Bar:** Tracks total study time vs. daily target (6 hours)  
- **Motivational Quotes:** Randomly displayed for encouragement  

---

## 🧠 Technologies Used

| Technology | Role / Application |
|-------------|--------------------|
| **Tkinter** | GUI framework for building the main interface (frames, buttons, tables) |
| **Matplotlib** | Data visualization for pie charts and bar charts integrated directly into the GUI |
| **NumPy** | (Optional) Numerical operations and statistical extensions for future versions |
| **Threading** | Enables concurrent timer operations without freezing the GUI |
| **datetime** | Handles scheduling logic — calculates start and end times for tasks and breaks |
| **MySQL** | Database integration for storing schedules, quotes, and persistent user data |

---

## 🗄️ Database Integration (MySQL)

The **Pastel Student Scheduler** uses a **MySQL database** to store user data persistently, ensuring that schedules, session logs, and analytics are saved even after the application is closed.  
This allows the app to maintain data across multiple sessions and prepares it for future multi-user expansion.

### ⚙️ Database Setup

1. **Install MySQL Server**
   - Download and install MySQL Community Server:  
     👉 [https://dev.mysql.com/downloads/mysql/](https://dev.mysql.com/downloads/mysql/)
   - During setup, note your **username** (usually `root`) and **password**.

2. **Create the Database**
   ```sql
   CREATE DATABASE student_scheduler;
   USE student_scheduler;

   CREATE TABLE schedule (
       id INT AUTO_INCREMENT PRIMARY KEY,
       task_name VARCHAR(100),
       duration INT,
       priority VARCHAR(10),
       start_time DATETIME,
       end_time DATETIME
   );

   CREATE TABLE quotes (
       id INT AUTO_INCREMENT PRIMARY KEY,
       quote_text VARCHAR(255)
   );
