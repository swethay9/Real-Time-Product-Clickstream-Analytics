# Real-Time Product Clickstream Analytics with Kafka, Spark & Airflow

🚀 This project simulates a real-time clickstream analytics pipeline—similar to those used in e-commerce platforms—for capturing, processing, and visualizing user behavior.

---

## 🧠 Architecture Overview

**Pipeline Flow:**
Kafka → Spark Structured Streaming → Parquet/CSV → Airflow DAGs → Flask Dashboard + Tableau Reports

---

## ⚙️ Technologies Used
- **Apache Kafka** – Click event ingestion
- **Apache Spark (PySpark)** – Real-time stream processing with window aggregations
- **Apache Airflow** – Job orchestration and automation
- **Flask + Plotly** – Interactive real-time dashboard
- **Tableau** – Visual analytics and trend exploration
- **Parquet/CSV** – Data storage

---

## 🔍 Key Features
- Kafka producer generates product click events
- Spark processes streaming data in 10-second time windows
- Airflow DAG schedules ETL workflows
- Final results saved in Parquet and CSV
- Flask + Plotly dashboard for live insights
- Tableau dashboard for post-analysis

---



## 📁 **Repository Structure**
pgsql
Copy
Edit
├── kafka_producer/        → Python Kafka producer for click events  
├── spark_streaming/       → PySpark Structured Streaming script  
├── airflow_dags/          → Airflow DAG to orchestrate stream jobs  
├── flask_dashboard/       → Flask app to show real-time insights  
├── data/                  → Output data in Parquet/CSV  
├── tableau_dashboard/     → Tableau visuals/snapshots  
├── requirements.txt       → Python dependencies  
└── README.md              → Project overview  


## 📊 **Demo Dashboard**
![Flask With BS Dashboard1](https://github.com/user-attachments/assets/ee9e59e0-9ff6-44f7-9382-2a48ac5c8e51)
![Flask with BS Dashboard2](https://github.com/user-attachments/assets/5fa8d787-a387-4a21-931c-19420fe85b17)





## ✅ How to Run

Tested locally on **Windows + Ubuntu WSL**. You can simulate the full stack locally.
### Step-by-Step Instructions

#### 1️⃣ Start Kafka Services (on Windows)
Start **Zookeeper** and **Kafka server**:

```bash
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
.\bin\windows\kafka-server-start.bat .\config\server.properties
2️⃣ Run Kafka Producer (on Windows)
Sends simulated product click events to Kafka topic:

bash
Copy
Edit
python3 kafka_producer.py
3️⃣ Run Spark Structured Streaming Consumer (on Ubuntu/WSL)
Consumes Kafka stream, aggregates data, and saves as Parquet and CSV:

bash
Copy
Edit
spark-submit spark_streaming_consumer.py
4️⃣ Start Apache Airflow Scheduler (on Ubuntu/WSL)
Schedules or triggers the Spark job via Airflow DAG:

bash
Copy
Edit
source ~/airflow_env/bin/activate
airflow scheduler
5️⃣ Launch Flask Dashboard (on Ubuntu/WSL)
Reads Parquet files and displays insights:

bash
Copy
Edit
python3 app.py
Then open your browser and go to:
http://localhost:5000



---



---

## 📝 **License**
This project is licensed under the MIT License.

## 📬 **Contact**
For any inquiries or suggestions, feel free to reach out:

Name: Swetha

Email: swethachowdhary33@gmail.com

GitHub: SWETHAY9

