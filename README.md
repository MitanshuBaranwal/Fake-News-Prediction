## News Article Classification
This Python script is designed to classify news articles into two categories: real and fake. It uses machine learning techniques to perform this task. Below, you'll find a step-by-step guide on how to use and understand this script.

Table of Contents
Import Dependencies
Load Dataset
Label Data
Combine Datasets
Remove Non-Important Columns
Shuffle the Data
Download Stopwords
Text Preprocessing
Create X and Y
Train-Test Split
Text Vectorization
Model Training and Evaluation
Choose the Final Model
Make Predictions


- [Import Dependencies](#Dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Contact](#contact)

  
## Import Dependencies

This section imports the necessary Python libraries and modules, including Pandas, NLTK, joblib, and scikit-learn. These libraries are used for data manipulation, text preprocessing, and machine learning.

2. Load Dataset<a name="load-dataset"></a>
Here, two datasets are loaded: "True.csv" and "Fake.csv." These datasets contain news articles labelled as either real or fake.

3. Label Data<a name="label-data"></a>
The "True" and "Fake" datasets are labelled with 1 for real news and 0 for fake news, respectively.

4. Combine Datasets<a name="combine-datasets"></a>
Both datasets are combined into a single DataFrame for further processing.

5. Remove Non-Important Columns<a name="remove-non-important-columns"></a>
Unnecessary columns such as "text," "subject," and "date" are removed. Only the "title" column is used for the classification.

6. Shuffle the Data<a name="shuffle-the-data"></a>
The data is shuffled to ensure randomness and prevent any inherent order bias.

7. Download Stopwords<a name="download-stopwords"></a>
Common English stopwords are downloaded. These stopwords will be removed during text preprocessing.

8. Text Preprocessing<a name="text-preprocessing"></a>
Text data is preprocessed by applying stemming, removing non-alphabetical characters, converting to lowercase, and removing stopwords.

9. Create X and Y<a name="create-x-and-y"></a>
The feature (X) and target (Y) variables are defined. X contains the preprocessed "title" column, and Y contains the corresponding labels.

10. Train-Test Split<a name="train-test-split"></a>
The data is split into training and testing sets for model evaluation. An 80-20 split is used with stratification.

11. Text Vectorization<a name="text-vectorization"></a>
The "title" text data is converted into numerical values using TF-IDF vectorization.

12. Model Training and Evaluation<a name="model-training-and-evaluation"></a>
Several machine learning models, including Logistic Regression, Decision Tree, Random Forest, and Gradient Boosting, are trained and evaluated for their performance in classifying news articles.

13. Choose the Final Model<a name="choose-the-final-model"></a>
The Random Forest classifier is chosen as the final model based on its performance.

14. Make Predictions<a name="make-predictions"></a>
A function predict_news_type is defined to take text input and predict whether the news is real or fake using the final model.

Example Usage:

print(predict_news_type("Pope Francis Just Called Out Donald Trump "))
# Output: 'The news is Real'

print(predict_news_type("Gaza receives largest aid shipment since Israel-Hamas war began"))
# Output: 'The news is Fake'
Feel free to use this script for news article classification and make predictions. You can customize it further to suit your needs.
