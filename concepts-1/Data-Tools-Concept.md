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
            #img3
    
    - `Fault Tolerance`
        - Spark achieves fault tolerance through data replication. `Resilient Distributed Datasets(RDDs)`,the fundamental data structure in spark,automatically recover lost data in case of node failures.

        - `RDDs` hides the complexity form users,who don't have to worry about defining where specific files are sent,what resource used to store and retrive files.
        #img1

        - process of RDDs is done by drivers and executors
        #img2

    - `Community and Ecosystem`
        - support docs and range of third party libraries and tools
        - it integrate with various data storage systems, including `HDFS`,`Apache Cassandra`

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