# Google File System(GFS) and Hadoop Distributed File System (HDFS)



## Google File System 

- `Distributed File Storage``, at any given cluster (1cluster = 100s of commodity servers) and this cluster provide an interface to n number of client to either read a file or write a file.
- it's basically a file system but distruted among 100 or 1000's of servers or more.

### Design Consideration
- Commodity Hardware
    - commodity servers are cheap and can be made to scale horizontally with right software(failure are common:disk/network/server,OS bugs,Human errors)
- Large File
- File Operations
    - Read + Append only
        - No random writes
        - Mostly sequential reads
- Chunks
    - Files split into chunks
        - each chunk of 64mb
        - identified by 64 bit ID (globally unique)
        - Stored in Chunkservers
    #img
- Replicas
    - Files split into chunks so
        - Replica count by client ( at least 3 replica of each chunks in 3 different servers)

-Let's understand with image
![google file system 1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/946766d7-672b-442d-a86e-ba90ec5711b8)

![google file system 2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/a42f2171-d587-43de-82e6-626c5d5bf209)

![google file system 3](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/1f9fafdb-a7d9-41b1-9b86-406221f19974)

- GFS master Metadata
![google file system 4](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/cc06bc0c-cf3f-4332-b6cf-cc51bcfbc766)

![google file system 5](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/31124a89-96d9-456c-a9d6-3a52eeb1bd15)

![google file system7](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/df00c497-9153-4875-8904-6e1daedd98dc)

```Note:Client interact with master to only get metadata```




### MapReduce (GFS continued)

- MapReduce is a programming model and an associated implementation for processing and generating big dataset with a parellel,distributed algorithm on a cluster.

- It provides a scalable and fault-tolerant approach to processing large datasets in parallel across a distributed cluster of computers. 

- lets understand this with Use-Case.

- Google Music analytics stored in GFS
    - Write progem to find which song was played how many times.
    - simple way to do that.
        ![mapreduce1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/fa0bab17-be0c-4b8d-8b3c-d06d61a0cdf7)
    - but problem statements
        ![mapreduce2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/c23efb7f-b790-45ac-a7a9-151d76a68121)
    - solution
        - step 1
        ![mapreduce3](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/418636ea-9b99-4b8c-83c5-9923301787de)
        - step 2
        ![mapreduce4](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/fc45e2f4-54e1-4e56-ba68-1fab467c77d4)
        - step 3
        ![mapreduce5](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/c092e2af-3a67-4c86-85ec-c996fafa9d86)
        - step 4
        ![mapreduce6](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/61620c5c-d8c8-45d3-b459-ef09a9618f37)


- WorkFlow of MapReduce
    - step 1
      ![mapreducestep1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/c817c8c9-5f0a-40b2-9361-2934740dc990)

    - step 2
      ![mapreducestep2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/f536a34e-4218-4e77-ae52-99a2d381c599)

    - step 3
      ![mapreducestep3](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/0510561d-2250-4a24-86e9-be39db6c4ada)

    - step 4
      ![mapreducestep4](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/f327253d-b08e-45b1-b806-1fd67c20b8c5)

    - step 5
      ![mapreducestep5](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/95e26cc0-0b3e-4e67-8345-b3fcf300003b)

    - step 6
      ![mapreducestep6](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/6f831809-b536-4183-866f-00ae01bbb3e4)
      
    - step 7
      ![mapreducestep7](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/7b2d0547-4472-481e-9c61-baa651aba791)


### MapReduce General Overview

![generaloverview1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/f75fd8d6-0d0c-4315-a94c-07dc4f921734)

- key points to note:
    - Distributed File system
        - meaning we got large dataset that are splited into chuck and these chunks are replicated and sperated out across 100's or 1000's of machince.(also has central controller)
  - No Data Movement (we send map program to the data)
  - key-value structure
  - Handle machine failure(re performs the map function and reduce function by central controller)
  - Idempontent(output doesnot changed despite of how many time we perform map and reduce function)

- Example of Word Count on Text file
![generaloverview2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/fca9be87-8a14-452a-bed8-2a2a437a91af)


## Hadoop Distributed File System


### Hadoop (AKA Apache Hadoop)
- Hadoop is an oen source framework from apache and is used to store process and analyz data which are very huge in volume.

- It is designed to handle massive amount of data and provide a scalable,fault-tolerant storage and processing infrastructure.

- modules of hadoop

  - `HDFS`
    - Hadoop distributed file system states that the files will be broken into blocks and stored in nodes over the distributed architecture.
  - `Map Reduce`
    - help to processing large datasets in parallel across a distributed cluster of computers.
    - helps to do the parallel computation on data using key value pair.
  - `Yarn`
    - Yet another resource negotiator is used for job scheduling and manage the cluster.


### Hadoop distributed file system
- HDFS is a distributed file system that allows you to sotre large data across the cluster.
- HDFS distributes data across multiple nodes ina hadoop cluster.it breaks large faile sinto samller blocks (typically 128 mb or 256mb in size) and stores multiple copies of theses blocks across different nodes for fault tolerance.

- HDFS Architecture
  - Master-Slave Architecture
    - `NameNode (master)`
      - master server/node 
      - manages the metadata and namesacpe of the file system.
      - also keeps track of te structure of the file system, including the locations of data blocks and other metadata.
    - `DataNodes (slave)` 
      - Slave/worker servers/nodes
      - store the actual data blocks
      - responsible for reading and writing data upon request from clients and reporting their health and status to the NameNode(HeartBeats)

- The Hadoop ecosystem comprises seveal other components like
  - hive
  - apache spark etc
- The hadoop ecosystem works together on big data management