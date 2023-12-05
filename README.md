# Power Real Time Chat Toxicity
This project repository is created in partial fulfillment of the requirements for the Big Data Analytics course offered by the Master of Science in Business Analytics program at the Carlson School of Management, University of Minnesota

# Introduction
 Across all platforms that enable communication between individuals, there is the risk of unsafe or “toxic” messaging that harms others. While human moderation is often the key factor for intervention, automated models can be leveraged to intercept toxic messaging in real-time to secure the safety of platforms. Nowhere is this more applicable than in the world of video games, where intense competition can bring out the worst in players.

Using the Databricks platform, we can train a model to detect toxic messages using MLflow, incorporate streaming data using Delta Lake and Spark, process the textual data using SparkNLP, and deploy such a model to monitor toxic messages in real time. Using a big data platform like Databricks ensures this architecture scales with the growth of the game and with other types of data, like voice and video chat. Stopping toxicity increases player retention and makes a safer, more fun environment for all players.

# Data Set
#### Surge AI Social Media Comments
Provided by Surge AI, the world's most powerful NLP data labeling platform and workforce.
This dataset contains 500 toxic and 500 non-toxic comments from a variety of popular social media platforms. The toxicity texts are labeled with "toxic" or "not toxic", we will utilize the labeled data to train our NLP model with John Snow Lab for toxic behavior detection.

Source: https://github.com/surge-ai/toxicity/blob/main/toxicity_en.csv

#### Dota 2 
Dota 2 is a multiplayer online battle arena (MOBA) video game in which two teams of five players compete to destroy a large structure defended by the opposing team known as the "Ancient" whilst defending their own.
This dataset is originated from Kaggle contest - Dota 2 Matches, containing 50000 ranked ladder matches from the Dota 2 data dump created by Opendota. We would use this dataset to demonstrate Databricks Delta Lake storage and apply our NLP classification model to predict 144k game chat toxicity classification.

Source: https://www.kaggle.com/datasets/devinanzelmo/dota-2-matches

# Environment Configuration
To run the demo notebook, make sure the cluster supports Spark NLP. We are using below config version in the cluster 

Databrick Runtime Version: 14.2 ML (includes Apache Spark 3.5.0, Scala 2.12)

Additional Spark Config:
- spark.kryoserializer.buffer.max 2000M
- spark.serializer org.apache.spark.serializer.KryoSerializer

Install Libraries:
- PyPi: spark-nlp==5.1.4
- Maven Coordinates: com.johnsnowlabs.nlp:spark-nlp_2.12:5.1.4

# Data Workflow
<img width="804" alt="截圖 2023-12-04 下午7 19 16" src="https://github.com/YenChenHsu/Power_Real_Time_Chat_Toxicity/assets/57134574/e9605707-ff75-4339-b94d-95f182301241">

# NLP Pipeline
<img width="804" alt="截圖 2023-12-04 下午7 19 48" src="https://github.com/YenChenHsu/Power_Real_Time_Chat_Toxicity/assets/57134574/64fca9e8-99b5-4d73-8108-b13bcfd0e51f">

# Link
- Video [https://youtu.be/62H7PHu7ZNg]
- Dota 2 data set [https://drive.google.com/drive/folders/1opGHCa9Tsg-AS4QE6vyS9i_2dj8KkGV2?usp=sharing]

# Contributors
Mike Jiang, Shivani Vats, Thomas Farrell, Priyanka Prashanth Kumar, Yen Chen Hsu

