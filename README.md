## Project Overview
This project implements a sentiment analysis system to classify IMDB movie reviews as either **positive** or **negative**. The model is trained using machine learning algorithms and evaluates its performance based on **F1-Score** and confusion matrix analysis.

## Dataset
The dataset used is **IMDB Movie Reviews Dataset**, which consists of **50,000** reviews categorized into positive and negative classes. You can access and download the dataset from the following link:

[IMDB Movie Reviews Dataset](https://drive.google.com/file/d/13u7afZIUzeTo2RaL6SkVApdR09zRGws-/view?usp=sharing)

## Preprocessing Steps
1. **Text Cleaning**: Removal of HTML tags, URLs, and non-alphabetic characters.
2. **Lowercasing**: Converting all text to lowercase.
3. **Tokenization**: Splitting text into individual words.
4. **Stopword Removal**: Removing common words that do not contribute to sentiment.
5. **Lemmatization**: Reducing words to their base forms.

## Feature Extraction
- **TF-IDF Vectorization**: Extracts key features from the text.
- **Latent Dirichlet Allocation (LDA)**: Extracts topic distributions for enhanced classification.
- **Feature Combination**: Merging TF-IDF and LDA features for better accuracy.

## Classification Models
The following classification algorithms were considered:
- **Logistic Regression**
- **Naïve Bayes**
- **Support Vector Machines (SVM)**
- **K-Nearest Neighbors (KNN)**
- **Multi-Layer Perceptron (MLP)**

The final model selected was **Linear SVC** with hyperparameter tuning using GridSearchCV.

## Model Training & Evaluation
1. **Data Splitting**: The dataset was split into 80% training and 20% testing.
2. **Hyperparameter Tuning**: The **C** parameter was optimized using a **grid search**.
3. **Model Training**: The best model was trained on the full dataset.
4. **Performance Evaluation**:
   - **Classification Report**
   - **Confusion Matrix**
   - **F1-Score Calculation**

## Results
| Metric  | Negative Class | Positive Class | Weighted Average |
|---------|---------------|---------------|-----------------|
| Precision | 0.93 | 0.91 | 0.92 |
| Recall    | 0.91 | 0.94 | 0.92 |
| F1-Score  | 0.92 | 0.92 | 0.92 |
| Accuracy  | **0.92** | - | - |

### Confusion Matrix
|                | Predicted Positive | Predicted Negative |
|---------------|------------------|------------------|
| **Actual Positive** | 4712 | 327 |
| **Actual Negative** | 4507 | 454 |

## Observations
- The model achieves an overall **92% accuracy**.
- The recall for the **positive class** is slightly higher, meaning the model is better at detecting positive reviews.
- The balanced F1-score indicates a good trade-off between precision and recall.

## Conclusion
This sentiment analysis system successfully classifies IMDB movie reviews with high accuracy. Future improvements could involve:
- Experimenting with deep learning models like **LSTMs** or **Transformers**.
- Using **word embeddings** (Word2Vec, GloVe, BERT) instead of TF-IDF.
- Expanding the dataset to include more nuanced sentiment categories.

