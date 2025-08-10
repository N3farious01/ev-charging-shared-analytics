![EV Charging Station](charging_station.jpg)

📁 Project Title: Analyzing EV Charging Sessions at Shared Stations

🧠 Description:
This project explores EV charging behavior at shared stations. The analysis focuses on three deliverables: (1) unique users per garage, (2) the top 10 most popular charging start times by weekday and hour, and (3) users whose average charging duration exceeds 10 hours—filtered strictly to shared usage.

📌 Objectives:
- Filter sessions where user_type = 'Shared'.
- Compute the number of unique users per garage_id.
- Group sessions by weekdays_plugin and start_plugin_hour, then count sessions.
- Compute average charging duration per user and keep only users with AVG(duration_hours) > 10.
- Export clean, well-labeled outputs for reproducibility.

🛠️ Tools Used:
- SQL (querying)
- Datalab / PostgreSQL interface
- CSV for data export
- Text editor for code storage

📊 Output:
Three tables with the following columns:

1) unique_users_per_garage
- garage_id: Garage identifier
- num_unique_users: Number of distinct users who charged at that garage (Shared only)

2) most_popular_shared_start_times
- weekdays_plugin: Weekday of the plugin event
- start_plugin_hour: Hour (0–23) when charging started
- num_charging_sessions: Number of sessions starting at that weekday+hour (Shared only)

3) long_duration_shared_users
- user_id: User identifier
- avg_charging_duration: Average duration_hours for that user (Shared only; AVG > 10h)

📁 Files Included:
- `notebook.ipynb`: SQL queries & analysis notebook (contains the three deliverables)
- `Dataset 1_EV charging reports.csv`: Source dataset
- `project_description.txt`: Original task description

✅ Author: Abdulaziz
🗓️ Date: August 10, 2025
