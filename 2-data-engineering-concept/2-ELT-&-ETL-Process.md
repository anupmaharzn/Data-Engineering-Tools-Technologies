# ELT and ETL Process

## ETL
- ETL stands for Extract, Transform, Load. 

- It’s a process that involves:
    - `Extract`: Data is extracted from homogeneous or heterogeneous data sources

    - `Transform`: Data is transformed for storing in the proper format or structure for the purposes of querying and analysis.

    - `Load`: Data is loaded into the final target database, more specifically, an operational data store, data mart, or data warehouse.

## ELT

- ELT (Extract, Load, Transform) is a `variant of ETL` wherein the extracted data is first loaded into the target system. ***Transformations are performed after the data is loaded into the target database.***

### Advantages of ELT over ETL 

- `Speed`: Since data is loaded first, transformations can often be done more quickly.

- `Flexibility`: Transformations can be modified without having to re-load the data.

- `Scalability`: ELT is typically more scalable than ETL as it leverages the power of the target system for transformations.

`ELT is particularly useful when dealing with large volumes of data where the transformation processing would be resource-intensive on the source system.`


**`NOTE`**

- **`ETL`** is typically used when the `transformations are complex`, `the data quality is poor`, or the source `system` is `not powerful enough` to handle the `transformation load`.

- **`ELT`** is typically used when dealing with `very large volumes of data`, the source `system` is `powerful enough` to handle the` transformation load`, or `real-time insights are needed`.
