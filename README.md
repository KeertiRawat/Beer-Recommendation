# Crowdsourced Beer Recommender System

## Project Overview
This project transforms unstructured consumer sentiment into a high-precision recommendation engine. By analyzing 20,000+ beer reviews, the system moves beyond simple numerical ratings to connect users with beers based on specific, nuanced attributes such as "black," "bourbon," and "thick."

The core of the project involves a comparative analysis of three NLP methodologies—Bag-of-Words (BoW), Pre-trained Embeddings (spaCy), and Custom Word2Vec—to determine which best captures domain-specific "beer language."

---

## Key Features & Methodology

### 1. Multi-Model NLP Pipeline
* **Bag-of-Words (Baseline):** Used exact keyword matching to identify attribute frequency across the corpus.
* **spaCy (Pre-trained):** Leveraged the `en_core_web_md` model for general semantic similarity and vector representation.
* **Custom Word2Vec:** Trained a domain-specific model to understand niche relationships, such as the semantic link between "bourbon" and "vanilla" or "oak."

### 2. Sentiment-Weighted Recommendations
* **Contextual Sentiment:** Integrated VADER Sentiment Analysis to ensure recommendations align with positive consumer experiences.
* **Weighted Scoring:** Developed a distance-weighted algorithm where words closer to an attribute mention carry more weight, ensuring high-fidelity sentiment mapping.

### 3. Data Engineering & Scraping
* **Custom Scraper:** Engineered a Selenium-based scraper to collect data for 250 top-rated beers, including metadata and reviews.
* **Balanced Dataset:** Cleaned and filtered raw transcripts to maintain a 100-review-per-beer cap, preventing popularity bias from skewing results.

---

## Tech Stack
* **Languages:** Python
* **NLP & ML:** NLTK (VADER), spaCy, Gensim (Word2Vec), Scikit-learn (Cosine Similarity)
* **Data Tools:** Selenium, BeautifulSoup, Pandas, NumPy

---

## Business Applications
* **Personalized Discovery:** Enables users to find products via taste attributes rather than just browsing top-rated lists.
* **Product Positioning:** Helps breweries identify which attributes are most valued by consumers for better marketing and packaging.
* **Unstructured Data Analytics:** Demonstrates the ability to extract actionable business insights from large-scale, messy text data.

---

## Results
The Custom Word2Vec model emerged as the most effective approach, achieving high Cosine Similarity for complex attribute queries. It successfully captured beer-specific descriptors that general models often miss, proving that domain-trained embeddings provide superior recommendation accuracy.
