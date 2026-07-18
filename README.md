# 📊 InsightVoice AI

### Customer Feedback Intelligence using Machine Learning and Natural Language Processing

---

## 📖 Overview

**InsightVoice AI** is an end-to-end **Machine Learning** and **Natural Language Processing (NLP)** project that automatically analyzes customer reviews and classifies them into **Positive**, **Neutral**, or **Negative** sentiments.

The project is built using the **Amazon Product Reviews Dataset**, containing **568,454 real-world customer reviews**, and demonstrates a complete sentiment analysis pipeline—from data preprocessing and feature engineering to model training, evaluation, and interactive sentiment prediction.

Rather than relying on a single machine learning algorithm, the project compares the performance of multiple classification models and selects the best-performing model based on evaluation metrics and predictive performance.

This repository is designed to showcase an end-to-end machine learning workflow while demonstrating practical applications of Natural Language Processing for customer feedback analysis.

---

## 🎯 Problem Statement

Customer reviews are one of the most valuable sources of feedback for businesses. However, manually reading and categorizing hundreds of thousands of reviews is time-consuming, expensive, and impractical.

The objective of this project is to automate this process by developing a sentiment analysis model capable of understanding customer opinions and accurately classifying reviews into predefined sentiment categories.

Such systems can help organizations:

- Understand customer satisfaction
- Identify product strengths and weaknesses
- Monitor customer sentiment at scale
- Support data-driven business decisions

---

## ✨ Key Features

- 📊 End-to-end Machine Learning workflow
- 📝 Natural Language Processing (NLP) pipeline
- 🧹 Comprehensive text preprocessing
- 🔤 TF-IDF feature extraction
- 🤖 Multiple Machine Learning models
- 📈 Model performance comparison
- 📉 Confusion Matrix visualization
- 💾 Saved trained models for future inference
- 🔍 Interactive sentiment prediction
- 📁 Well-organized and reproducible project structure

---

## 🚀 Project Workflow

```text
Amazon Product Reviews Dataset
               │
               ▼
     Exploratory Data Analysis
               │
               ▼
     Data Cleaning & Preprocessing
               │
               ▼
        Text Vectorization
          (TF-IDF)
               │
               ▼
   Machine Learning Model Training
               │
               ▼
       Model Evaluation
               │
               ▼
 Best Performing Model Selection
        (Linear SVM)
               │
               ▼
 Interactive Sentiment Prediction
```

---

## 🛠️ Project Highlights

| Feature | Description |
|---------|-------------|
| Dataset | Amazon Product Reviews |
| Total Reviews | **568,454** |
| Sentiment Classes | Positive, Neutral, Negative |
| NLP Technique | TF-IDF Vectorization |
| Machine Learning Models | Multinomial Naive Bayes, Logistic Regression, Linear SVM |
| Best Performing Model | Linear SVM |
| Programming Language | Python |
| Libraries | Pandas, NumPy, Scikit-learn, Matplotlib, NLTK, Joblib |

---

> **InsightVoice AI demonstrates how Natural Language Processing and Machine Learning can transform large-scale customer feedback into actionable insights through accurate and automated sentiment classification.**

---

## 📂 Dataset

The project uses the **Amazon Product Reviews Dataset**, a large-scale collection of real customer reviews widely used for sentiment analysis and Natural Language Processing research.

The dataset contains customer feedback with corresponding sentiment labels, enabling supervised machine learning for multi-class sentiment classification.

### Dataset Summary

| Attribute | Value |
|-----------|------:|
| Dataset Name | Amazon Product Reviews |
| Total Reviews | **568,454** |
| Total Features | **10** |
| Sentiment Classes | Positive, Neutral, Negative |
| Classification Type | Multi-class Classification |

### Sentiment Distribution

| Sentiment | Number of Reviews |
|-----------|------------------:|
| 😊 Positive | **443,777** |
| 😐 Neutral | **42,640** |
| 😞 Negative | **82,037** |

The dataset is naturally imbalanced, with **Positive** reviews representing the majority class. This characteristic reflects real-world customer feedback, where satisfied customers generally outnumber dissatisfied ones.

---

## 📊 Exploratory Data Analysis (EDA)

Before model development, exploratory data analysis was performed to understand the structure, quality, and distribution of the dataset.

The analysis focused on:

- Understanding dataset dimensions
- Identifying missing values
- Examining sentiment distribution
- Analyzing rating distribution
- Investigating review length distribution
- Exploring text characteristics

The generated visualizations provide valuable insights into the dataset and help guide preprocessing and feature engineering decisions.

### EDA Visualizations

The project includes visualizations such as:

- Rating Distribution
- Sentiment Distribution
- Review Length Distribution

