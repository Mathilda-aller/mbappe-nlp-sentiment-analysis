# Kylian Mbappé Transfer Analysis: A Study of Public Opinion Using Sentiment Analysis and Topic Modeling

This project conducts a comprehensive analysis of public opinion in the French-speaking world regarding the high-profile transfer of football superstar Kylian Mbappé to Real Madrid. By scraping and analyzing thousands of YouTube comments before and after the transfer, this study uses Natural Language Processing (NLP) techniques to uncover shifts in public sentiment and identify key discussion topics.

This repository contains all the code, notebooks, and visualizations used for the research paper: *A Study of Public Evaluation in French-speaking Regions on Kylian Mbappé's Transfer to Real Madrid Based on Sentiment Analysis and Topic Modeling*.

## 📊 Key Findings

Based on the analysis of over 6,000 cleaned French comments, the study reveals:

* **Sentiment Shift**: There was a noticeable shift in public sentiment following the transfer announcement. While comments were predominantly positive when Mbappé was at PSG, the proportion of negative comments increased after the move to Real Madrid. This reflects a part of the fan base's disappointment with his decision to leave.
* **Time-based Emotional Fluctuation**: A time-series analysis shows that sentiment towards Mbappé became significantly more negative between October and November post-transfer, which may correlate with a dip in his on-field performance and other negative press at the time.
* **Core Discussion Topics**: The LDA topic model identified five major themes in the comments:
    1.  Mbappé's personal qualities and public image (maturity, intelligence).
    2.  His achievements and career milestones (champion).
    3.  The transfer itself and his future at Real Madrid.
    4.  Discussions related to PSG, media, and controversies.
    5.  His football talent, potential, and opportunities.
* **Impact of Transfer on Topics**: While discussions about Mbappé's talent and achievements remained stable, conversations about his future with Real Madrid and the controversies surrounding the transfer saw a significant increase after the move was confirmed.

## ⚙️ Project Methodology

The project follows a systematic data science workflow:

1.  **Data Collection**: Scraped approximately 11,100 French comments from 10 YouTube videos related to Mbappé's transfer (5 pre-transfer, 5 post-transfer) using a custom Python script.
2.  **Data Cleaning & Preprocessing**: Implemented a rigorous cleaning process, including deduplication, language filtering (French only), and removing irrelevant comments. The text was preprocessed by converting to lowercase, removing stop-words (using `stopwords-iso`), special characters, and performing lemmatization with NLTK.
3.  **Sentiment Analysis**: Utilized a pre-trained **CamemBERT** model from Hugging Face, specifically fine-tuned for French sentiment analysis (`ac0hik/Sentiment_Analysis_French`), to classify comments as positive, negative, or neutral.
4.  **Topic Modeling**: Employed Latent Dirichlet Allocation (LDA) after vectorizing the text with TF-IDF to discover the underlying topics in the public discourse.
5.  **Data Visualization**: Used `Matplotlib` and `WordCloud` to create insightful visualizations, including sentiment distribution bars, time-series trend lines, and word clouds for positive/negative comments, to effectively present the findings.

## 📁 Repository Structure

* `data_collection/`: Contains the Jupyter notebook (`YouTube scraping.ipynb`) for scraping YouTube comments.
* `data_cleaning/`: Notebook (`data_cleaning.ipynb`) for preprocessing and cleaning the collected text data.
* `sentiment_analysis/`: Notebook (`sentiment_analysis.ipynb`) that implements the sentiment analysis using the CamemBERT model.
* `topic_modelling/`: Notebook (`topic_modelling.ipynb`) for identifying key topics with LDA.
* `sentiment_visualization/`: Notebook (`sentiment_analysis_visualization.ipynb`) for generating all the charts and word clouds presented in the analysis.

## 🚀 How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Mathilda-aller/mbappe-nlp-sentiment-analysis.git](https://github.com/Mathilda-aller/mbappe-nlp-sentiment-analysis.git)
    cd mbappe-nlp-sentiment-analysis
    ```

2.  **Set up a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install dependencies:**
    This project requires Python and several key libraries. You can install them using pip.
    ```bash
    pip install pandas numpy jupyterlab nltk torch transformers
    pip install wordcloud matplotlib scikit-learn gensim stopwords-iso
    ```

4.  **Launch Jupyter Lab and run the notebooks:**
    ```bash
    jupyter lab
    ```
    You can then open and run the notebooks, preferably following the numerical order of the workflow (data collection -> cleaning -> analysis -> visualization).

---
*This project was completed as part of a computational linguistics course.*
