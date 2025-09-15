# 🍽️ Uber Eats Restaurant Recommender

This project analyzes Uber Eats restaurant and menu data to build a location- and price-based restaurant recommendation system using **Apache Spark**, **AWS S3**, and **AWS Athena**. The system uses **cosine similarity** to find restaurants that are similar in terms of location and average menu pricing, allowing users to explore new restaurants without worrying about cost or distance.

---

## 🧰 Tech Stack

- **Apache Spark** (PySpark)
- **AWS S3** (for cloud storage)
- **AWS Athena** (for cloud-based SQL querying)
- **Spark MLlib** (for building the recommendation model)
- **Python**, **SQL**

---

## 📊 Overview
The goal of this project was to design and implement a **restaurant recommender system** that identifies similar restaurants based on menu items, location, and pricing.

Data contents:
- ~**60,000 restaurants**
- ~**1 million menu items**

📌 **Kaggle Dataset**:  
[Uber Eats USA Restaurants & Menus](https://www.kaggle.com/datasets/ahmedshahriarsakib/uber-eats-usa-restaurants-menus)

- `restaurants.csv` (10 MB)
- `restaurant-menus.csv` (871 MB)

---

## ⚙️ Tech Stack
- **Data Processing**: PySpark (Spark DataFrames, Spark SQL)
- **Storage**: AWS S3  
- **Query Engine**: AWS Athena  
- **Modeling**: Spark MLlib (cosine similarity)  
- **Language**: Python (Jupyter Notebooks)

## 🧪 Project Pipeline

1. **Data Loading**
   - Raw CSV data uploaded to AWS S3  
   - Ingested into PySpark DataFrames  

2. **Data Cleaning & Transformation**
   - Standardized menu items (case normalization, removing nulls)  
   - Price normalization  
   - Added geospatial features (latitude, longitude)  

3. **Feature Engineering**
   - Average menu prices per restaurant  
   - Aggregated cuisine and item features  
   - Location embeddings  

4. **Modeling**
   - Cosine similarity to compute restaurant similarity  
   - Recommend "nearest" restaurants by feature vector distance  

5. **Evaluation**
   - Qualitative evaluation using sample queries  
   - Validation by comparing known similar restaurants 

---

## 📈 Architecture

🛠️ **Project-Level Architecture**  
Describes how Spark, Athena, and S3 are used together to process and analyze data.

🌐 **Real-World Deployment Architecture (Optional)**  
Shows how this system could be scaled for real-time use with APIs and user queries.

📂 Diagrams can be found in the `architecture/` folder.

---

## 📌 Notes

- ⚠️ **This project was originally built using AWS S3, Athena, and Spark.**  
  While live execution is not currently possible due to AWS access limits, the notebooks include all output cells and fully reflect the pipeline's implementation and results.
  
---

## Key Insights

- Handling big data pipelines with PySpark and AWS.

- Using Athena for SQL-style querying over large datasets.

- Building a content-based recommender with cosine similarity.

- Managing scalability issues with datasets in the order of millions of rows.

---

