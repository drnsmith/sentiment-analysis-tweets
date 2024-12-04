### Big Data Sentiment Analysis: Hadoop, Hive, and NLP for NASDAQ Companies

This project leverages Big Data technologies and Natural Language Processing (NLP) to analyse over 4 million tweets related to NASDAQ-listed companies. Using tools like **Hadoop**, **Hive**, and **MapReduce**, combined with sentiment analysis libraries like **TextBlob**, we extract actionable insights into public perception. The results provide a foundation for correlating social media sentiment with financial market trends, offering value to investors, analysts, and businesses.

---

#### **Motivation**

Understanding public sentiment can provide critical insights into brand reputation, customer satisfaction, and even market behavior. For NASDAQ-listed companies, real-time social media data serves as a valuable resource to:
- **Gauge Public Opinion**: Understand how products, services, or announcements are perceived.
- **Monitor Brand Reputation**: Track changes in sentiment over time.
- **Predict Market Trends**: Lay the groundwork for correlating sentiment with stock market performance.

---

## **Features**

1. **Big Data Processing**:
   - Utilized **Hadoop** for distributed storage and **Hive** for querying structured datasets at scale.
   - Designed efficient **MapReduce** jobs for cleaning, tokenizing, and analyzing large datasets.

2. **Sentiment Analysis**:
   - Employed **TextBlob** and **AFINN-111 Lexicon** for sentiment classification (positive, neutral, negative).
   - Integrated advanced NLP techniques to enhance accuracy.

3. **Dynamic Visualisation**:
   - Generated meaningful insights through visual tools like **Kibana**, **Matplotlib**, and **Seaborn**.
   - Explored sentiment trends and their implications on market dynamics.

4. **Scalable Pipeline**:
   - Designed a robust pipeline for real-time data processing and sentiment scoring.
   - Adaptable for larger datasets and advanced predictive analytics.

---

## **Technologies Used**

| **Category**      | **Tools & Frameworks**                                     |
|--------------------|-----------------------------------------------------------|
| **Big Data**       | Hadoop, Hive, MapReduce, AWS                              |
| **Programming**    | Python, Java                                              |
| **NLP**            | TextBlob, NLTK, Vader, AFINN-111 Lexicon                  |
| **Visualisation**  | Kibana, Matplotlib, Seaborn                               |
| **Data Handling**  | Pandas, NumPy                                             |

---

## **Pipeline**

1. **Data Collection**:
   - Aggregated tweets from public datasets or APIs using company-related hashtags and mentions.
   - Stored raw data in a Hadoop Distributed File System (HDFS).

2. **Data Cleaning**:
   - Applied **MapReduce** jobs to remove noise (e.g., URLs, special characters).
   - Structured data for analysis using **Hive**.

3. **Sentiment Scoring**:
   - Processed tweets with **TextBlob** and **AFINN** to classify sentiments.
   - Output sentiment scores for each company.

4. **Query and Aggregation**:
   - Used **Hive** to run queries on structured datasets and extract insights.
   - Aggregated results to display sentiment trends across companies.

5. **Visualisation**:
   - Visualised sentiment distributions and trends using **Kibana**, **Matplotlib**, and **Seaborn**.

---

## **How to Run**

1. **Prerequisites**:
   - Install Hadoop and Hive on your local system or set up AWS for distributed processing.
   - Install Python 3.x and required libraries (`requirements.txt`).

2. **Clone the Repository**:
   ```bash
   git clone https://github.com/YOUR-USERNAME/Big-Data-Sentiment-Analysis
   cd Big-Data-Sentiment-Analysis
   ```

3. **Set Up Hadoop & Hive**:
   - Configure HDFS for data storage.
   - Import cleaned datasets into Hive for querying.

4. **Run Sentiment Analysis**:
   - Execute MapReduce jobs for data cleaning and sentiment scoring:
     ```bash
     hadoop jar sentiment-analysis.jar input_path output_path
     ```

5. **Query Results**:
   - Use Hive to query aggregated sentiment data.

6. **Visualise**:
   - Generate visualisations with Python scripts.

---

## **Challenges**

1. **Data Quality**:  
   Cleaning noisy social media data required extensive pre-processing.
   
2. **Scalability**:  
   Managing over 4 million tweets tested the system’s capacity, requiring optimised MapReduce and Hive queries.
   
3. **Real-Time Processing**:  
   Future versions aim to implement real-time sentiment tracking using tools like **Apache Kafka**.

---

## **Contributing**

Contributions are welcome! If you'd like to improve this project:
1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feature/YourFeatureName
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add YourFeatureName"
   ```
4. Push your branch:
   ```bash
   git push origin feature/YourFeatureName
   ```
5. Open a pull request!

---

## **License**

Distributed under the MIT License. See `LICENSE` for more details.

---

### **Acknowledgments**

This project was a collaborative effort led by **Natasha Smith** and **Elaheh Bastani**, leveraging expertise in Big Data, NLP, and data visualization.

For inquiries, connect on [LinkedIn](https://www.linkedin.com/in/YOUR-LINKEDIN).



