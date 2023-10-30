## News Article Classification
This Python script is designed to classify news articles into two categories: real and fake. It uses machine learning techniques to perform this task. We are using TfIdf along with models of LogisticRegression, DecisionTreeClassifier, RandomForestClassifier and GradientBoostingClassifier for News Article Classification.

## Clone the repository:
   
   ```sh
   git clone https://github.com/MitanshuBaranwal/Fake-News-Prediction.git
   cd Fake-News-Prediction
   ```


Below, you'll find a step-by-step guide on how to use and understand this script.
- [Dependencies](#Dependencies)
- [LoadDataset](#LoadDataset)
- [LabelData](#LabelData)
- [RemoveNonImportantColumns](#RemoveNonImportantColumns)
- [ShuffleData](#ShuffleData)
- [DownloadStopwords](#DownloadStopwords)
- [TextPreprocessing](#TextPreprocessing)
- [CreateXY](#CreateXY)
- [TrainTestSplit](#TrainTestSplit)
- [TextVectorization](#TextVectorization)
- [ModelTrainingandEvaluation](#ModelTrainingandEvaluation)
- [ChooseFinalModel](#ChooseFinalModel)
- [Predict](#Predict)


  
#### Dependencies

This section imports the necessary Python libraries and modules, including Pandas, NLTK, joblib, and scikit-learn. These libraries are used for data manipulation, text preprocessing, and machine learning.

#### LoadDataset
Here, two datasets are loaded: "True.csv" and "Fake.csv." These datasets contain news articles labelled as either real or fake.

#### LabelData
The "True" and "Fake" datasets are labelled with 1 for real news and 0 for fake news, respectively.

#### CombineDatasets
Both datasets are combined into a single DataFrame for further processing.

#### RemoveNonImportantColumns
Unnecessary columns such as "text," "subject," and "date" are removed. Only the "title" column is used for the classification.

#### ShuffleData
The data is shuffled to ensure randomness and prevent any inherent order bias.

#### DownloadStopwords
Common English stopwords are downloaded. These stopwords will be removed during text preprocessing.

#### TextPreprocessing
Text data is preprocessed by applying stemming, removing non-alphabetical characters, converting to lowercase, and removing stopwords.

#### Create XY
The feature (X) and target (Y) variables are defined. X contains the preprocessed "title" column, and Y contains the corresponding labels.

#### TrainTestSplit
The data is split into training and testing sets for model evaluation. An 80-20 split is used with stratification.

#### TextVectorization
The "title" text data is converted into numerical values using TF-IDF vectorization.

#### ModelTrainingandEvaluation
Several machine learning models, including Logistic Regression, Decision Tree, Random Forest, and Gradient Boosting, are trained and evaluated for their performance in classifying news articles.

#### ChooseFinalModel
The Random Forest classifier is chosen as the final model based on its performance.

#### MakePredictions
A function predict_news_type is defined to take text input and predict whether the news is real or fake using the final model.

## Example Usage:

      print(predict_news_type("Pope Francis Just Called Out Donald Trump for his remarks"))
Output: 'The news is Real'

      print(predict_news_type("Gaza receives largest aid shipment since Israel-Hamas war began"))
Output: 'The news is Fake'
Feel free to use this script for news article classification and make predictions. You can customize it further to suit your needs.

## Contact
For any enquiries please contact me at :  

      mitanshubaranwal70232@gmail.com
