# APACHE SPARK
- `Apache Spark is fast and general-purpose multi-language engine for executing data engineering,data science and machine learning on single-node machines or cluster.`

## Spark Infrastructure
#img

## Spark Cluster Using Databricks

- just an example
    #img

### executor in spark cluster

- executor is nothing but Java Virtual Machines (JVMs)
- each JVMs have slots (unused capacity of a given node )(eg. 4core = 4slots)
- slots are tasks that take care of processing the data. (task is used capacity)
#img

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

#img explaing job and stage
