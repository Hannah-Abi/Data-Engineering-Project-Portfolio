## **Extracting Data in ETL:**

**Extracting Data in ETL:**

1. **Source Systems:**
   - Common sources: CSV, parquet, JSON, SQL databases, APIs, data lakes.
   - Focus on tabular sources like parquet files and SQL databases.
   - 
     ```python
     import pandas as pd

     # Replace 'your_csv_file.csv' with the actual file path
     csv_data = pd.read_csv('your_csv_file.csv')
     ```

2. **Reading Parquet Files:**
   - Efficient column-oriented format for storage.
   - Reading into DataFrame with pandas (`read_parquet`), faster than CSV.
   - 
     ```python
     import pandas as pd

     # Replace 'your_parquet_file.parquet' with the actual file path
     parquet_data = pd.read_parquet('your_parquet_file.parquet', engine='fastparquet')
     ```

3. **Connecting to SQL Databases:**
   - Widely used tabular data source.
   - `read_sql` in pandas for querying and storing in DataFrame.
   - Connection through sqlalchemy's `create_engine` with a connection URI.
   ```
   import sqlalchemy
   import pandas as pd
   # Connection URI:
   schema_identifier://username:password@host:port/db
   connection_uri = "postgresql+psycopg2://repl:password@localhost:5432/market"
   db_engine = sqlalchemy.create_engine(connection_uri)
   ```
   ```
   # Query the SQL database
   raw_stock_data = pd.read_sql("SELECT * FROM raw_stock_data LIMIT 10", db_engine)
   ```
5. **Modularity:**
   - Crucial for pipeline development.
   - Separate "extract," "transform," and "load" logic into functions.
   - Adherence to PEP-8 principle "don't repeat yourself."
   - Code reformatted into reusable functions for efficiency and troubleshooting in future pipelines.
