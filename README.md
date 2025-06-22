# Synapse_Data_Warehouse_Project

This project is to explore the Data Warehouse creation in Azure Synapse Analytics by using the Medallion Architecture

Highlights -- 

1. Bronze, Silver, Gold containers are created in ADLS gen 2 as the data is extracted from source, transformed and then loaded into data warehouse for final serving.
2. The source is a csv file stored in the Source container in ADLS gen 2.
3. The Bronze layer serves as the staging layer where the data is stored by incremental loading using the pipelines in synapse analytics.
4. The Silver layer serves as the transformed layer where the data is transformed using data flows in synapse analytics.
5. External tables are created in the Silver layer on top of the transformed data in order to query the data using serverless sql pool.
6. In the Gold layer which servers as the core layer the dimension and fact external tables are created to serve the data for analytical purpose.
7. The file format used throughout the different layers apart from source is parquet.
