# 📌 Real-Time Financial Data Processing Pipeline
🚀 A real-time data pipeline that fetches, processes, and visualizes financial data using **Apache Kafka, Apache Spark, PostgreSQL, and Grafana**.

## 📖 Project Overview
This project demonstrates a **real-time data processing pipeline** that:
1. **Fetches stock market data** from the **Financial Modeling Prep API**.
2. **Streams real-time financial data** into Apache Kafka.
3. **Processes the data using Apache Spark** and stores it in PostgreSQL.
4. **Visualizes insights** in Grafana dashboards.
5. Provides a **fully containerized solution** using Docker and Kubernetes.

## 🎯 Objectives
✅ **Real-time data ingestion** using **Kafka**.  
✅ **Distributed data processing** using **Apache Spark**.  
✅ **Efficient storage & querying** with **PostgreSQL**.  
✅ **Interactive dashboards** for financial analytics using **Grafana**.  
✅ **Automated workflow orchestration** using **Apache Airflow**.  
✅ **Scalable architecture** with **Docker & Kubernetes**.

## 🛠️ Technologies Used
| Category            | Tools/Technologies |
|--------------------|------------------|
| **Programming**   | Python, SQL |
| **Data Streaming** | Apache Kafka |
| **Big Data Processing** | Apache Spark (PySpark) |
| **Database** | PostgreSQL |
| **Monitoring & Dashboards** | Grafana |
| **Workflow Orchestration** | Apache Airflow |
| **Containerization** | Docker, Kubernetes |


## 📂 Project Architecture
```plaintext
┌──────────────────────────┐
│  Financial Data Source   │
│   (API)                 │
└──────────┬──────────────┘
           │
           ▼
┌──────────────────────────┐
│  Kafka Producer          │
│  - Fetches stock data    │
│  - Pushes to Kafka topic │
└──────────┬──────────────┘
           │
           ▼
┌──────────────────────────┐
│  Apache Kafka Topic      │
│  - Real-time data stream │
└──────────┬──────────────┘
           │
           ▼
┌──────────────────────────┐
│  Apache Spark Streaming  │
│  - Processes Data        │
│  - Transforms and Cleans │
└──────────┬──────────────┘
           │
           ▼
┌──────────────────────────┐
│  PostgreSQL Database     │
│  - Stores processed data │
└──────────┬──────────────┘
           │
           ▼
┌──────────────────────────┐
│  Grafana Visualization   │
│  - Dashboard for insights│
└──────────────────────────┘
```

## 🚀 Setup and Installation
### 1️⃣ Clone the Repository
```sh
git clone https://github.com/SaiGowtham18/Financial-Data_Real-Time-Streaming-Pipeline.git
cd Financial-Data_Real-Time-Streaming-Pipeline
```

### 2️⃣ Set Up Environment Variables
Create a `.env` file and add:
```ini
POSTGRES_USER=your_username
POSTGRES_PASSWORD=your_password
POSTGRES_DB=financial_data
KAFKA_BROKER=kafka:9092
```

### 3️⃣ Build and Run with Docker
```sh
docker-compose up --build
```

### 4️⃣ Verify Running Services
Check if Kafka, Spark, PostgreSQL, and Grafana are running:
```sh
docker ps
```

## 🛠️ How to Run the Project
### 1️⃣ Start the Kafka Producer
```sh
python kafka_postgresql/stream_data_producer.py
```
- This fetches real-time stock market data and streams it into Kafka.

### 2️⃣ Start the Spark Processing Job
```sh
python spark_postgresql/spark_process_data.py
```
- This reads data from Kafka, processes it, and loads it into PostgreSQL.

### 3️⃣ Access PostgreSQL
Login to PostgreSQL inside Docker:
```sh
docker exec -it postgresql psql -U your_username -d financial_data
```
Run SQL queries:
```sql
SELECT * FROM stock_data;
```

### 4️⃣ View Real-Time Dashboard in Grafana
1. Open [http://localhost:3000](http://localhost:3000) in your browser.
2. Login with `admin / admin`.
3. Navigate to **Stock Market Dashboard**.


📧 **Email:** [your-email@example.com](mailto:your-email@example.com)  
🌍 **GitHub:** [SaiGowtham18](https://github.com/SaiGowtham18)  

🚀 **Happy Coding!** 🎯
