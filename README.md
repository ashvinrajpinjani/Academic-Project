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
