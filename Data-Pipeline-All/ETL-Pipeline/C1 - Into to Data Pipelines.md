## Overview od Data Pipelines 

### 1. **What is a Data Pipeline?**
   - Definition: An automated process that extracts data from a source system, transforms it into a desired model, and loads the data into a file, database, or other data storage tool
   - ETL Pipelines: Extract, Transform, Load.
   - Automation is a key feature, triggered by events or schedules.

###  **Components of an ETL Pipeline:**
- **Extraction:**
   - Process of pulling data from a source system, which may be a file, database, or API.
   - Involves accessing and retrieving raw data in its original format.

-  **Transformation:**
   - Converts the extracted raw data into a desired model or format.
   - Encompasses both simple and advanced transformations to create a dataset ready for reporting.

-  **Loading:**
   - Involves loading the transformed data into a storage medium for downstream use.
   - The destination could be a file, data warehouse, or a POST request to an API.
   - Ensuring stable access to the transformed data for users is crucial.

-  **ELT Pipeline (Alternative Architecture):**
   - Briefly mentioned as an alternative to ETL.
   - In this approach, the "load" and "transform" steps are swapped based on the organization's architecture.
   - Focus in the course remains primarily on ETL pipelines.

