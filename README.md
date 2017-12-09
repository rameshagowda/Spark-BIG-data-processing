# Spark-BIG-data-processing
Data exploration and Analysis using Spark standalone version. Spark replaces Map reducer as data processing unit and still uses Hadoop HDFS for data storage.
### Key issue with HADOOP and How Spark solves it:
Hadoop has 3 components
- HDFS -  storing large amount of data
- YARN for managing computational resources across multiple nodes in the cluster for distibuted computing and scheduling algorithms in the cluster in most optimal way (Cluster manager).
- Map Reduce - The only limitations in Hadoop is it's map reduce layer, which is not designed well for multi-stage and iterative algorithms.
The way map reduce is desinged on hadoop is the maps read data from HDFS, send to reducers and reducers write the result back to HDFS. Reading and writing to a file system, which ultimately write to disk, make processing extremely slow.
The other key issues was Map Reduce on Hadoop is not designed for interactive / stream processing. It is primarily designed for batch processing.

### Spark has only data processing unit, but does not have storage and Cluster Management components of its own.Spark is designed to integrate well into HDFS and YARN layer.

Spark run programs up to 100x faster than Hadoop MapReduce, using its in-memory computing capabilities (RDD).
It comes with built-in libraries to work with structure data (Spark SQL), machine learning (MLlib) and streaming (Spark Streaming).

Spark - built using Scala, possible to write Spark applications using Java, Python, Scala and R.
- An engine for data processing and analysis.
- Data is processed using Resilient Distributed Datasets (RDD).
- RDDs are in-memory collections of objects (collection of entities).
- Each object in the colletion represent one record in the dataset.
- RDDs are in-memory, yet resilient (tolerent to faults and crashes).

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

### Install and Configure Spark on Windows 10. Follow these links.
https://hernandezpaul.wordpress.com/2016/01/24/apache-spark-installation-on-windows-10/
https://simonsuthers.wordpress.com/2017/02/13/how-to-install-spark-on-a-windows-10-machine/
