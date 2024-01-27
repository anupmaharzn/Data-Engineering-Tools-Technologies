# Google File System(GFS) and Hadoop Distributed File System (HDFS)



## Google File System (published in 2003)

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


```Client interact with master to only get metadata```




### MapReduce (GFS continued)

- lets understand this with Use-Case.

- Google Music analytics stored in GFS
    - Write progem to find which song was played how many times.
    - simple way to do that.
        #img
    - but problem statements
        #img
    - solution
        #img


- WorkFlow of MapReduce


