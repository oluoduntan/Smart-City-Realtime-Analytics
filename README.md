# Smart City Realtime Analytics | End-to-End Data Engineering Project

## Table of Contents
- [Introduction](#introduction)
- [System Architecture](#system-architecture)
- [Technologies](#technologies)
- [Getting Started](#getting-started)

## Introduction

This project provides a comprehensive guide to building an end-to-end data engineering pipeline. It covers every stage, from data ingestion and processing to storage, using a robust tech stack that includes Apache Kafka, Apache Zookeeper, and, Apache Spark. The entire system is containerized with Docker, ensuring easy deployment and scalability.

## System Architecture

![System Architecture](https://github.com/oluoduntan)


## Technologies
- Apache Spark
- Apache Kafka
- Apache Zookeeper
- Docker
- AWS

## Getting Started

1. Clone the repository:
    ```bash
    git clone https://github.com/oluoduntan/Smart-City-Realtime-Analytics.git
    ```

2. Navigate to the project directory:
    ```bash
    cd Smart-City-Realtime-Analytics
    ```
3. Create Virtual Environment:
    ```bash
    python<version> -m venv <virtual-environment-name>
    Example: python3 -m venv myenv
    ```
4.  Activate the Virtual Environment:
    ```bash
    Mac: source venv-name/bin/activate
    Windows: env/Scripts/activate.bat (Command Prompt)
           : env/Scripts/Activate.ps1 (PowerShell)
    ```
5. Run Docker Compose to spin up the services:
    ```bash
    docker-compose up -d
    ```
6. Run the Spark Jobs
   ```bash
   docker exec -it spark-master spark-submit --master spark://spark-master:7077 --packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.5.1,org.apache.hadoop:hadoop-aws:3.3.1,com.amazonaws:aws-java-sdk:1.11.469 jobs/spark-city.py
    ```
