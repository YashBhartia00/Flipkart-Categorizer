# Category_Flipkart
<!-- explain -->

# Data Cleaning and Categories
1. Removed puntuation, extra spaces and digits
2. Lower case all text
3. Chose the first Node of `product_category_tree` to be Main Category
4. Removed Categories with < 100 rows

# Exploratory Data Analysis
1. Catorical plots using Seaborn and matplotlib
2. Stiplots of price, discounts vs Category
3. Reviews Anlysis
4. Word Cloud

# Training the Model (XLNet)
1. Initially used a DistillBERT but switched to XLNet because it performs better at classification and has no number of token  
1. Used a pretrained XLNet adding a Classifier layer on top of it
2. Balanced class imbalance using class weights
3. finally used description with name, brand, and product specification

## Scores
Final Validation F1 Score: 74

Confusion Matrix:

[](.\confusion_matrix.png)

## Improvements
- Using a data augmentation method to fix class imbalance
    - using translation
    - using hypernyms and hyponymns and synonyms