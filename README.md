# Instructor-Effectiveness_Modeling
# 🎓 Instructor Effectiveness Prediction

**Made by:** Harmandeep Singh  
**Project Type:** Machine Learning — Classification  
**Algorithm:** Random Forest Classifier  
**Accuracy:** 83%

---

## 📌 Problem Statement
An EdTech platform runs the same course across multiple batches 
taught by different instructors. This project analyzes instructor 
effectiveness using learner outcomes, engagement, and feedback data.

---

## 📁 Dataset
- 2000 rows — each row represents one course batch
- Multiple rows per instructor
- Features include completion rate, quiz scores, 
  feedback, engagement metrics

---

## ⚙️ Approach

1. **EDA** — Null check, correlation heatmap, anomaly detection
2. **Feature Engineering** — Created weighted effectiveness score
   using correlation-based weight calculation
3. **Aggregation** — Batch level → Instructor level
4. **Classification** — Low / Medium / High tier prediction
5. **Evaluation** — Accuracy, F1 Score, Confusion Matrix

---

## 🧮 Effectiveness Score Formula

Weights derived by normalizing correlations with completion_rate:

| Feature | Weight |
|---|---|
| completion_rate | 0.26 |
| retention_rate (1-dropout) | 0.24 |
| avg_score_improvement | 0.10 |
| avg_quiz_score | 0.08 |
| avg_feedback_score/5 | 0.08 |
| feedback_response_rate | 0.07 |
| assignment_submission_rate | 0.06 |
| avg_watch_time | 0.05 |
| forum_activity_rate | 0.05 |

---

## 📊 Results

| Metric | Score |
|---|---|
| Accuracy | 83% |
| High Tier F1 | 0.93 |
| Medium Tier F1 | 0.82 |
| Low Tier F1 | 0.73 |

---

## 🔍 Key Findings
- dropout_rate was most important feature (0.31 importance)
- avg_quiz_score second most important (0.18)
- assignment_submission_rate least important (0.01)

---

## ⚠️ Limitations
- Effectiveness label is self-defined — weights based on 
  assumptions
- Small batch instructors have less reliable scores
- completion_rate can be high due to easy course, 
  not instructor quality

---

## 🛠️ Libraries Used
pandas, numpy, scikit-learn, matplotlib, seaborn

---

## 📂 Files
- `notebook.ipynb` — Main project notebook
- `dataset.csv` — Input data
- `README.md` — Project documentation
