Fake News Detection using Machine Learning
By Poojitha Pulugundla
MSc Data Science · University of Hertfordshire

#Project Overview
This project focuses on building an interpretable and efficient machine learning pipeline to classify news articles as Fake or Real using a combination of:

TF–IDF text features
Engineered stylistic features (readability, sentiment, capitalisation ratio, word count, etc.)
The goal is to create models that are accurate, explainable, and suitable for real-world decision-support contexts (not black-box systems).

#Research Question
Can traditional machine learning models accurately distinguish fake and real news articles using TF–IDF text features combined with simple linguistic and stylistic indicators?

#Dataset
Source: Kaggle – Fake and Real News Dataset
Combined size after cleaning: ~44,267 articles
#Labels:
1 → Fake News
0 → Real News


Features include article title, text, subject, publish date.
All rows with missing or empty titles/text were removed to prevent incorrect learning.

#Ethical Considerations
Dataset includes publicly available news articles, not private user data.
Contains no personal identifiers—only text is analysed.
All preprocessing avoids bias-inducing or privacy-risk elements.
Project used strictly for academic research and awareness.

#Exploratory Data Analysis (EDA)
Key patterns observed:
1. Article Length
Fake articles are typically shorter, clustering around 400–500 words.
Real news shows a wider length distribution with more long articles.

2. Readability (Flesch Score)
Fake news is generally easier to read, using simpler language.
Real news is more complex and formal.

3. Sentiment Patterns
Fake titles show more extreme sentiment (positive/negative).
Real titles are mostly neutral.

#Pre-processing Steps
Removed empty or corrupted rows.
Combined title + text into a new full_text feature.
Engineered five numeric features:
Title capitalisation ratio
Title sentiment (VADER)
Article word count
Flesch readability score
Full-text sentiment

#Models Used
1. Multinomial Naive Bayes
Trained only on TF–IDF text features
Baseline text-only performance

2. Logistic Regression (Hybrid Model)
Combined TF–IDF + numeric features
Best overall performance

3. Decision Tree (Hybrid Model)
Captures non-linear patterns
Highly interpretable


Hyperparameters (depth, regularisation) were selected based on stability and performance.

#Model Evaluation
Multiple metrics were used:
Accuracy
Precision
Recall
F1-Score
Confusion Matrix (for class-specific error analysis)


#Key insights:
Naive Bayes achieves ~93% accuracy.
Logistic Regression performs best with strong precision and recall.
Decision Tree performs well but is slightly sensitive to feature patterns.
Hybrid features significantly improve classification compared to text-only models.

#Further steps Done 
Implemented "hybrid feature engineering" combining TF-IDF, readability metrics, word counts, and sentiment features.
Optimised "Logistic Regression" and constrained "Decision Tree" to reduce overfitting.
Evaluated models using accuracy, precision, recall, F1-score, and confusion matrices.
Modularised preprocessing, training, and evaluation for reproducibility.


#Models Used
Naive Bayes  
Logistic Regression  
Decision Tree  

#Tools & Libraries
Python, Pandas, NumPy, Scikit-learn, NLTK/VADER, Matplotlib, Seaborn

#Conclusion
Hybrid feature-based "Logistic Regression" provides the most reliable and interpretable solution for fake news detection.

#work Done By
Poojitha Pulugundla
MSc Data Science | University of Hertfordshire









