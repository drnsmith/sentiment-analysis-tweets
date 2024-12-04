### Big Data Sentiment Analysis: Hadoop and NLP for NASDAQ Companies
As the world becomes more digital, organisations seek insights from large datasets. Social media platforms like Twitter offer a wealth of real-time, user-generated data, making them valuable sources for sentiment and topic analysis. 
This project conducts **Sentiment Analysis (SA)** on over 4 million tweets related to NASDAQ companies. The goal is to gain insights into public perception using **Big Data tools** like **MapReduce**, **Hadoop**, and **AWS** for distributed processing, with the potential to correlate this data with stock market movements in future extensions.

---
#### **Motivation**
Social media platforms like Twitter have become powerful tools for understanding public opinion, making them a valuable resource for sentiment analysis and trend detection. For NASDAQ-listed companies, gauging sentiment can provide critical insights into how the public perceives their performance, products, and reputation.

This project was motivated by the following key factors:
1. **Real-Time Insights**:  
   Understanding public sentiment on Twitter can offer real-time feedback on events, campaigns, or announcements, allowing companies and investors to make timely decisions.

2. **Impact on Stock Performance**:  
   Public sentiment often influences stock prices. This project lays the groundwork for correlating social media data with market movements, enabling better predictive models for stock performance.

3. **Big Data Challenges**:  
   The immense volume of social media data requires advanced storage and processing solutions. This project demonstrates the use of distributed technologies like **Hadoop** and **MapReduce** to address these challenges.

4. **Practical Applications**:  
   Insights from sentiment analysis can be used by businesses, investors, and policymakers to:
   - Understand consumer behaviour.
   - Evaluate brand reputation.
   - Monitor industry trends.
   - Anticipate market shifts.

5. **Extensibility**:  
   The project serves as a foundational framework for:
   - Correlating sentiment with stock prices.
   - Applying advanced NLP techniques like transformer models.
   - Building real-time dashboards for live sentiment tracking.

---
### Key Takeaways
 - The project demonstrates the power of Big Data tools like Hadoop, Hive, and Elasticsearch for large-scale sentiment and topic analysis.
 - Sentiment scoring and topic modelling provided insights into public opinion and key trends in NASDAQ companies.
 - Visualisation with tools like Matplotlib, Seaborn, and Kibana enabled meaningful exploration of results.
 - By leveraging distributed data technologies, this project showcases a scalable approach to real-time social media analysis with applications across business, politics, and consumer feedback.

#### Challenges Faced
 - **Scalability:**
Managing high-volume Twitter data required careful scaling using AWS.
 - **Data Quality:**
Noise and inconsistencies in raw tweet data made cleaning a crucial but time-intensive step.
 - **Real-Time Processing:**
Optimising indexing and retrieval processes in Elasticsearch for near real-time results.

## Requirements

- **Python**: Core language used for data analysis.
- **Pandas**: For data manipulation and cleaning.
- **TextBlob**: For performing sentiment analysis.
- **Hadoop/AWS**: Used for large-scale **MapReduce** operations to process vast amounts of Twitter data.


## Tools & Technologies

1. **MapReduce**
   - **Role**: MapReduce allows to efficiently distribute the task of cleaning, tokenising, and analysing sentiment across multiple nodes.
   - **Reason**: It is essential when working with large datasets (4 million+ tweets) to ensure scalability.
   
2. **Hadoop**
   - **Role**: A distributed file system to store the tweet data and perform MapReduce operations.
   - **Reason**: Hadoop ensures we can store large datasets in a scalable manner and process them efficiently.

3. **TextBlob**
   - **Role**: Provides sentiment analysis through the processing of cleaned tweets, assigning a sentiment score (positive, neutral, or negative).
   - **Reason**: TextBlob is simple to implement and provides a lexicon-based approach to sentiment analysis.

4. **AFINN-111 Lexicon**
   - **Role**: This sentiment lexicon was used in our MapReduce jobs to score tweets based on positive and negative words.
   - **Reason**: AFINN is optimised for short texts like tweets, making it ideal for this project.

5. **Matplotlib and Seaborn**
   - **Role**: These Python libraries were used for data visualisation to present the sentiment distribution across different NASDAQ companies.
   - **Reason**: They provide flexible and powerful tools for creating clear, concise visualisations.
   
   _Note_: Tools like **Kibana** can also be used for dynamic, real-time visualisation, though not demonstrated in this version.

#### Pipeline: Steps to Reproduce

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

#### How to Run

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

#### Notes

- Ensure Hadoop/AWS is properly set up to run the MapReduce jobs.
- Use environment variables to store sensitive data (API keys, file paths) to avoid exposure in public code.

#### Prerequisites
 - Python 3.x: Ensure Python is installed.
 - Dependencies: Install the required libraries listed in requirements.txt by running the following command:
```bash
pip install -r requirements.txt
```

- Remember to use relative paths or environment variables to avoid exposing personal details.
- If using other Big Data tools or platforms, ensure they are correctly set up and configured.

### Acknowledgments and Contributing

This project was a collaborative effort between Natasha Smith and Elaheh Bastani. We would like to acknowledge each other’s contribution in designing, implementing, and executing the entire pipeline, from data collection and cleaning to sentiment analysis and visualisation. Our complementary skills made this project a success.
Contributions are welcome! If you have ideas or improvements to share, please follow these steps:

1. **Fork the Repository:**
Create your own copy of the repository by clicking the "Fork" button at the top right of this page.

2. **Create a Feature Branch:**
Work on your changes in a dedicated branch.

```bash
git checkout -b feature/YourFeatureName
```
3. **Commit Your Changes:**
Write clear and concise commit messages explaining what you’ve done.

```bash
git commit -m "Add YourFeatureName"
```
4. **Push Your Changes**:
Push your feature branch to your forked repository.
```bash
git push origin feature/YourFeatureName
```
5. **Open a Pull Request**:
Submit your changes to the main repository by opening a pull request (PR). Ensure your PR description explains your changes clearly.

6. **Review and Feedback**:
We will review your PR and may suggest improvements before merging it into the main branch.

Thank you for your interest in contributing!

### License
Distributed under the MIT License. See `LICENSE` for more information.


