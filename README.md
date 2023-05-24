# Student-Records-Analysis-using-Machine-Learning
This project involves building a basic Data Engineering pipeline using various components. Here is a summary of the tasks involved:

Task 1 - Creating a Data Source - Databricks:

The project starts by uploading the "StudentData.csv" file and creating a table in Databricks to train the model.
The column data types are checked and verified.

Task 2 - Create a Kafka Producer - Google Colab:

A Kafka Producer is created in Google Colab to read the "unseenData.json" file and publish it to a topic.
The number of partitions for the topic is decided and created.
The data is published to the topic as a JSON string.

Task 3 - Train a model in PySpark and Save:

A classification model is trained in PySpark using the "AtRisk_academic" column as the target variable.
The model developed in Lab 4 can be used for this task.
The model is persisted by saving it, and then loaded for predicting on unseen data.
The ML pipeline is utilized for all operations, including StringIndexer and VectorAssembler.

Task 4 - Create a Kafka Consumer:

A Kafka Consumer is created in the PySpark coding environment to consume data from the created topic.
The data is consumed as a Spark DataFrame. To address issues with predicting for a single instance, the data is appended to a DataFrame.
Predictions are made for a batch size of 10.

Task 5 - Save the data onto a database:

The predicted data is saved in a database, preferably Atlas MongoDB service.
The selected columns for saving are "AtRisk_academic" and "prediction".
The pymongo library is used to connect to the database.

Task 6 - Display the data in Tableau:

The database is queried to retrieve the data, and the resulting table is displayed on a Tableau Dashboard.
