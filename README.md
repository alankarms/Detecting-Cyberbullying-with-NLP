# Detecting Cyberbullying with NLP: A Comparative Study of Machine Learning Models

This project uses Natural Language Processing (NLP) and machine learning to detect and classify cyberbullying in tweets. The aim is to compare different classification models and evaluate how effectively text-based features can identify harmful online behaviour.

## Project Overview

The analysis uses a labelled tweet dataset containing 47,692 entries across six classes:

- Religion
- Age
- Gender
- Ethnicity
- Other cyberbullying
- Not cyberbullying

The project includes text preprocessing, exploratory data analysis, feature extraction, model training, and model comparison.

## Methods Used

The NLP pipeline includes:

- Tokenisation
- Lowercasing
- Stopword removal
- Punctuation and special character removal
- Stemming and lemmatisation
- POS tagging and chunking
- VADER and TextBlob sentiment analysis
- Named entity recognition
- TF-IDF feature extraction

Three machine learning models were trained and compared:

- Naive Bayes
- Support Vector Machine (SVM)
- Random Forest

## Results

| Model | Accuracy | Macro F1-Score | Weighted F1-Score |
|---|---:|---:|---:|
| Naive Bayes | 0.7659 | 0.7652 | 0.7639 |
| SVM | 0.8233 | 0.8245 | 0.8230 |
| Random Forest | 0.8013 | 0.8057 | 0.8041 |

The SVM model achieved the best overall performance, with an accuracy of approximately 82.33%.

## Repository Contents

```text
.
├── cyberbullying_nlp.ipynb
├── Detecting_Cyberbullying_with_NLP_Report.pdf
├── cyberbullying_tweets.csv
├── README.md
└── requirements.txt
```

## How to Run

Clone the repository:

```bash
git clone https://github.com/alankarms/Detecting-Cyberbullying-with-NLP.git
cd Detecting-Cyberbullying-with-NLP
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Download the spaCy English model:

```bash
python -m spacy download en_core_web_sm
```

Make sure the dataset is stored in the following location:

```text
data/cyberbullying_tweets.csv
```

The notebook reads the dataset using:

```python
df = pd.read_csv("data/cyberbullying_tweets.csv")
```

Open the notebook:

```bash
jupyter notebook cyberbullying_nlp.ipynb
```

## Technologies Used

- Python
- pandas
- NumPy
- NLTK
- spaCy
- TextBlob
- VADER
- scikit-learn
- matplotlib
- wordcloud
- Jupyter Notebook

## Report

The full methodology, analysis, results, discussion, and limitations are available in:

```text
Detecting_Cyberbullying_with_NLP_Report.pdf
```

## Content Warning

This dataset contains offensive language, slurs, harassment, and abusive text as part of the cyberbullying detection task.
