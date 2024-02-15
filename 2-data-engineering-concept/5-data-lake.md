# Data Lake

- A Data Lake is a centralized repository that allows you to store and manage vast amounts of `structured` and `unstructured` data at any scale.

- Unlike traditional data warehouses,which often require a `predefined schema` of data organization (`structured only`),data lakes can store data in its raw,unprocessed form.(`holds vast quantities of unrefined information`)

- Data is `loaded directly` into the data lake `without` passing through an `integration layer` or a `transformation layer`. The imported data can be structured, such as relational database tables, semi-structured, like CSV and JSON files, or unstructured, such as PDFs and images.

- This includes data from various sources such as social media, sensors, devices, logs, and other sources.

- `Users can apply different schemas or interpretations of the data based on their analysis needs`, making data lakes suitable for storing raw, varied, and large volumes of data.

## Data Warehouse vs Data Lake

- `Data Warehouse` often use an `ETL layer` and data in warehouse is ready for immediate use without requiring further processing.

- `Data Lakes` generally use `ELT layer` and Data is ingested as-is, `regardless` of whether it matches the format of other data contained in the data lake. `Transformation` is performed `on-demand` by specialist tools, such as Big Data analytics platforms, which is referred to as schema-on-read.

- `Data Warehouse` is `schema-on-write` where as `Data Lakes` is `schema-on-read`.

    - `schema-on-write` 
        - the approach in which we define the columns,data format,relationships of columns etc `before` the `actual data upload`
        - Meaning `before` data is `loaded` into the `warehouse`, it must conform to a `predefined schema`. 

    - `schema-on-read`
        - In a data lake, the data is `ingested`(Load) in its raw,structured or unstructured form without a `predefined schema`.
        - It has fast data ingestion because `data shouldn't` follow any `internal schema` - it's just copying/moving files.

        #img

### Why are Data Lakes Useful?

- For high-volume data sources
- To perform Big Data analytics
- For long-term storage
- Real-time Data processing

### What are the Drawbacks of Data Lakes?

- Unreliable data
- Slow analytics and production use
- Need of Good Data governance and transparency
    - setting internal standards-data policies-that apply to how data is gathered,stored,processed and disposed of.