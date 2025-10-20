# 📝 Task 5 - Consumer Complaint Classification

This project implements a **text classification model** to automatically categorize consumer complaints into product types using **Natural Language Processing (NLP)** and **Naive Bayes**.

---

## 📌 Objective

- Build a model to classify consumer complaints based on the narrative text.  
- Predict which **financial product category** a complaint belongs to.  
- Analyze important words/features for each product category.  

---

## 🛠 Technology Stack

- **Python 3**  
- **Pandas & NumPy** – data manipulation  
- **NLTK** – natural language processing, stopwords  
- **Scikit-learn** – machine learning, Naive Bayes classifier  
- **Matplotlib** – visualization (confusion matrix)  

---

## 📂 Dataset

- **Source:** Consumer Complaint Database  
- **Format:** CSV  
- **Columns used:**  
  - `Product` – target label  
  - `Consumer complaint narrative` – text to classify  

**Sample Data:**

| Product | Consumer complaint narrative |
| --- | --- |
| Credit reporting | There are many mistakes appear in my report... |
| Mortgage | My mortgage payment was not processed on time. |

---

## ⚙ Workflow

1. **Import Dependencies:** Load required Python libraries.  
2. **Load Dataset:** Read CSV and select relevant columns.  
3. **Text Preprocessing:**  
   - Lowercase text  
   - Remove punctuation & numbers  
   - Remove stopwords using NLTK  
4. **Encode Labels:** Convert product categories into numeric labels.  
5. **Split Data:** Train-test split (80% train, 20% test).  
6. **Vectorization:** Convert text into numerical features using **TF-IDF**.  
7. **Train Model:** Train a **Multinomial Naive Bayes** classifier.  
8. **Evaluate Model:**  
   - Accuracy score  
   - Classification report  
   - Confusion matrix visualization  
9. **Analyze Features:** Display top words for each product category.  
10. **User Input Prediction:** Enter a complaint description and predict the product category.  
11. **Sample Predictions:** Test model with predefined sample complaints.  

---

## 📊 Model Performance

- **Accuracy:** ~67%  
- **Top Categories:**  
  - High performance: `Mortgage`, `Debt collection`, `Student loan`  
  - Low performance: `Virtual currency`, `Other financial service`  

- **Confusion Matrix:** Visualizes predicted vs actual categories.  

---

## 🔑 Example Usage

### Predicting a single complaint:

```python
user_input = "My mortgage payment was not processed on time."
user_cleaned = clean_text(user_input)
user_vec = vectorizer.transform([user_cleaned])
prediction = model.predict(user_vec)
predicted_category = le.inverse_transform(prediction)[0]
print(f"Predicted Product Category: {predicted_category}")
```
### Screenshots
![ss](https://github.com/Varshith34/KaiburrTask5/blob/f1856996c5b51471715a8c83dd3d6b92fe941b39/Task5.1.png)
![ss](https://github.com/Varshith34/KaiburrTask5/blob/f1856996c5b51471715a8c83dd3d6b92fe941b39/Task5.2.png)
![ss](https://github.com/Varshith34/KaiburrTask5/blob/f1856996c5b51471715a8c83dd3d6b92fe941b39/Task5.3.png)
