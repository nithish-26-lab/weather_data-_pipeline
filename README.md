# 🌦️ Real-Time Weather Data Pipeline

## 📌 Project Overview

The Real-Time Weather Data Pipeline is an ETL (Extract, Transform, Load) project that collects live weather data from a weather API, processes it using Python and Pandas, and stores it in a PostgreSQL database.

The pipeline is automated using Windows Task Scheduler, allowing weather data to be collected regularly. The stored data is then connected to Power BI to create an interactive dashboard for visualizing weather trends.

---

## 🏗️ Project Architecture

```text
                 🌦️ Weather API
                        │
                        ▼
              ┌─────────────────┐
              │     EXTRACT      │
              │     Python       │
              └─────────────────┘
                        │
                        ▼
              ┌─────────────────┐
              │    TRANSFORM     │
              │     Pandas       │
              └─────────────────┘
                        │
                        ▼
              ┌─────────────────┐
              │      LOAD        │
              │   PostgreSQL     │
              └─────────────────┘
                        │
                        ▼
              ┌─────────────────┐
              │    Power BI      │
              │    Dashboard     │
              └─────────────────┘
🔄 ETL Workflow
Weather API
    │
    ▼
Extract Weather Data
    │
    ▼
Transform & Clean Data
    │
    ▼
Load into PostgreSQL
    │
    ▼
Automated Data Collection
    │
    ▼
Power BI Visualization

⚙️ Technologies Used:

🐍 Python
🐼 Pandas
🌐 Weather API
🐘 PostgreSQL
🔗 SQLAlchemy
🔄 Windows Task Scheduler
📊 Power BI
🔐 Python Dotenv

📂 Project Structure:

weather-data-pipeline/
│
├── src/
│   ├── extract.py
│   ├── transform.py
│   ├── load.py
│   └── pipeline.py
│
├── .env
├── requirements.txt
├── run_pipeline.bat
├── weather_dashboard.pbix

🔹 Extract
Weather data is collected from a weather API using Python.
The extracted data includes information such as:

City
Temperature
Humidity
Apparent Temperature
Precipitation
Rain
Weather Code
Wind Speed
└── README.md

🔹 Transform
The raw API response is transformed using Pandas.
The transformation process:

Extracts required weather attributes
Converts raw JSON data into a structured format
Creates a Pandas DataFrame
Adds a timestamp for each record

🔹 Load
The transformed weather data is loaded into PostgreSQL using SQLAlchemy.

Python
   │
   ▼
SQLAlchemy
   │
   ▼
PostgreSQL
   │
   ▼
weather_data Table

⏰ Automation
The pipeline is automated using Windows Task Scheduler.

Every Hour
    │
    ▼
Windows Task Scheduler
    │
    ▼
run_pipeline.bat
    │
    ▼
Python ETL Pipeline
    │
    ▼
PostgreSQL Database

📊 Power BI Dashboard
The PostgreSQL database is connected to Power BI to visualize weather data.
The dashboard includes:

🌡️ Temperature
💧 Humidity
🌡️ Apparent Temperature
💨 Wind Speed
📈 Temperature Trend
📈 Humidity Trend
🏙️ City Filter
