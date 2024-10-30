# Sentiment Analysis on NASDAQ Companies

## Project Overview

This project conducts **Sentiment Analysis (SA)** on over 4 million tweets related to NASDAQ companies. The goal is to gain insights into public perception using **Big Data tools** like **MapReduce**, **Hadoop**, and **AWS** for distributed processing. In future extensions, the sentiment data can be correlated with stock market movements.
![X](https://github.com/drnsmith/sentiment-analysis-NASDAQ-companies-Tweets/blob/main/X.png?raw=true)


## Requirements

- **Python**: Core language used for data analysis.
- **Pandas**: For data manipulation and cleaning.
- **TextBlob**: For performing sentiment analysis.
- **Hadoop/AWS**: Used for large-scale **MapReduce** operations to process vast amounts of Twitter data.


## Tools & Technologies

### 1. **MapReduce**
   - **Role**: MapReduce allows to efficiently distribute the task of cleaning, tokenising, and analysing sentiment across multiple nodes.
   - **Reason**: It is essential when working with large datasets (4 million+ tweets) to ensure scalability.
   
### 2. **Hadoop**
   - **Role**: A distributed file system to store the tweet data and perform MapReduce operations.
   - **Reason**: Hadoop ensures we can store large datasets in a scalable manner and process them efficiently.

### 3. **TextBlob**
   - **Role**: Provides sentiment analysis through the processing of cleaned tweets, assigning a sentiment score (positive, neutral, or negative).
   - **Reason**: TextBlob is simple to implement and provides a lexicon-based approach to sentiment analysis.

### 4. **AFINN-111 Lexicon**
   - **Role**: This sentiment lexicon was used in our MapReduce jobs to score tweets based on positive and negative words.
   - **Reason**: AFINN is optimised for short texts like tweets, making it ideal for this project.

### 5. **Matplotlib and Seaborn**
   - **Role**: These Python libraries were used for data visualisation to present the sentiment distribution across different NASDAQ companies.
   - **Reason**: They provide flexible and powerful tools for creating clear, concise visualisations.
   
   _Note_: Tools like **Kibana** can also be used for dynamic, real-time visualisation, though not demonstrated in this version.

## Steps to Reproduce

1. **Data Collection**: 
    - We used a dataset of NASDAQ-related tweets available on Kaggle.
    - Collected using the Twitter API, with relevant filters applied to gather company-related discussions.

2. **Data Cleaning**:
    - Implemented **MapReduce** jobs to process the raw Twitter data. 
    - Removed URLs, user mentions, special characters, and unnecessary whitespaces.
    - The cleaned data served as input for the sentiment analysis.

3. **Sentiment Analysis**:
    - We employed the **TextBlob** library to assign sentiment scores (positive, neutral, negative).
    - For MapReduce operations, the **AFINN-111 lexicon** was used to compute sentiment scores on a large scale.

4. **Data Aggregation**:
    - **MapReduce** was used again to aggregate sentiment scores by NASDAQ company.
    - The result is an overview of the general public's sentiment toward each company.

5. **Visualisation**:
    - Used **Matplotlib** and **Seaborn** for basic visualisations of the sentiment trends.
    - The visualisations show sentiment distribution and could be further extended with tools like **Kibana**.

6. **Results**:
    - The sentiment results are saved for future analysis.
    - Next steps could include correlating sentiment with stock prices.

## How to Run

1. **Setup Environment**:
    - Ensure all required libraries (listed above) are installed.
    - Set up environment variables like `CLEANED_TWEETS_PATH` if using relative paths.

2. **Clone the Repository**:
    ```bash
    git clone [YOUR REPO URL]
    ```

3. **Navigate to the Project Directory**:
    ```bash
    cd [YOUR REPO NAME]
    ```

4. **Run the Scripts**:
    - Follow the steps outlined in the sections above for each phase (data collection, cleaning, sentiment analysis, and visualisation).

## Notes

- Ensure Hadoop/AWS is properly set up to run the MapReduce jobs.
- Use environment variables to store sensitive data (API keys, file paths) to avoid exposure in public code.

## Prerequisites
Python 3.x: Ensure Python is installed.
Dependencies: Install the required libraries listed in requirements.txt by running the following command:
pip install -r requirements.txt

## Contributing

Contributions are welcome! If you have ideas or improvements:
1. Fork the project.
2. Create a feature branch:
    ```bash
    git checkout -b feature/AmazingFeature
    ```
3. Commit your changes:
    ```bash
    git commit -m 'Add some AmazingFeature'
    ```
4. Push to the branch:
    ```bash
    git push origin feature/AmazingFeature
    ```
5. Open a pull request.

## Notes

- Remember to use relative paths or environment variables to avoid exposing personal details.
- If using other Big Data tools or platforms, ensure they are correctly set up and configured.

## Acknowledgments

This project was a collaborative effort between Nat Smith and Elaheh Bastani. We would like to acknowledge each other’s contribution in designing, implementing, and executing the entire pipeline, from data collection and cleaning to sentiment analysis and visualisation.

Both of us were involved equally in:
- Data preprocessing and cleaning
- Writing and optimising MapReduce jobs
- Sentiment analysis using TextBlob and AFINN-111 lexicon
- Data aggregation, visualisation, and result interpretation

Our complementary skills made this project a success.


## License
Distributed under the MIT License. See `LICENSE` for more information.

# Building a Big Data Pipeline for Twitter Sentiment and Topic Analysis

As the world becomes more digital, organisations seek insights from large datasets. 
Social media platforms like Twitter offer a wealth of real-time, user-generated data, making them valuable sources for sentiment and topic analysis. 
This blog explores the end-to-end process of building a data pipeline to collect, process, and analyze Twitter data, utilising big data tools like Hadoop, Hive, Elasticsearch, and Kibana.

## Project Overview

Our project aims to ingest, transform, and analyze Twitter data for sentiment and topic trends. 
We use distributed data technologies to process millions of tweets, classify sentiments, and detect popular topics. 
By combining multiple tools and techniques, we created a pipeline that delivers both quantitative and qualitative insights, 
which can be leveraged in domains like business, politics, and customer feedback.

## Setting Up the Data Pipeline: Step-by-Step

An overview of each component in our big data pipeline:

### 1. Data Collection
   - We collected a large dataset of tweets. Twitter's APIs provide options for streaming tweets in real-time or fetching historical data based on specific keywords or user accounts.
   - To handle large-scale data collection, we deployed our data ingestion on **AWS EC2** instances, leveraging AWS's scalability to ensure data collection could handle spikes in volume.

### 2. Data Ingestion and Storage
   - **Hadoop**: We chose Hadoop’s HDFS for distributed storage, allowing for efficient handling of massive data volumes. Each tweet was stored as a structured JSON document containing metadata (like date and user ID) and text data for analysis.
   - Using Hadoop made it possible to process the data in parallel, distributing the workload across multiple nodes and minimizing latency.

### 3. Data Processing with Hive
   - To analyse the data effectively, we used **Hive**, a SQL-like interface built on top of Hadoop, which allowed us to query our data and create a structured dataset.
   - **Tokenisation and Cleaning**: Using Python and NLTK libraries, we cleaned each tweet by removing URLs, mentions, hashtags, and punctuation. Text was tokenized, and stop words were filtered to reduce noise.
   - **Sentiment and Topic Classification**: We performed sentiment analysis to classify tweets as positive, negative, or neutral. For topic analysis, we used Natural Language Processing (NLP) techniques to identify key themes. By creating Hive tables with sentiment and topic labels, we could easily query and summarize these results.

### 4. Data Storage and Indexing with Elasticsearch
   - **Elasticsearch** offered a scalable, near-real-time search and analytics engine, ideal for exploring our Twitter data.
   - After data was cleaned, structured, and analyzed, we indexed it in Elasticsearch, providing fast access to query the data for various insights.

### 5. Visualisation with Kibana
   - We used **Kibana**, an open-source visualisation tool, to display our analysis results. Kibana integrates directly with Elasticsearch, enabling us to create interactive dashboards for trend analysis and detailed exploration of sentiment changes over time.
   - **Building Interactive Dashboards**: With dashboards, we visualised topics, sentiment distribution, and temporal trends, allowing stakeholders to easily identify shifts in public opinion and prominent topics in real time.

## Key Takeaways

### 1. Sentiment Analysis Using Hive
Using Hive’s SQL capabilities on top of HDFS allowed us to perform data manipulation and analysis efficiently. 
The sentiment analysis involved aggregating data based on keywords, sentiment scores, and timestamps. 
This setup provided valuable insights into user sentiment patterns on Twitter, showcasing Hive's capabilities for big data analytics.

### 2. Topic Modeling and NLP
Topic modelling was instrumental in identifying trends. We used NLP techniques to classify and categorise tweets, unveilling user concerns, interests, and behaviors. By implementing machine learning models (e.g., LDA or Latent Dirichlet Allocation) in a big data context, we could efficiently extract topics from vast amounts of text.

### 3. Elasticsearch for Quick Retrieval
With a high volume of incoming tweets, Elasticsearch proved valuable in storing, searching, and retrieving data with minimal latency. Its inverted index structure allowed us to conduct fast searches, making it perfect for time-sensitive applications like social media analysis.

### 4. Data Visualization with Kibana
Kibana allowed us to represent the data visually, highlighting trends and patterns that might otherwise go unnoticed. With charts and interactive dashboards, our sentiment and topic analysis results were accessible and actionable for end-users.

## Challenges Faced

1. **Scalability**: Managing and processing high-volume Twitter data required careful scaling, which AWS facilitated.
2. **Data Quality**: Noise and inconsistencies in raw tweet text made cleaning and preprocessing a crucial but time-consuming task.
3. **Real-Time Processing**: To achieve near-real-time results, we optimized our indexing and retrieval processes in Elasticsearch.

## Conclusion

This project demonstrates the power of big data tools for transforming vast amounts of unstructured text data into meaningful insights. By leveraging Hadoop, Hive, Elasticsearch, and Kibana, we developed a scalable and robust pipeline for real-time social media analysis. Whether used for customer feedback, trend analysis, or political sentiment monitoring, this pipeline showcases a comprehensive approach to making sense of social media data.

This project provides a foundational approach to big data processing with applications extending across industries, especially where rapid analysis and visualisation of user-generated content are essential.


