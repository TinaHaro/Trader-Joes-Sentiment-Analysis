[README.md](https://github.com/user-attachments/files/27310729/README.md)
# 🛒 Trader Joe's Reddit Sentiment Analysis

**Course:** CISD 43 | **Author:** Christina Perez De-Haro

## Overview

This project scrapes posts from the r/traderjoes subreddit and performs natural language processing (NLP) and sentiment analysis to uncover how Reddit users feel about Trader Joe's. Using TextBlob for sentiment scoring and NLTK for tokenization, the analysis categorizes posts as positive, negative, or neutral and visualizes the results through bar charts, pie charts, polarity trend lines, and word clouds.

---

## Features

- **Reddit Data Collection** — Fetches up to 100 posts from r/traderjoes using Reddit's public JSON API
- **Data Cleaning** — Selects relevant columns, converts UTC timestamps, handles missing post bodies, strips emojis and whitespace
- **Sentiment Analysis** — Computes polarity and subjectivity scores using TextBlob; labels each post as Positive, Negative, or Neutral
- **Visualizations:**
  - Bar chart of sentiment counts
  - Pie chart of sentiment distribution
  - Polarity trend line across all posts
  - Word cloud of all post text
  - Word cloud filtered to adjectives only (using NLTK POS tagging)

---

## Tech Stack

| Library | Purpose |
|---|---|
| `requests` | Reddit API data fetching |
| `pandas` / `numpy` | Data manipulation |
| `TextBlob` | Sentiment polarity & subjectivity |
| `NLTK` | Tokenization & POS tagging |
| `WordCloud` | Word cloud generation |
| `matplotlib` | Data visualization |
| `emoji` | Emoji-to-text conversion |
| `re` | Text cleaning with regex |

---

## Setup

Install required libraries:

```bash
pip install emoji textblob wordcloud nltk
```

Then run all cells in `TraderJoes.ipynb` from top to bottom.

> **Note:** NLTK will automatically download the required `punkt_tab` and `averaged_perceptron_tagger_eng` data on first run.

---

## Project Structure

```
TraderJoes.ipynb    # Main notebook with all code and outputs
README.md           # Project documentation
```

---

## References

- [Reddit JSON API Documentation](https://www.jcchouinard.com/documentation-on-reddit-apis-json/)
- [Handling Emojis in NLP](https://medium.com/@ebimsv/nlp-series-day-5-handling-emojis-strategies-and-code-implementation-0f8e77e3a25c)
- [Matplotlib Pie Chart Gallery](https://matplotlib.org/stable/gallery/pie_and_polar_charts/pie_features.html)
- [Getting Started with NLTK](https://medium.com/@danielwume/getting-started-with-nltk-10-essential-examples-for-natural-language-processing-in-python-54451eae1366)
- [NLTK Book – Chapter 5: POS Tagging](https://www.nltk.org/book/ch05.html)
- [Filtering Adjectives from Strings](https://stackoverflow.com/questions/71974922/is-there-a-way-to-filter-out-all-adjectives-from-a-string-and-store-them-in-an-a)
