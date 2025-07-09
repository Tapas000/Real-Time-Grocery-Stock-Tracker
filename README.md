
# 📦 Real-Time Inventory Management System

This project simulates a real-time inventory tracking system using **Apache Kafka**, **PostgreSQL**, **Streamlit**, and **Grafana**.

## ✅ What Happens in Real-Time
A random grocery product is ordered every 2 seconds by producer.py.
consumer.py reads the order from **Kafka**:
Updates the stock table (decreases quantity)
Logs the order in the orders table
All data is committed in **PostgreSQL** for analytics or dashboards.

---

## 🔧 Tech Stack

- **Apache Kafka and zookeeper** – Real-time messaging system to stream order events.
- **PostgreSQL** – Relational database to manage stock and order history.
- **Docker Compose** – Container orchestration for Kafka, Zookeeper, PostgreSQL, and Grafana.
- **Streamlit** – Real-time dashboard to visualize stock levels and alerts.
- **Plotly** – For interactive visualizations within the dashboard.
- **Grafana** – (Optional) For monitoring and advanced dashboards.

---

## 🚀 Features

- 📤 **Kafka Producer** generates random orders every few seconds.
- 📥 **Kafka Consumer** logs transactions and updates stock in PostgreSQL.
- 📊 **Streamlit Dashboard** shows real-time inventory levels with low-stock alerts.
- 📈 **Grafana =** is used for real time dashboard , refresh every 5 sec

---

## 🐳 Docker Setup

docker-compose up --build

project/
├── docker-compose.yml
├── producer.py
├── consumer.py
├── app.py
├── db/
│   └── init.sql
└── README.md

