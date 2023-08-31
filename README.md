# Sentiment Analysis of NASDAQ Companies based on Tweets

## Project Overview

This project aims to conduct Sentiment Analysis (SA) on tweets related to NASDAQ companies. By utilising Big Data analytics tools, we processed a vast volume of Twitter data to gain initial insights into public perception regarding these companies. The sentiments extracted can potentially be correlated with stock market movements in future analyses.

## Requirements

- Python
- Pandas
- TextBlob
- Hadoop/AWS (for MapReduce operations)

## Steps to Reproduce

1. **Data Collection**: A large volume of tweets pertaining to NASDAQ companies is available on Kaggle.
2. **Data Cleaning**:
   - Wrote MapReduce that processes the Twitter data.
   - Removed URLs, user mentions, non-alphanumeric characters, and unnecessary whitespaces.
   - The output from this step serves as input for the next phase.
3. **Sentiment Analysis**:
   - Employed the TextBlob library for sentiment scoring.
   - Processed the cleaned tweets to determine sentiment (positive, neutral, or negative).
   - Utilised the AFINN-111 lexicon for sentiment scoring in the MapReduce job.
4. **Data Aggregation**: Used MapReduce to aggregate sentiment scores for each NASDAQ company based on the associated ticker symbols in the tweets.
5. **Visualisation**: Used Python (e.g., libraries such as Matplotlib, Seaborn) for visualisation of the sentiment analysis results. (Note: Though not demonstrated here, tools like Kibana can offer a different perspective and method for visualisation.)
6. **Results**: The results were saved and can be further analysed to see if any correlation exists between public sentiment and stock market movements.

## How to Run

1. Ensure you have all the necessary libraries and tools installed.
2. Set up your environment variables if required. For example, `CLEANED_TWEETS_PATH` if using the environment variable method for file paths.
3. Clone this repository: `git clone [YOUR REPO URL]`.
4. Navigate to the project directory: `cd [YOUR REPO NAME]`.
5. Run the scripts in the order of the steps mentioned above.

## Notes

- Remember to use relative paths or environment variables to avoid exposing personal details.
- If using other Big Data tools or platforms, ensure they are correctly set up and configured.
