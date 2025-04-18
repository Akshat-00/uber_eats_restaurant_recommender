# 🍽️ Uber Eats Restaurant Recommendation using Spark and AWS

This project analyzes Uber Eats restaurant and menu data to build a location- and price-based restaurant recommendation system using **Apache Spark**, **AWS S3**, and **AWS Athena**. The system uses **cosine similarity** to find restaurants that are similar in terms of location and average menu pricing, allowing users to explore new restaurants without worrying about cost or distance.

---

## 🧰 Tech Stack

- **Apache Spark** (PySpark)
- **AWS S3** (for cloud storage)
- **AWS Athena** (for cloud-based SQL querying)
- **Spark MLlib** (for building the recommendation model)
- **Python**, **SQL**

---

## 📊 Dataset

The dataset was obtained from Kaggle and includes over **60K restaurants** and nearly **1M menu items**.

📌 **Kaggle Dataset**:  
[Uber Eats USA Restaurants & Menus](https://www.kaggle.com/datasets/ahmedshahriarsakib/uber-eats-usa-restaurants-menus)

- `restaurants.csv` (10 MB)
- `restaurant-menus.csv` (871 MB)

---

## 🧪 Project Pipeline

1. **Data Ingestion**
   - Files loaded from AWS S3 into PySpark DataFrames
2. **Data Cleaning & Transformation**
   - Normalized columns (e.g., "$$" → numeric), removed nulls, standardized menu item names
3. **Athena Queries**
   - Used AWS Athena for efficient SQL joins and aggregations on large datasets
4. **Feature Engineering**
   - Created final dataset with latitude, longitude, and average menu price
5. **Modeling**
   - Used Spark’s MLlib to compute **cosine similarity** between restaurants
   - Filtered and returned a list of similar restaurants
6. **Evaluation**
   - Qualitative evaluation using similarity scores and sample outputs

---

## 📈 Architecture

🛠️ **Project-Level Architecture**  
Describes how Spark, Athena, and S3 are used together to process and analyze data.

🌐 **Real-World Deployment Architecture (Optional)**  
Shows how this system could be scaled for real-time use with APIs and user queries.

📂 Diagrams can be found in the `architecture/` folder.

---

## 🧠 Challenges Faced

- All data initially in string format → Required extensive type casting and cleaning
- Large data volume (~900MB+) → Solved with Spark’s distributed processing
- Maintaining performance across joins and queries in Athena

---

## 📌 Notes

- ⚠️ **This project was originally built using AWS S3, Athena, and Spark.**  
  While live execution is not currently possible due to AWS access limits, the notebooks include all output cells and fully reflect the pipeline's implementation and results.
  
---

## 🚀 Future Improvements

- Incorporate **cuisine types** (e.g., map Pizza, Burgers → Fast Food) to improve recommendation logic
- Include **real-time data updates** using APIs
- Expand model with additional features (ratings, delivery time, etc.)

---

## 👨‍💻 Author

**Akshat Gaur**
📧 [akshat99gaur@gmail.com](mailto:akshat99gaur@gmail.com)

---



