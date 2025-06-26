# Kylian Mbappé Transfer Saga: A NLP Analysis of Fan Sentiment

This project analyzes the sentiment of football fans regarding the Kylian Mbappé transfer saga by scraping and analyzing YouTube comments from videos related to Real Madrid and PSG.

## Project Structure

-   **/data_collection**: Contains the Jupyter notebook (`YouTube scraping.ipynb`) for scraping YouTube comments.
-   **/data_cleaning**: Notebook (`data_cleaning.ipynb`) for preprocessing and cleaning the collected text data.
-   **/sentiment_analysis**: Implements sentiment analysis using VADER. The notebook and results are stored here.
-   **/topic_modelling**: Identifies key topics discussed in the comments using techniques like LDA.
-   **/sentiment_visualization**: Visualizes the sentiment analysis results.

## How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/mbappe-nlp-sentiment-analysis.git](https://github.com/your-username/mbappe-nlp-sentiment-analysis.git)
    cd mbappe-nlp-sentiment-analysis
    ```

2.  **Install dependencies:**
    It's recommended to create a virtual environment first.
    ```bash
    pip install pandas numpy jupyterlab nltk vaderSentiment scikit-learn gensim
    ```

3.  **Run the notebooks:**
    You can run the Jupyter notebooks (`.ipynb`) in numerical order, starting from data collection and cleaning.

