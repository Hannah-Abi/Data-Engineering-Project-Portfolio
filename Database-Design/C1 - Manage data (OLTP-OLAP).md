![OTLP-OLAP](./OLTP-OLAP-work-together.png)
## Organizing and Managing Data
- **Key Question:** How should we organize and manage data efficiently?
- **Considerations:**
  - Different schemas, management options, and objects in a database
  - Various factors impacting data storage and access, including query speed, memory usage, and cost
- **No One-Size-Fits-All Answer:** The optimal solution depends on how the data will be used.

## Approaches to Data Processing
- **OLTP and OLAP:** These are fundamental approaches to processing data, influencing data flow, structure, and storage.
- **OLTP (Online Transaction Processing):** Oriented around day-to-day transactions.
- **OLAP (Online Analytical Processing):** Oriented around analytics and business decision-making.

## Concrete Examples
- **OLTP Usage:** Tracking book prices, customer transactions, and employee work hours for day-to-day operations.
- **OLAP Usage:** Analyzing profitable books, identifying loyal customers, and determining the employee of the month for strategic decision-making.

## OLAP vs. OLTP
- **OLTP Systems:** Application-oriented, supporting daily operations and providing current transaction snapshots.
- **OLAP Systems:** Subject-oriented, focusing on specific analyses over a more extended period, consolidating data for long-term insights.
- **Query Complexity:** OLTP queries are simpler, while OLAP queries for analysis are more complex.
- **User Base:** OLTP systems used by a broader audience, including customers, while OLAP systems primarily utilized by analysts and data scientists.

## Working Together
- **Collaboration:** OLAP and OLTP systems complement each other.
- **Data Flow:** OLTP data stored in operational databases, pulled and cleaned to create OLAP data warehouses.
- **Influence:** OLAP analyses inform business practices and daily activities, influencing OLTP databases.

