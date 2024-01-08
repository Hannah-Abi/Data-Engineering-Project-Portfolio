# Data-Engineering-Project-Portfolio
Data Engineering Project Portfolio

| No. | Project | Cateogry | Tools |
|----------|----------|----------|----------|
| 1 | [Tokyo Olympic 2020 Data Analysis](https://github.com/Hannah-Abi/Olympics-Data-Analysis---Azure-Data-Engineering) | Building end-to-end Data Pipeline  | Microsoft Azure, Power BI, Windows |
| 2 | [Apache Airflow with Weather Map API](https://github.com/Hannah-Abi/Weather-Data-Pipeline-with-Apache-Airflow) |Data Pipeline Automation with Airflow | AWS, Visual Studio Code, Linux |
| 3 | [Database Design for distribution of vaccines](https://github.com/Hannah-Abi/Database-Design---Vaccine-Distribution) | Relational Database Design | posgreSQL |
| 4 | [Database Design for a Music Concert](https://github.com/Hannah-Abi/PE-Case---Database-Design) | Relational Database Design | MySQL Server |


### Project 1 
- This project is to create an end to end data platform right from Data Ingestion, Data Transformation, Data Loading and Reporting.
- **Some data analysis questions:**
   1. Which countries do most athletes come from?
   2. Which discipline is most popular and which country has the highest participants in it?
   3. Which country produces highest number of coaches?
   4. Gender across disciplines
   5. Which country recieved most gold medals? Which recieved most silver and most bronze? Which received least for each?
 - **Azure Data Factory** - to ingest data from an HTTP server into ADF
 - **Azure Data Lake Storage Gen2** - to store the raw data
 - **Azure Databricks** - to transform the RAW data to the clean form
 - **Azure Synapse Analytics** - to load the clean data <br> 
 - **Microsoft Power BI**: to build an interactive dashboard
### Project 2 -  Designing a Relational Database - Vaccine Distribution
 - The business requires to build a database to keep track of the different vaccine types, transportation of vaccine batches, treatment plans, and patient data.
   - **Requirement 1:**
     - Draw an ER diagram for the vaccine database based on the information defined in this document.
     - Convert the UML diagram to the relational data model.
     - Present the schemas of the relations and underline the attributes which form the key for each relation.
    - **Requirement 2:**
     - Create a relational database in SQL based on the design from Part I
     - Populate the database with given data (from your project git repository ./data/vaccine-distribution-data.xlsx)
     - Create SQL queries to answer the requested questions
### Project 3 - Designing a Relational Database - Music Concert
 - Paisley Event Association is a small non-profit association organizing a few local concerts, dance and theatre performances and other cultural events yearly. So  tickets have been sold in person at the Paisley tourist office. Now the association is keen on offering web pages, where clients could see upcoming events and book tickets. 
- **Requirement Deliverablea:**
  1. Database Design documentation (One PDF document: DM_Case_Design.pdf)
     - 1.1 ER diagram
     - 1.2 Relational schema
     - 1.3 Repository
     - 1.4 Database diagram (in STEP 2)
  2. SQL Scripts (Four .sql files)
     - 2.1 SQL script to create the database structure in SQL Server
     - 2.2 SQL script to create the basic set of indexes
     - 2.3 SQL script to populate the database with a reasonable amount of proper data for testing
     - 2.4 SQL script to test the database (see STEP 2 below)
  3. Project Closing Report (OnePDF document: DM_Case_Closing_Report.pdf)
     - 3.1 Evaluation of the product and the process
     - 3.2 Working time records per each person per each task

