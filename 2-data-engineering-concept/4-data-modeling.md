# Data Modeling

- Data modeling is a process used in information systems design and software engineering to define and analyze data requirements needed to support business processes.

- It involves `creating` a `visual representation` of the `structure` and `relationship` within a `database` or `information system`.

- The primary goal of data modeling is to ensure that data is organized and stored in a way that meets the needs of the business while also facilitating efficient and effective data management.

- Key aspects of data modeling include:
    - View Data model
        - represents high-level concepts and relationships between them.

        - this level tells the application about `how the data should be shown to the users`.
    
    - Logical Data Model
        - this level of data modeling translates the view model into a more detailed structure that can be implemented in a database management system.

        - this level tells `how the data is actually stored and structured`.

        - it defines `entites`,`attributes`,`relationships` and `constraints` in a way that is independent of any specific database technology.

    - Physical Level
        - this level involves specifying the actual database `internal schema`,including details like `tables`,`columns`,`data types` and `indexes`.

        - the physical level tells us that `where the data is actually stored`

## Categories of Data Model

    - **Entity-Relationship Data Model**
        - The Entity-Relationship (ER) model is a `conceptual data modeling technique` used to represent the structure of a database in terms of `entities` , `attributes`, and `relationships`.  

        - `ER diagrams` visually represent these components and their relationships.

        #img

    - **Object-based Data Model**
        - An Object-Based Data Model (OBDM) is a type of data model that is based on the principles of `object-oriented programming`

        - In an object-based data model, data is organized and represented as objects, which encapsulate both data (attributes) and behaviors (methods or procedures). 

        - Example use case
            - Object-Relational Mapping(ORM)
                - Focuses on bridging the gap between object-oriented programming and relational databases, mapping objects to database tables.

    - **Dimensional Data Model**

        - A Dimensional Data Model is a data modeling techinque used in `Data warehousing` and `business intelligence` to organize and structure data for efficient `querying` and `reporting`

        - Key Components

            - `Fact Table`
                - Definition: The central table in the dimensional model that contains quantitative data or facts related to a specific business process or event

                - Example: If the business process is sales, the fact table may contain measures like sales revenue, quantity sold, and profit.

            - `Dimension Tables`
                - Definition: Tables that store descriptive attributes or dimensions associated with the data in the fact table. Dimension tables provide context to the measures in the fact table.

                - Example: For a sales fact table, dimension tables might include tables for products, customers, time, and geography.               

            - `Primary Key - Foreign Key Relationships`
                - Definition: Relationships between the fact table and dimension tables are established through primary key-foreign key relationships.

                - Example: Example: The primary key of the dimension table (e.g., product ID in the product dimension) is used as a foreign key in the fact table.    


            - Some of the prominent schemas used in data warehousing are:

                - `Star Schema`
                    
                    #img

                - `Snowflake Schema`

                    #img


### Why Denormalization ?

- Denormalization is a database design technique where redundancy is intentionally introduced into the data model.

- Denormalization is done for various reasons, and its benefits include improved query performance, simplified data retrieval, and support for specific types of queries.

- Here are some reasons why denormalization is used:

    - Improved Query Performance:
        - Reduced Joins:
            - Normalized databases often involve multiple joins to retrieve data from related tables. Denormalization reduces the need for joins by incorporating redundant data into a single table, speeding up query performance.

    - Aggregation and Reporting:
        - Efficient Aggregation:
            -  Denormalization can facilitate efficient aggregation and summarization of data, especially when dealing with large datasets.

## NoSql Databases

- `MongoDB`:
    - `Type`: Document Store

- `Cassandra`:
    - `Type`: Wide-Column Store

- `Redis`:
    - `Type`: Key-Value Store

- `Amazon DynamoDB`:
    - `Type`: Key-Value and Document Store