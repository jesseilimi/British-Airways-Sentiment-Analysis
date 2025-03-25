# British-Airways-Sentiment-Analysis
 

## ✈️ British Airways Review Scraper & Sentiment Analysis

This project scrapes customer reviews of British Airways from [Skytrax](https://www.airlinequality.com/airline-reviews/british-airways), performs text cleaning and sentiment analysis, and visualizes customer feedback using word clouds and sentiment distribution charts.

## 📊 Project Overview

- **Goal**: Analyze customer sentiment toward British Airways using publicly available reviews.
- **Data Source**: [airlinequality.com](https://www.airlinequality.com/airline-reviews/british-airways)
- **Tools & Libraries**: 
  - Python
  - `requests`, `BeautifulSoup` (web scraping)
  - `pandas` (data handling)
  - `textblob` (sentiment analysis)
  - `wordcloud`, `matplotlib` (visualization)

---

## 📁 Project Structure

```
British-Airways/
│
├── Data/
│   ├── BA_reviews.csv                # Raw scraped reviews
│   ├── cleaned_BA_reviews.csv        # Cleaned and preprocessed reviews
│
├── Sentiment_Analysis/
│   └── sentiment_analysis.ipynb      # Notebook for text processing & visualization
│
├── review_scraper.py                 # Python script for scraping reviews
├── README.md                         # Project documentation (you're reading it!)
├── requirements.txt                  # Python dependencies
```

---

## ⚙️ Installation & Setup

1. **Clone the repository**

```bash
git clone https://github.com/your-username/British-Airways.git
cd British-Airways
```

2. **Create a virtual environment (recommended)**

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

3. **Install required packages**

```bash
pip install -r requirements.txt
```

---

## 🧼 Step 1: Scrape the Reviews

The `review_scraper.py` script scrapes the first 10 pages of British Airways reviews (100 reviews per page):

```bash
python review_scraper.py
```

This will save a file to `Data/BA_reviews.csv`.

---

## 🧹 Step 2: Clean the Data

In the sentiment analysis notebook:

- Removes HTML tags
- Strips non-alphabet characters
- Converts all text to lowercase

Cleaned reviews are saved as `cleaned_BA_reviews.csv`.

---

## 🔍 Step 3: Sentiment Analysis

- Uses **TextBlob** to calculate polarity scores for each review.
- Adds a new column: `Sentiment` (ranges from -1 to 1).

---

## 🌥️ Step 4: Visualizations

- **Word Cloud** of most frequent words
- **Histogram** showing sentiment distribution across reviews

Example output:

![Word Cloud](images/wordcloud_example.png)
![Sentiment Histogram](images/sentiment_histogram.png)

---

## 📦 Requirements

All dependencies are listed in `requirements.txt`:

```text
requests
beautifulsoup4
pandas
textblob
wordcloud
matplotlib
nltk
```

To generate this file:

```bash
pip freeze > requirements.txt
```

---

## ✅ Features

- Robust review scraping using BeautifulSoup
- Clean and structured data pipeline
- Simple sentiment scoring with TextBlob
- Easy-to-understand visualizations

---

## 🚀 Future Enhancements

- Scrape review metadata (e.g., star ratings, reviewer location)
- Use advanced NLP techniques (e.g., VADER, BERT)
- Time-series sentiment analysis (if dates are available)
- Dashboard using Streamlit or Plotly Dash

---

## 🙌 Acknowledgments

- Review data from [Skytrax Airline Quality](https://www.airlinequality.com/)
- NLP powered by [TextBlob](https://textblob.readthedocs.io/en/dev/)
- Word clouds by [wordcloud](https://github.com/amueller/word_cloud)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## ✉️ Contact

For questions or collaborations, please contact:

**Your Name**  
[LinkedIn](https://linkedin.com/in/jikato) | [Email](mailto:j.ilimikato@gmail.com)
