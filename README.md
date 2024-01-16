# Academic-Project
Craiglist - Beauty and Health Section Classification


# Project Objective

To analyze and refine the beauty and health listings on Craigslist for the New York market, utilizing the region's rich data to enhance categorization and improve the user search experience.


The lack of filters and tags on Craigslist leads to a chaotic Beauty and Health section, mixing various items from weighing scale to trimmers and even coconut milk, leading to a poor search experience.


# Data Collection

Utilized Selenium and BeautifulSoup to navigate and parse web data. Retrieved approximately 1680 product URLs across 19 pages for a comprehensive dataset.
Extracted detailed product information, including Product descriptions, Title and IDs
Compiled and organized all data into CSV format

# Labels Identified
1. Fragrances
2. Skincare and Makeup
3. Hair Care
4. Health Equipments
5. Medications and Supplements
6. Other Health Care
7. Other Beauty
8. Vision Care

# Model Identification - Logistic Regression

Text Preprocessing 
Map NLTK POS tags to WordNet tags, clean, tokenize and lemmatize text

Word Weighting by TF-IDF
Use TfidfVectorizer to convert text data into TF-IDF features.

Model Building
Set hyperparameters for Logistic Regression
Use a balanced class weight to handle potential class imbalances.
Wrap Logistic Regression in OneVsRestClassifier to handle multi-label classification.

Model Evaluation
Accuracy on the test data: 0.58

# Model Identification - LSTM

Text Preprocessing: 
Convert words to lowercase, remove punctuation and symbols, and eliminate stop words

Tokenizing and Padding Documents
Convert labels into a one-hot encoded format, suitable for multi-class classification.

Model Building
An embedding layer, A spatial dropout layer (to reduce overfitting), An LSTM layer, A dense output layer with a softmax activation function

Model Evaluation
Best Model Accuracy: 0.595

Trials: Model Architecture & Embedding Dimension

GloVe Embedding - Tried 50, 100, 200, 300 dimension
Adding additional LSTM Layer
Increasing LSTM Layer from 100 to 128, 200
Increased epochs from 5 to 6

# Best Model: SVM

Text Preprocessing
Convert words to lowercase, tokenize text, remove stopwords, lemmatize words

Label Encoding
Uses LabelEncoder to convert categorical labels ('Label' column) into numerical format, which is required for training machine learning models

TF-IDF Vectorization
Convert the preprocessed text data into TF-IDF features

Model Training
Tried different kernels and identified RBF as the best one for the SVM model

Model Evaluation
Accuracy on the test data: 0.66

# Demo Implementation
![image](https://github.com/ashvinrajpinjani/Academic-Project/assets/70865274/25952b22-0a5b-4bae-a4ab-eb3327c0787d)



