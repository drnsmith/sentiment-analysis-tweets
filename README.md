# Sentiment Analysis of NASDAQ Companies based on Tweets

## Project Overview

This project aims to conduct Sentiment Analysis (SA) on tweets related to NASDAQ companies. We processed over 4 mllion Twitter data to gain initial insights into public perception regarding these companies. We show how this can be done more effectively utilising Big Data tools (Mapreduce/Hadoop/AWS). The sentiments extracted can potentially be correlated with stock market movements in future analyses.
![X] https://raw.githubusercontent.com/drnsmith/sentiment-analysis-NASDAQ-companies-Tweets/main/X.avif?token=GHSAT0AAAAAACGLJXNVYPBGGXJ6XCF7KCSKZHRGEYA

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


## Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
Distributed under the MIT License. See `LICENSE` for more information.