These visualizations are available in the **figures/** directory.

---

## 🧹 Data Preprocessing

Customer reviews contain inconsistent formatting, punctuation, stop words, and other textual noise that can negatively impact machine learning performance.

To prepare the data for modeling, a comprehensive preprocessing pipeline was applied.

### Preprocessing Steps

- Convert text to lowercase
- Remove punctuation
- Remove numerical characters
- Remove stop words
- Apply lemmatization
- Clean unnecessary whitespace

These preprocessing steps normalize textual data while preserving semantic meaning, resulting in cleaner input for feature extraction.

---

## 🔤 Feature Engineering

Since machine learning algorithms cannot directly process raw text, customer reviews were transformed into numerical feature vectors using **Term Frequency–Inverse Document Frequency (TF-IDF)**.

TF-IDF measures the importance of words within individual reviews while reducing the influence of commonly occurring words across the dataset.

### Why TF-IDF?

- Converts text into numerical vectors
- Captures word importance
- Reduces the impact of frequently occurring words
- Produces sparse, high-dimensional feature representations
- Well-suited for traditional machine learning algorithms

The generated TF-IDF vectors served as the input features for all classification models used in this project.

---

## 🤖 Machine Learning Models

To evaluate the effectiveness of different machine learning algorithms for sentiment classification, three widely used supervised learning models were implemented and compared.

Each model was trained using the same TF-IDF feature vectors, ensuring a fair comparison based on identical input features.

### Models Implemented

#### 1. Multinomial Naive Bayes

Multinomial Naive Bayes is a probabilistic classifier commonly used for text classification problems. It is computationally efficient and performs well on high-dimensional sparse datasets generated through TF-IDF vectorization.

#### 2. Logistic Regression

Logistic Regression is a robust linear classification algorithm that estimates class probabilities using the logistic function. It provides a strong baseline for many Natural Language Processing tasks.

#### 3. Linear Support Vector Machine (Linear SVM)

Linear SVM is a powerful supervised learning algorithm designed for high-dimensional classification problems. It identifies the optimal decision boundary that maximizes the margin between different sentiment classes, making it highly effective for text classification.

After comparing all three models, **Linear SVM achieved the best overall performance** and was selected as the final model for sentiment prediction.

---

## 📈 Model Evaluation

The trained models were evaluated using multiple performance metrics to ensure a comprehensive assessment of their classification capabilities.

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

Using multiple evaluation metrics provides a balanced understanding of model performance, especially when working with an imbalanced dataset.

Confusion matrices were generated for each classifier to visualize prediction accuracy across all sentiment classes.

---

## 🏆 Model Comparison

The performance of all implemented machine learning models was compared using standard classification metrics.

The notebook includes:

- Performance comparison table
- Comparative performance graph
- Individual confusion matrices
- Classification reports

These comparisons provide a clear understanding of the strengths and limitations of each model and support the selection of the best-performing classifier.

---

## ✅ Final Model Selection

Based on the evaluation results, **Linear Support Vector Machine (Linear SVM)** demonstrated the strongest overall performance and was selected as the final prediction model.

The model consistently achieved superior classification performance while maintaining excellent generalization on unseen customer reviews.

---

## 💾 Saved Models

To avoid retraining the model every time predictions are required, the trained artifacts were saved using **Joblib**.

The repository includes:

- Trained Linear SVM model
- TF-IDF Vectorizer

Saving these artifacts enables fast and efficient inference for future applications without repeating the complete training pipeline.

---

## 🔍 Interactive Sentiment Prediction

The notebook includes an interactive prediction interface that allows users to enter custom customer reviews and receive instant sentiment predictions.

Example workflow:

```text
Enter Customer Review
        │
        ▼
Text Preprocessing
        │
        ▼
TF-IDF Vectorization
        │
        ▼
Linear SVM Prediction
        │
        ▼
Positive / Neutral / Negative
```

This demonstrates how the trained model can be applied to real-world customer feedback beyond the original dataset.

---

## 📁 Repository Structure

```text
InsightVoice-AI/
│
├── dataset/
│   └── README.md
│
├── figures/
│   ├── rating_distribution.png
│   ├── sentiment_distribution.png
│   ├── review_length_distribution.png
│   ├── model_comparison.png
│   ├── nb_confusion_matrix.png
│   ├── lr_confusion_matrix.png
│   └── svm_confusion_matrix.png
│
├── models/
│   ├── svm_model.pkl
│   └── tfidf_vectorizer.pkl
│
├── notebook/
│   └── InsightVoice_AI.ipynb
│
├── outputs/
│   ├── model_comparison.csv
│   └── missing_values_summary.csv
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/MansiMuneshwar/InsightVoice-AI.git
```

Navigate to the project directory:

```bash
cd InsightVoice-AI
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

1. Clone the repository.
2. Install all required Python libraries.
3. Open the Jupyter Notebook or Google Colab notebook located in the `notebook/` directory.
4. Run the notebook cells sequentially.
5. Use the interactive prediction section to classify custom customer reviews.

---

## 📈 Results

The project demonstrates that traditional Machine Learning techniques combined with effective Natural Language Processing can achieve strong performance on large-scale customer review datasets.

Among the evaluated models, **Linear Support Vector Machine (Linear SVM)** consistently produced the best overall performance and was selected as the final sentiment classifier.

The repository includes:

- Model comparison table
- Performance visualizations
- Confusion matrices
- Saved trained model
- Interactive prediction pipeline

---

## 🚀 Future Improvements

Potential enhancements for future versions of this project include:

- Deep Learning–based sentiment analysis
- Transformer models (BERT, RoBERTa)
- Streamlit web application
- Flask/FastAPI REST API
- Docker containerization
- Cloud deployment
- Real-time sentiment prediction
- Model explainability using SHAP or LIME

---

## 🤝 Contributing

Contributions, suggestions, and improvements are always welcome.

If you would like to contribute:

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes.
4. Submit a Pull Request.

---

## 👩‍💻 Author

**Mansi Muneshwar**

- LinkedIn: https://www.linkedin.com/in/mansi-muneshwar/
- GitHub: https://github.com/MansiMuneshwar

---

## 📜 License

This project is licensed under the **MIT License**.

See the `LICENSE` file for more information.

---

⭐ If you found this project useful, consider giving the repository a **Star** on GitHub.
