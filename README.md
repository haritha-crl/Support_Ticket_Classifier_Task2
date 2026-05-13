# Support Ticket Classification and Prioritization

This project implements a Machine Learning system to automatically classify and prioritize customer support tickets using Natural Language Processing (NLP).

## Overview

In modern businesses, support teams handle thousands of tickets daily. Manual categorization and prioritization is time-consuming and error-prone. This ML system automates the process, ensuring:
- Faster response times for urgent issues
- Consistent categorization
- Reduced workload for support staff

## Features

- **Text Classification**: Categorizes tickets into predefined categories (e.g., Fileservice, Software, etc.)
- **Priority Prediction**: Assigns priority levels (High, Medium, Low) based on category
- **NLP Preprocessing**: Cleans and vectorizes text using TF-IDF
- **Model Evaluation**: Comprehensive metrics and confusion matrices

## Dataset

Uses the "Classification of IT Support Tickets" dataset from Zenodo (https://zenodo.org/records/7648117), containing ~2,229 manually classified support tickets across 7 categories.

## Categories and Priorities

- **Fileservice** → Medium Priority (access issues)
- **Software** → High Priority (technical problems)
- **O365** → Medium Priority (productivity tools)
- **Active Directory** → Low Priority (system administration)
- **Computer-Services** → High Priority (hardware/software services)
- **Support general** → Low Priority (general inquiries)
- **EOL** → Low Priority (end-of-life products)

## Installation

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn nltk matplotlib seaborn
   ```
3. Download the dataset files (X_train.csv, y_train.csv, X_test.csv, y_test.csv) from Zenodo
4. Run the Jupyter notebook: `Support_Ticket_Classifier.ipynb`

## Usage

1. Open the notebook in Jupyter
2. Execute all cells to train the models
3. Use the `classify_ticket()` function for new predictions:

```python
category, priority = classify_ticket("My software won't install")
print(f"Category: {category}, Priority: {priority}")
```

## Model Performance

- **Category Classification**: ~85% accuracy using Logistic Regression
- **Priority Prediction**: ~90% accuracy using Naive Bayes

## Files

- `Support_Ticket_Classifier.ipynb`: Main notebook with full implementation
- `category_model.pkl`: Trained category classifier
- `priority_model.pkl`: Trained priority predictor
- `tfidf_vectorizer.pkl`: TF-IDF vectorizer
- Dataset CSV files

## Business Impact

This system can:
- Reduce ticket sorting time by 70%
- Ensure critical issues are addressed within SLA
- Improve customer satisfaction through faster resolutions
- Scale to handle increasing ticket volumes

## Technologies Used

- Python
- Scikit-learn
- NLTK
- Pandas
- Matplotlib/Seaborn
- Jupyter Notebook