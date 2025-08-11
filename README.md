# 📱 Sprint 7: Predicting Mobile Plan Selection for Megaline

## 📌 Overview
Megaline, a mobile carrier, discovered that many subscribers are still using legacy plans. To encourage adoption of their newer offerings — **Smart** and **Ultra** — this project develops a **machine learning model** to recommend the most suitable plan for each user based on their historical usage patterns.

The final model predicts whether a subscriber should be on:
- **Ultra plan** (`is_ultra = 1`)
- **Smart plan** (`is_ultra = 0`)

---

## 🎯 Objective
- **Goal:** Build a classification model with the highest possible accuracy, with a minimum threshold of **0.75** on the test set.
- **Key Deliverables:**
  1. Data exploration and preprocessing
  2. Model training with multiple algorithms
  3. Hyperparameter tuning
  4. Model evaluation on validation and test sets
  5. Business-ready recommendations

---

## 📂 Dataset
**File:** `users_behavior.csv`  
**Description:** Monthly usage statistics for subscribers already on the Smart or Ultra plan.

| Feature     | Description |
|-------------|-------------|
| calls       | Number of calls per month |
| minutes     | Total monthly call duration (in minutes) |
| messages    | Number of text messages per month |
| mb_used     | Internet traffic used in MB per month |
| is_ultra    | Target variable (1 = Ultra plan, 0 = Smart plan) |

---

## 🛠 Tech Stack
- **Python 3**
- **Pandas** — data manipulation  
- **NumPy** — numerical operations  
- **Scikit-learn** — machine learning models and evaluation  
- **Jupyter Notebook** — development environment

---

## 🔍 Methodology
1. **Data Exploration**
   - Inspected dataset shape, data types, and statistical summaries.
2. **Data Splitting**
   - Train (60%), Validation (20%), Test (20%) split.
3. **Model Training**
   - **Decision Tree Classifier** — tuned `max_depth` from 1–10  
   - **Random Forest Classifier** — tuned `n_estimators` (10–100) and `max_depth` (1–10)  
   - **Logistic Regression** — baseline linear model
4. **Evaluation Metric**
   - **Accuracy Score** used as primary metric.
5. **Model Selection**
   - Chose the best-performing model from validation results.
6. **Sanity Check**
   - Compared against random prediction baseline.

---

## 📊 Results

| Model                     | Best Parameters             | Validation Accuracy | Test Accuracy |
|---------------------------|-----------------------------|--------------------|--------------|
| Decision Tree Classifier  | `max_depth=9`                | 0.7856             | 0.7832       |
| Random Forest Classifier  | `n_estimators=50, max_depth=10` | **0.7947**         | **0.7978**   |
| Logistic Regression       | default (`liblinear`)        | 0.7101             | 0.7155       |

- **Random Forest Classifier** achieved the highest accuracy:
  - **Validation Accuracy:** 0.7947  
  - **Test Accuracy:** 0.7978  
- Significantly outperformed the **random baseline** (0.5163 accuracy).

---

## 💼 Business Impact
- Enables **personalized plan recommendations** for subscribers.
- **Increased customer satisfaction** by matching users with better-suited plans.
- **Potential revenue growth** via upselling to Ultra plan.
- **Operational efficiency** by automating plan assignment.

---

## 🚀 Recommendations
1. **Deploy Model** into Megaline’s CRM for real-time recommendations.
2. **Monitor Performance** to ensure accuracy remains above threshold.
3. **Enhance Model** with additional behavioral features (e.g., roaming, time-of-day usage).
4. **Customer Feedback Loop** for continuous improvement.

---

## 📈 Conclusion
The **Random Forest Classifier** meets business and technical requirements, achieving nearly **80% accuracy** and significantly outperforming random guessing. This model is robust, reliable, and ready for integration into Megaline’s decision-making pipeline.

---

## 📜 License
This project is licensed under the MIT License.

---

## 👤 Author
**Matt Fuller** — Data Scientist  
📧 Email: mdfulls@gmail.com
💼 LinkedIn: www.linkedin.com/in/matt-fuller2 
