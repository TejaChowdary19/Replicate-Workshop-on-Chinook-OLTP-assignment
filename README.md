# Replicate-Workshop-on-Chinook-OLTP-assignment


### Overview
Replication of Chinook OLTP to Snowflake DW using Azure Data Factory, Blob Storage, and Key Vault.

### Architecture
1. **Pipeline 1:** Extract SQL Server → Blob (Parquet) → Snowflake STAGE  
2. **Pipeline 2:** Transform STAGE → DW (Date, Time, Customer hash merge, Artist, Sales Fact with Date key)    

### Components
- Azure Storage Account (`chinook-landing`, `chinook-dw`)  
- Azure Key Vault (secrets for SQL Pwd, Snowflake Pwd, Blob SAS)  
- Azure Data Factory (pipelines, linked services, datasets)  
- Snowflake DB `MEDIA_DB` ( schemas `STAGE`, `DW` )

### Validation
All dimension/fact counts > 0 and foreign-key checks = 0.  


### Author
Teja Chowdary 
