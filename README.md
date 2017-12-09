# Spark-BIG-data-processing
Data exploration and Analysis using Spark standalone version. Spark replaces Map reducer as data processing unit and still uses Hadoop HDFS for data storage.

Spark run programs up to 100x faster than Hadoop MapReduce, using its in-memory computing capabilities (RDD).
It comes with built-in libraries to work with structure data (Spark SQL), machine learning (MLlib) and streaming (Spark Streaming).

Spark - built using Scala
- An engine for data processing and analysis.
- Data is processed using Resilient Distributed Datasets (RDD).
- RDDs are in-memory collections of objects (collection of entities).
- Each object in the colletion represent one record in the dataset.
- RDDs are in-memory, yet resilient (tolerent to faults and crashes).

- With RDDs, you can interact and play with billions of rows of data without caring about any of the complexities.

### Components of Spark:
- Data processing unit / Spark Core - is a computing engine which deals with creation and processing of RDDs
- Data Storage unit 
			- that stores the data to be processed.
			- You can either chose 
				1. local file system (stand alone mode) 
				2. - HDFS if you are integrating with Hadoop.
- Cluster manager 
			- that helps Spark run tasks and schedule task across cluster.
			- You can either use  
				1. Spark's built-in Cluster manager for local file system (stand alone mode)
				2. - plug-in YARN if you are integrating with Hadoop.


### Characteristics of RDD:
- Partitions in to multiple nodes / machines. runs in parallel.
- Readonly / Immutable - 
- Lineage
- Resilience / Fault tolerant

### Types of operations on RDD:
- Transformation - transform into another RDD. for ex, filtering, extracting, sorting etc. each of these operations convert from one RDD to another RDD.	
- Action - request a result. For ex, request top 10 rows, request for SUM etc.
