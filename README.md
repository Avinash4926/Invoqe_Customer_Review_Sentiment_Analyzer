# ReviewSense — Customer Review Sentiment Analyzer

## Project Overview

**ReviewSense** is a Natural Language Processing (NLP) and data analytics project developed as part of the **Invoqe Data Analytics Internship — Task 4: Sentiment Analysis / Text Analytics**.

The project analyzes customer reviews to identify opinions and sentiment patterns. It classifies reviews into **Positive, Negative, or Neutral** categories using the VADER sentiment analysis tool.

In addition to analyzing an existing review dataset, ReviewSense allows users to enter their own review and receive an estimated sentiment prediction.

## Objectives

- Analyze customer reviews using NLP techniques.
- Clean and preprocess textual data.
- Classify reviews into positive, negative, and neutral sentiments.
- Identify frequently occurring words and patterns.
- Visualize sentiment distribution and review characteristics.
- Allow users to analyze a custom review through text input.
- Generate data-driven insights from customer feedback.

## Features

- **Dataset inspection:** Explore dataset structure, columns, missing values, and duplicates.
- **Text preprocessing:** Remove URLs, HTML tags, unwanted characters, and stopwords; normalize text and apply lemmatization.
- **Sentiment classification:** Use VADER compound scores to classify reviews.
- **Sentiment distribution:** Display sentiment counts and percentages.
- **Rating-based analysis:** Compare sentiment with customer ratings when available.
- **Review length analysis:** Explore review length and compare it across sentiment categories.
- **Word frequency analysis:** Identify commonly used words in customer reviews.
- **Word clouds:** Visualize frequently occurring words in positive and negative reviews.
- **Custom review analysis:** Enter a new review and receive a predicted sentiment with detailed VADER scores.
- **Exportable results:** Save the cleaned and analyzed dataset and sentiment summary as CSV files.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- VADER Sentiment
- WordCloud
- Jupyter Notebook

## Dataset

This project uses a customer review dataset containing textual reviews and, where available, customer ratings.

**Dataset source:** [Amazon Fine Food Reviews — Kaggle](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews)

The dataset is used to explore customer opinions and sentiment patterns. Refer to the original dataset source for its licensing and usage terms.

## Project Structure

```text
Invoqe_ReviewSense_Customer_Sentiment_Analyzer/
│
├── Customer_Review_Sentiment_Analysis.ipynb
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── reviews_raw.csv
│   ├── reviews_cleaned.csv
│   └── sentiment_summary.csv
│
└── visualizations/
    ├── sentiment_distribution.png
    ├── sentiment_percentage.png
    ├── sentiment_by_rating.png
    ├── review_length_distribution.png
    ├── average_review_length.png
    ├── top_20_words.png
    ├── positive_wordcloud.png
    ├── negative_wordcloud.png
    └── compound_score_distribution.png
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/Avinash4926/Invoqe_ReviewSense_Customer_Sentiment_Analyzer.git
```

### 2. Navigate to the project folder

```bash
cd Invoqe_ReviewSense_Customer_Sentiment_Analyzer
```

### 3. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 5. Add the dataset

Place the downloaded CSV file in the `data` folder and name it:

```text
reviews_raw.csv
```

### 6. Launch Jupyter Notebook

```bash
python -m jupyter notebook
```

Open `Customer_Review_Sentiment_Analysis.ipynb` and run the cells in order.

## Sentiment Classification

ReviewSense uses VADER compound sentiment scores to assign a sentiment label:

| Compound Score | Sentiment |
|---|---|
| 0.05 or above | Positive |
| -0.05 or below | Negative |
| Between -0.05 and 0.05 | Neutral |

The classification is rule-based and provides an estimated sentiment rather than a guaranteed interpretation of the review.

## Custom Review Analysis

The notebook includes a user-input feature that allows users to enter a customer review.

The system displays:

- Entered review
- Predicted sentiment
- Compound sentiment score
- Positive score
- Neutral score
- Negative score

This feature demonstrates how sentiment analysis can be applied to new customer feedback.

## Visualizations

The project generates visualizations including:

- Sentiment distribution
- Sentiment percentage
- Sentiment by customer rating
- Review length distribution
- Average review length by sentiment
- Top 20 frequent words
- Positive review word cloud
- Negative review word cloud
- Compound sentiment score distribution

## Key Findings

Add the actual findings after running the notebook. Example structure:

- **Dominant sentiment:** [Insert the sentiment with the highest percentage]
- **Positive reviews:** [Insert percentage]
- **Negative reviews:** [Insert percentage]
- **Neutral reviews:** [Insert percentage]
- **Average review length:** [Insert average number of words]
- **Common positive terms:** [Insert terms from the positive word cloud]
- **Common negative terms:** [Insert terms from the negative word cloud]

Findings should be based on the generated results rather than assumed values.

## Limitations

- VADER is a rule-based sentiment analyzer and may misclassify sarcasm or context-dependent reviews.
- Sentiment classification does not fully understand complex language or product-specific context.
- Results depend on the quality and representativeness of the selected dataset.
- The project provides sentiment estimates and should not be treated as a definitive measure of customer satisfaction.

## Future Enhancements

- Build a web interface using Streamlit.
- Add batch review upload and sentiment prediction.
- Compare VADER with TextBlob or machine-learning models.
- Add aspect-based sentiment analysis for product features.
- Support reviews in multiple languages.

## Internship

**Program:** Invoqe Data Analytics Internship  
**Task:** Task 4 — Sentiment Analysis / Text Analytics  
**Project:** ReviewSense — Customer Review Sentiment Analyzer

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements

- Invoqe for the Data Analytics Internship task.
- Kaggle and the dataset contributors for providing customer review data.
- NLTK and VADER contributors for NLP and sentiment analysis tools.
