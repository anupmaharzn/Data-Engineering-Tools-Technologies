# Lake House

- A lakehouse is a new, open architecture that combines the best elements of data lakes and data warehouses.

- `Data Lake` is really good when we want to capture tone's of data in cost effective way but it comes with certain challenges like
    - `Data Governance`
    - `Quality`
    - `Data Swamp`
        - happens when there is a lot of duplicate,inaccurate,incomplete data making it difficult to track and manage assests.

- `Data Warehouse` is great for query performace but we cannot put every thing in it because
    - high cost
    - limited support for semi-structure(json,xml,csv,txt) and unstructure (audio,video,img,pdf) data.


## Architecture of Lake House

#img




#img


### What is New and Different About the Data Lakehouse?

- It all starts with the data lake.Again, the data lakehouse is a higher-level abstraction superimposed over the data in the lake.

- The lake usually consists of serveral `zones`, the `names` and `purposes ` of which vary according to implementation.

- At a minimum,Lakehouse consist of the following:

    - one or more `ingest or landing` zones for data. **bronze**(`raw`)
    - one or more `staging` zones,in which experts work with and engineer data.**silver**(`validate`)
    - one or more `curated` zones,in which prepared and engineered data is made available for access. **gold**(`enriched`)

    #img

## Databricks Lakehouse Architecture


#img 

#img

- `Delta Lake` is an `open-source` `storage layer` that brings `ACID `(Atomicity, Consistency, Isolation, Durability) transactions to `Apache Spark` and `big data` workloads. 

- In Databricks, a `catalog` refers to the metadata service that `manages and organizes` `metadata` about your `data and tables`
    - Key features of the Databricks catalog include:

        - Table Management: 
            - The catalog helps manage tables that are created and used in Databricks.
            - These tables can be based on various data sources, including data stored in `Delta Lake`, `Apache Parquet`, `Apache Avro`, `CSV`, `JSON`, and other formats.

            - `delta` format tables are managed by `delta lake`.
