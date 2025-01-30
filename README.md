# Dynamic Stock Stream Processing with Kafka and AWS

Real-time data processing is the backbone of modern data-driven businesses. **Stock-Market-Real-Time-Data-Analysis** is a full-stack, scalable pipeline that simulates real-world stock market scenarios by generating, processing, storing, and analyzing real-time stock data. This project combines cutting-edge technologies like **Apache Kafka**, **Amazon S3**, **AWS Glue**, and **Amazon Athena** to deliver an end-to-end data streaming and analytics platform.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Architecture](#architecture)
- [Features](#features)
- [Core Technologies](#core-technologies)
- [Setup and Installation](#setup-and-installation)
- [Step-by-Step Workflow](#step-by-step-workflow)
- [Use Cases](#use-cases)
- [Future Scope](#future-scope)
- [Why This Project?](#why-this-project)
- [How to Run the Project](#how-to-run-the-project)
- [Contact Me](#contact-me)
- [License](#license)

---

## 🔍 About the Project

The goal of this project is to showcase the **real-time data processing pipeline** for **stock market simulation and analysis**. The pipeline can handle large volumes of data efficiently and demonstrates the practical application of big data technologies and cloud computing.

### Key Objectives:
- Build a **reliable real-time streaming system** using Kafka.
- Store the streamed data securely on **Amazon S3**.
- Automate metadata extraction and organization with **AWS Glue**.
- Enable fast querying and analytics with **Amazon Athena**.
- Simulate a real-world environment for processing and analyzing stock data.

### Why This Project?

This project is ideal for demonstrating skills in:
- **Big Data Technologies**: Working with large-scale data in real-time.
- **Cloud Computing**: Leveraging AWS services for modern data solutions.
- **Software Architecture**: Designing and implementing scalable data pipelines.
- **Analytics**: Empowering decision-making with processed data.

---

## 🏗 Architecture

The architecture of this project is designed to ensure scalability, fault-tolerance, and efficiency:

<img width="950" alt="Screenshot 2025-01-11 at 11 38 30 PM" src="https://github.com/user-attachments/assets/af0a3035-8dac-4a42-95e9-0919be33ec06" />
![Architecture Diagram](Architecture.jpg)

### Key Components:

1. **Producer**:
   - Simulates stock market data from a CSV dataset.
   - Streams data to Kafka using Python.
   - Integrates with AWS services via the `boto3` SDK.

2. **Apache Kafka**:
   - Acts as the backbone of real-time data streaming.
   - Deployed on **AWS EC2** for high availability.

3. **Consumer**:
   - Listens to Kafka topics.
   - Processes and pushes data into **Amazon S3**.

4. **Amazon S3**:
   - Stores stock market data for long-term durability.
   - Serves as the input for analytics workflows.

5. **AWS Glue**:
   - Automates the creation of metadata and schema for the data.
   - Integrates seamlessly with S3 and Athena.

6. **Amazon Athena**:
   - Provides SQL-based analytics and querying capabilities for processed data.

---

## ✨ Features

- **Real-Time Data Simulation**:
  - Generates stock market data dynamically for testing and analysis.
  
- **Stream Processing**:
  - Kafka enables high-throughput and low-latency data streaming.

- **Cloud-Based Storage**:
  - Leverages Amazon S3 for scalability, reliability, and affordability.

- **Automated Metadata Management**:
  - AWS Glue crawlers automate schema creation and management.

- **SQL Analytics**:
  - Query raw and processed data in Amazon S3 using Athena's SQL interface.

- **Scalable Architecture**:
  - Designed to handle increasing workloads with ease.

---

## 🛠 Core Technologies

- **Programming Languages**: Python
- **Real-Time Streaming**: Apache Kafka
- **Cloud Services**:
  - Amazon S3
  - AWS Glue
  - Amazon Athena
- **Deployment**: AWS EC2
- **Data Formats**: CSV, Parquet
- **SDKs**: `boto3`, `kafka-python`

---

## 🚀 Setup and Installation

### Prerequisites
1. AWS Account (with S3, Glue, and Athena access).
2. Apache Kafka installed on an AWS EC2 instance.
3. Python 3.7+ with required libraries installed.
4. IAM role with permissions for S3, Glue, and Athena.

### Installation Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/Stock-Market-Real-Time-Data-Analysis.git
   cd Stock-Market-Real-Time-Data-Analysis
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up AWS credentials**:
   - Configure  AWS access and secret keys in `~/.aws/credentials`.

4. **Update configurations**:
   - Modify the `config.py` file with  Kafka broker addresses, S3 bucket name, and other parameters.

5. **Deploy Kafka**:
   - Install and configure Kafka on EC2 instance following [this guide](https://kafka.apache.org/quickstart).

---

## 📜 Step-by-Step Workflow

1. **Producer**:
   - Simulates stock market data from a dataset and streams it to Kafka.

2. **Kafka**:
   - Buffers and distributes the real-time data stream.

3. **Consumer**:
   - Processes the stream and stores it in Amazon S3.

4. **AWS Glue**:
   - Crawls the S3 bucket to extract and catalog metadata.

5. **Athena**:
   - Enables querying and analytics of stock market data.

---

## 🌟 Use Cases

- **Real-Time Analytics**:
  - Analyze market trends, stock movements, and volumes in real-time.
  
- **Data Lake Solution**:
  - Create a centralized repository of historical stock data.

- **Big Data Processing**:
  - Demonstrate scalability with increasing data streams.

---

## 🔮 Future Scope

- **Dashboard Integration**:
  - Build visualizations using Amazon QuickSight or Tableau.
  
- **AI Integration**:
  - Incorporate machine learning models for stock predictions.

- **Multi-Region Availability**:
  - Deploy across multiple AWS regions for enhanced fault tolerance.

- **Enhanced Security**:
  - Add Kafka ACLs and AWS-specific security practices like encryption.


## ▶ How to Run the Project

1. **Start Kafka**:
   - Launch Zookeeper and Kafka brokers on your EC2 instance:
     ```bash
     bin/zookeeper-server-start.sh config/zookeeper.properties
     bin/kafka-server-start.sh config/server.properties
     ```

2. **Run the Producer**:
   - Simulate and stream stock data:
     ```bash
     python producer.py
     ```

3. **Run the Consumer**:
   - Consume data from Kafka and upload it to S3:
     ```bash
     python consumer.py
     ```

4. **Run AWS Glue Crawler**:
   - Create and start a crawler to catalog the data.

5. **Query with Athena**:
   - Use SQL queries to analyze the data in S3.


Sources: Reference - @Darshil parmer
