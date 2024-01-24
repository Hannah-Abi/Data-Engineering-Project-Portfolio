### 1.  Star Schema
- **Overview:** Simplest form of the dimensional model.
- **Components:**
  - Fact Table: Holds metrics records.
  - Dimension Tables: Provide details related to the metrics.
- **Example:** Book sales database for bulk sales across the US and Canada.
- **Connection Pattern:** One-to-many relationships represented by lines, forming a star shape.

### 2.  Star Schema Example
- **Fact Table:** Holds sales amount and quantity.
- **Dimensions:**
  - Books Sold
  - Time of Sale
  - Store Buying the Books
- **Relationships:** One-to-many, creating the star schema appearance.
![star-schema-book](./star-schema.png)
### 3.  Snowflake Schema (an Extension)
- **Extension of Star Schema:** More tables involved.
- **Similarities with Star Schema:**
  - Same Fact Table.
  - Information remains the same.
- **Difference:** Dimension tables are more normalized, extending over multiple dimensions.
![snowflake-schema-book](./snowflake-schema.png)
### 4.  Normalization
- **Definition:** Technique dividing tables into smaller ones, connected via relationships.
- **Goal:** Reduce redundancy and enhance data integrity.
- **Example:** Identifying repeating groups in the book dimension and normalizing them.

### Book Dimension
- **Star Schema:**
  - Represents titles, authors, publishers, and genres.
- **Normalization (Snowflake Schema):**
  - Creates separate tables for authors, publishers, and genres.
![book-dimension-normalisation](./book-dimension-of-snowlake-schema.png)
### Time Dimension
- **Normalization:** Extends days to months, quarters, and more.

