# APACHE SPARK
- `Apache Spark is fast and general-purpose multi-language engine for executing data engineering,data science and machine learning on single-node machines or cluster.`

## Spark Infrastructure
![apachespark1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/3a5c0466-2adb-4df2-a4a4-5c9e7b778f64)


## Spark Cluster Using Databricks

- just an example
  
![apachespark2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/e573528c-53dd-460d-a328-628fbfcd1ed0)

### Executor in spark cluster

- executor is nothing but Java Virtual Machines (JVMs)
- each JVMs have slots (unused capacity of a given node )(eg. 4core = 4slots)
- slots are tasks that take care of processing the data. (task is used capacity)

![apachespark3](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/9837147d-8e6a-4685-92bc-9f7a427b838b)


### Spark Terms

- `Application`
    - User program built on Spark.Consists of a driver program and executors onthe cluster.
- `Application jar`
    - A jar containing the user's Spark application.(for Java or Scale)
    - for python zip
- `Driver program`
    - the process running the main[] function of the application and creating the SparkContext

- `Cluster Manger`
    - An external service for acquiring resources on the cluster(eg.standalone manager,mesos,yarn,kubernetes)

- `Worker node`
    - Any node that can run application code in the cluster
- `Executor`
    - A process launched for an application on a worker node,that runs tasks and keeps data in memeory or disk storage

- `Task`
    - A unit of work that will be sent to one executor

- `Job`
    - A parallel computation consisting of multiple tasks that gets spawned in response to spark action(eg save,collect),can see in `driver logs`

- `Stage`
    - Each job gets `divided` into `smaller sets of tasks` called `stages` that depend on each other.

### Img explaining job and stages

![apachespark4](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/2c78b37c-73d4-4de8-84a2-c834b0389156)
