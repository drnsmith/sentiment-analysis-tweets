# sentiment-analysis-tweets

### In this project, the power of Hadoop's distributed computing was harnessed to analyse vast Big Twitter data related to major tech companies (i.e., Apple, Amazon, Google, Microsoft and Tesla). Our goal was to dive deep into the sentiments of millions of tweets to understand public perception these companies.

## Key steps of the project:
### Data Ingestion: 
Using Hadoop's ecosystem, a CSV file containing tweets was ingested into the Hadoop Distributed File System (HDFS).

### Data Preprocessing with MapReduce: 
To cleanse and structure the data, MapReduce jobs were executed. These jobs filtered out noise like URLs, special characters, and numbers, ensuring a pure textual sentiment analysis.

### Sentiment Analysis with Python's TextBlob:
 - Employed TextBlob's sentiment analysis capabilities to allocate sentiment scores to every tweet.
 - Classified tweets as positive, negative, or neutral grounded on these scores.

### Visualisation and Insight Extraction with Python's Matplotlib: 
The processed data were then exported from HDFS to be visualised. This step:
- Generated plots like word clouds and bar charts depicting sentiment distribution.

## Final Observations and Implications:
Utilising the vast potential of Hadoop combined with the precision of TextBlob, we delved into the public's perception of leading tech corporations. This kind of deep dive provides insights that are useful for a variety of audiences, from curious investors to the very companies being discussed. Hadoop's distributed framework ensured smooth processing of our extensive dataset, emphasising the critical role of big data solutions in today's data-intensive era.
