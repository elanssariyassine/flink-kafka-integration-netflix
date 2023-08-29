# flink-kafka-integration-netflix
The purpose of this Project is to know how netflix uses the cluster combination kafka with apache flink for streaming and processing data in Real Time  through the realization of diagram below :
* ![](https://github.com/elanssariyassine/flink-kafka-integration-netflix/blob/main/Architecture.png)
# About The Project
Netflix employs multiple Kafka clusters to generate streaming data originating from various sources. This data is then transformed using the Apache Flink distributed processing engine, after which consumers will consume this processed data.

* In summary, there are three parts:
Part 1: Generation of data from various sources by Kafka clusters.
Part 2: Flink performs ETL (Extract, Transform, Load): extracting data from Kafka, then transforming it, and finally loading it back into Kafka.
Part 3: Consumption and utilization of this data by other data engines
**We will implement this scheme through 3 Java classes:**
- Flink_Kafka_Receiver.java: In this class, Flink will act as a consumer of data coming from Kafka.
- Flink_Kafka_Sender.java: In this class, Flink will act as a producer of data to Kafka.
- Flink_Kafka_Receiver_Sender.java: This class represents the implementation of the overall schema, such as the uppercase transformation.

* I utilized 2 topics for this Project:
The first topic is meant for data coming from various sources, and the second one is for data sent by Flink after the transformation.
Data Source: Default Kafka Producer.
Project Type: Maven, to work with Flink and Kafka APIs, along with JARs to establish the connection between Flink and Kafka.

