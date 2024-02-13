# Data Warehousing

- A data warehouse is a large, centralized repository of data that combines data from various sources to support business intelligence and reporting efforts.

- The concept of a data warehouse was introduced by `Bill Inmon`, who defined it as a “`subject-oriented`, `integrated`, `time-variant`, and `non-volatile` collection of data in support of management’s decision-making process.” 
    - Let's break down this defination:
        - `Subject-Oriented`: Data warehouses are organized around key subjects of an organization, such as customers, products, sales, etc.

        - `Integrated`: A data warehouse integrates data from multiple data sources into a unified, consistent format.

        - `Time-Variant`: Data warehouses maintain historical data, unlike operational systems which keep transactional data.

        - `Non-Volatile`: Once data is entered into the warehouse, it should not change. This ensures consistency in reporting.

## Data Warehouse Architecture and its Components

- img 1
![datawarehouse1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/fa3aaf39-d9b5-4c10-a019-924583fa7ce2)


- img 2
![datawarehouse2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/60d191b4-17e3-44e6-bf13-acbd3552fe3a)


### Key components of a data warehouse include:

    - `Database`:This is where the data is stored after it’s been cleaned, transformed, and loaded.

    - `ETL Tools`: These tools extract, transform, and load data into the data warehouse.

    - `Metadata`: This is the data about the data, and it helps users understand the data warehouse content.

    - `Data Directory`: This is a catalogue that helps users navigate through the data warehouse.



### Benefits and Challenges of Data Warehousing

- Benefits:
    - `Better Data`:By integrating data from multiple sources, a data warehouse provides a unified, consistent view of an organization’s data.

    - `Improved Decision Making`:With a data warehouse, decision-makers have access to high-quality, reliable data, which leads to more informed decision making

    - `Increased Productivity`:  By providing quick responses to complex business queries, a data warehouse increases productivity.

- Challenges

    - `Complexity` : Designing and implementing a data warehouse can be a complex process due to the need to source and integrate data from many different sources.

    - `Maintenance` : A data warehouse requires ongoing maintenance to ensure it continues to meet the needs of its users.
