# 🌦️ Weather ETL Pipeline with Apache Airflow, Astro, and PostgreSQL  

This project demonstrates how to build an **ETL (Extract, Transform, Load) pipeline** using **Apache Airflow**, **Astro (Astronomer.io)**, and **PostgreSQL**.  
The pipeline extracts live **weather data** from the [Open-Meteo API](https://open-meteo.com/), transforms it into structured format, and loads it into a PostgreSQL database.  

---

## 🚀 Features
- **Extract** weather data (temperature, windspeed, direction, etc.) from Open-Meteo API.  
- **Transform** JSON response into a clean schema.  
- **Load** transformed data into PostgreSQL database.  
- **Orchestration** handled by Apache Airflow DAGs.  
- **Astro** simplifies Airflow setup with Docker.  
- **DBeaver** used to query and verify the database.  

---

## 📂 Project Structure

├── dags/
│ └── weather_etl_pipeline.py # Main Airflow DAG
├── requirements.txt # Python dependencies
├── Dockerfile # Container setup
├── .astro/ # Astro project configs
└── README.md # Project documentation


---

## ⚙️ How It Works
1. **Airflow DAG** runs daily (`@daily`) and orchestrates tasks.  
2. **Extract Task** – Calls Open-Meteo API for London weather.  
3. **Transform Task** – Parses and formats JSON into structured data.  
4. **Load Task** – Inserts records into `weather_data` table in PostgreSQL.  
5. Logs and status can be monitored in **Airflow UI**.  

---

## 🐳 Prerequisites
- [Docker](https://www.docker.com/) installed  
- [Astro CLI](https://docs.astronomer.io/astro/cli/overview) installed  
- Python 3.9+  

---
📊 Workflow Visualization

Airflow DAG (weather_etl_pipeline) looks like this in the Airflow UI:

Extract → Transform → Load

📝 Future Enhancements

Replace Open-Meteo API with Twitter API for social data.

Add logging & alerting with Airflow Notifications.

Deploy pipeline to AWS/GCP/OCI instead of local Docker.

👨‍💻 Author

Developed by Usman Asif
Bachelor’s in Data Science | Data Engineering & Machine Learning Enthusiast
