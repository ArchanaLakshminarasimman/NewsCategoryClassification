## Objective

To develop and compare models based on BERT and RoBERTa to classify news headlines into categories with high accuracy.

## Dataset Overview

- The dataset includes approximately **210k news headlines** from HuffPost between 2012 and 2022.
- Contains data on categories, short descriptions, authors, and publication dates.
- Dataset source: [News Category Dataset](https://www.kaggle.com/rmisra/news-category-dataset).

## Key Steps

### 1. Data Cleaning and Exploration
- Removed duplicates and unnecessary columns.
- Checked for missing values and basic statistics.
- Conducted exploratory data analysis (EDA) using visualizations like bar plots, pie charts, and word clouds.

### 2. Data Preprocessing
- Combined `headline` and `short_description` fields for better context.
- Removed stop words and converted text to lowercase.
- Tokenized text data using `DistilBERTTokenizer` and RoBERTa's tokenizer.

### 3. Model Training
- Fine-tuned **BERT** and **RoBERTa** models on the dataset.
- Used stratified splits for training and testing.
- Optimized models using **AdamW** optimizer and cross-entropy loss.

### 4. Evaluation
- Calculated accuracy, precision, recall, and F1-score.
- Visualized results with confusion matrices and classification reports.

## Results

| Model    | Train Accuracy | Test Accuracy |
|----------|----------------|---------------|
| **BERT** | 72.1%          | 68.8%         |
| **RoBERTa** (50k subset) | 84.7%          | 65.7%         |

### Observations
- BERT achieved better test accuracy than RoBERTa for the full dataset.
- RoBERTa was tested on a smaller subset due to computational constraints.

## Future Work
- Enhance models with dropout layers and weight decay.
- Experiment with other optimization functions and learning rate schedules.
- Use larger models like `RoBERTa-large` for better performance.
