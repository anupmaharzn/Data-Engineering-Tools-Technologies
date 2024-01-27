# Big Data Tools Conceptual Overview

## Apache Spark

- Apache Spark is fast and general-purpose engine for large-scale data processing.

- Feature of spark

    - `speed`
        - In-Memory Processing
            - spark processes data in-memory,allowing it to perform operations much faster than Hadoop that relies on disk storage type for data processing
        - Distributed Computing
            - enabling parallel processing across a cluster of machines
    
    - `Ease of use`
        - Unified API
            - Spark provides a unified API for batch processing,interactive queries,streaming and machine learning.
        - Support for multiple Languages
            - like Scala,Java,Python(PySpark),R
        
            ![bigdata3](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/93c7a218-f1d3-44e8-896b-43890b01b952)

    
    - `Fault Tolerance`
        - Spark achieves fault tolerance through data replication. `Resilient Distributed Datasets(RDDs)`,the fundamental data structure in spark,automatically recover lost data in case of node failures.

        - `RDDs` hides the complexity form users,who don't have to worry about defining where specific files are sent,what resource used to store and retrive files.
          
        ![bigdata1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/3b3f6d36-3c1a-4fe2-94a1-1f4f27c5e840)

        - process of RDDs is done by drivers and executors
          
        ![bigdata2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/e910d876-3218-4ab1-ad60-2a1862d65498)

    - `Community and Ecosystem`
        - support docs and range of third party libraries and tools
        - it integrate with various data storage systems, including `HDFS`,`Apache Cassandra`
     
- `Overview Architecture Of Apache Spark`

![bigdata4](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/ab1b2639-8d82-4b5a-957b-df8737d8ac47)


- `Why Spark Performs Better than Hadoop ?`

    - Spark run programs up to 100 times faster than Hadoop MapReduce when running `in memory`, or 10x faster when running on disk.

    - It has an advanced DAG execution engine that supports acyclic data flow and in-memeory execution

    - Spark's goal was not to repalce the MapReduce paradigm but to replace Hadoop's implementation of it with it's faster and efficient one.

    - Resource Management 
        - While using hadoop,when you want to run a MapReduce job, you need to have a Hadoop Cluster to execute it.It uses `YARN` for resource management. the application in hadoop negotiates with yarn to get the resource it requires for execution.
        - On the toher had, sparks comes with `in-built` resource management so it doesn't require `YARN` for managing cluster, nodes and memory.

- `What problem Spark tires to address?`

    - `Iterative processing`
        - It refers to executing a MapReduce job multiple times or in simple terms iterating through the data sets multiple times to get the desired output. Graph processing algorithms, Page Ranking and Logistic Regression are some of the examples of iterative data mining and machine learning algorithms.
        - In Hadoop, when we write a MapReduce job, in each iteration it will read data from the disk and write temporary data back to the disk. So the problem here is that reading the initial data and writing the intermediate output data back to the disk is unavoidable because you have to save this temporary data somewhere. The more intermediate data you read/write the slower your execution will be.
        - `Spark optimizes this by keeping intermediate data in memory instead of disk.` 


## Spark SQL

- Spark SQL is a module in Apache Spark that provides a programming interface for working with structured and semi-structured data using SQL.
- Spark SQL introduces the Dataframe API, which is higher-level abstraction than the traditional Resilient Distributed Dataset(RDD).DataFrames represent distributed collections of data organized into named columns,similar to tables in a relational database.

## PySpark

- PySpark is the Python API for Apache Spark,allowing to interact with the Spark framework for distributed data processing.
- PySpark provies a module for `Spark SQL`, allowing users to perform SQL queries on structured data using Python.

- PySpark supports `Dataframes`,a distributed collection of data organized into named columns. Dataframes provides a higher-level abstraction than `RDDs` and integrate well with `SparkSQL`.


## Databricks

- Databricks is cloud-based platform for working with Spark that provides automated cluster management and IPython-style notebooks.

- Databricks is built on top of Apache Spark, leveraging its capabilities for distributed data processing, machine learning, and graph processing.