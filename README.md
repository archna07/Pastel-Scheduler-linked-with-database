🎨 Pastel Student Scheduler
📘 Introduction
The Pastel Student Scheduler is a full-stack Python desktop application designed to help students structure their study sessions, manage time efficiently, and stay focused.
It combines proven productivity techniques—like the Pomodoro Technique and time-boxing—with real-time timers, automatic break scheduling, and visual analytics.

The app’s pastel-themed, minimal design creates a calm environment, helping students manage workloads without stress. It supports both planning and execution phases of study, turning abstract productivity theories into a hands-on, supportive tool.

🎯 Project Objectives
The project was developed with the following key goals:

Implement Time-Boxing and Flow Scheduling:
Allow users to define study sessions and built-in breaks (e.g., Water/Food). The app calculates accurate start and end times, creating a realistic daily flow.

Provide Real-Time Focus Tools (Timer & Alarms):
Includes a background multi-threaded timer system that runs independently, helping users focus and automatically alerting them when sessions end.

Generate Study Analytics:
Dynamically visualize schedules using Matplotlib, with:

A Time Distribution Pie Chart
A Daily Schedule (Bar Chart)
Enhance Motivation & Accountability:
Display motivational quotes and a visible progress bar that tracks total committed time against a daily study goal.

Modern GUI Design:
Use Tkinter to build a clean, responsive, pastel-themed interface that promotes calm focus and sustained use.

⚙️ Input and Output Discussion
🧾 Input
Users interact with the system through Tkinter input fields and buttons in two main sections — Input Frame and Timer & Alarms.

Session Details (for Schedule):

Subject/Task: e.g., "Organic Chemistry", "Practice Coding"
Duration (min): e.g., 45, 90
Priority: High / Medium / Low
Break Triggers (Predefined):

Water Break: 5 minutes
Food Break: 30 minutes
Timer Input:

Separate focus timer in minutes for single study sessions.
🧩 Output
The system provides real-time and historical feedback in several forms:

Scheduled Output (Treeview):

A live-updated schedule table with:
Start Time
Task Name
Duration
Priority
Automatically appends new tasks after existing ones to create a continuous flow.
Visualization Output (Matplotlib):

Time Distribution Pie Chart:
Displays proportions of Study, Water Break, and Food Break.
Daily Schedule Bar Chart (Gantt-style):
Shows the full-day timeline for all tasks.
Real-Time & Motivational Output:

Timer Display: Shows countdown for focus sessions.
Progress Bar: Tracks total study time vs. target goal (6 hours).
Motivational Quotes: Randomly displayed to encourage consistency.
🧠 Technologies Used
Technology	Role / Application
Tkinter	GUI framework for building the main interface (frames, buttons, tables).
Matplotlib	Data visualization for pie charts and bar charts integrated directly into the GUI.
NumPy	(Optional) For handling numerical operations and statistical extensions in future versions.
Threading	Enables concurrent timer operations without freezing the GUI.
datetime	Handles scheduling logic — calculates start and end times for tasks and breaks.
🖼️ Screenshots
🪟 Fig. 1 — Application Interface
Shows the main layout of the Pastel Student Scheduler.

📅 Fig. 2 — Task Scheduling
Allows adding multiple sessions and breaks.
Demonstrates automatic sequencing and Pomodoro-style scheduling across time blocks (even across midnight).
⏱️ Fig. 3 — Timer & Analytics
Timer & Alarms: Real-time focus control panel.
Analytics:
Pie Chart for time distribution.
Bar Chart (Gantt-style) for a 24-hour schedule view.
💡 Fig. 4 — Motivation & Progress
Displays motivational quotes and a progress tracker toward the daily study goal.
🗄️ Database Integration (MySQL)

The Pastel Student Scheduler uses a MySQL database to store user data persistently, ensuring that schedules, session logs, and analytics are saved even after the application is closed.
This makes the application scalable for multi-day usage and potential expansion to multi-user support.s
💾 Installation and Usage
1. Clone the Repository
git clone https://github.com/archna07/Pastel-studentscheduler.git
cd Pastel-studentscheduler 
