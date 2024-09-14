# Sentiment Analysis on NASDAQ Companies

## Project Overview

This project conducts **Sentiment Analysis (SA)** on over 4 million tweets related to NASDAQ companies. The goal is to gain insights into public perception using **Big Data tools** like **MapReduce**, **Hadoop**, and **AWS** for distributed processing. In future extensions, the sentiment data can be correlated with stock market movements.
![X](https://raw.githubusercontent.com/drnsmith/sentiment-analysis-NASDAQ-companies-Tweets/main/X.png)

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




