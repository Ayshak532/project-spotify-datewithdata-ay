# project-spotify-datewithdata-ay

# 🎧 Spotify End-to-End Data Engineering Project (AWS)

## 📌 Project Overview
This project implements an end-to-end data engineering pipeline on AWS using Spotify data.
Raw CSV files are ingested into Amazon S3, transformed using AWS Glue Visual ETL,
and queried using Amazon Athena for analytics.

This project follows real-world data engineering practices and cloud-native architecture.

---

## 🏗️ Architecture
**AWS Services Used**
- Amazon S3 – Data storage (staging & data warehouse)
- AWS Glue – Visual ETL for data transformation
- AWS Glue Data Catalog
- Amazon Athena – SQL analytics
- AWS IAM – Secure access control

---

## 🔄 Data Flow
1. Spotify CSV files uploaded to S3 staging layer
2. AWS Glue Visual ETL:
   - Join albums and artists
   - Join tracks with album-artist data
   - Drop unnecessary fields
3. Transformed data stored in S3 data warehouse layer
4. Athena queries executed to validate transformed data

---

## 🧰 Technologies Used
- AWS S3
- AWS Glue (Visual ETL)
- PySpark
- AWS Athena
- SQL
- Python

---

## 📊 Athena Query Examples
Athena SQL queries are stored in the `athena/` directory for reproducibility.

```sql
SELECT *
FROM spotify.datawarehouse
LIMIT 10;

---



