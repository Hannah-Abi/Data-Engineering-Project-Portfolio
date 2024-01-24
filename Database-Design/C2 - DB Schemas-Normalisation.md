### Star Schema
- **Overview:** Simplest form of the dimensional model.
- **Components:**
  - Fact Table: Holds metrics records.
  - Dimension Tables: Provide details related to the metrics.
- **Example:** Book sales database for bulk sales across the US and Canada.
- **Connection Pattern:** One-to-many relationships represented by lines, forming a star shape.

### Star Schema Example
- **Fact Table:** Holds sales amount and quantity.
- **Dimensions:**
  - Books Sold
  - Time of Sale
  - Store Buying the Books
- **Relationships:** One-to-many, creating the star schema appearance.

### Snowflake Schema (an Extension)
- **Extension of Star Schema:** More tables involved.
- **Similarities with Star Schema:**
  - Same Fact Table.
  - Information remains the same.
- **Difference:** Dimension tables are more normalized, extending over multiple dimensions.

### Normalization
- **Definition:** Technique dividing tables into smaller ones, connected via relationships.
- **Goal:** Reduce redundancy and enhance data integrity.
- **Forms of Normalization:** Explored later.
- **Example:** Identifying repeating groups in the book dimension and normalizing them.

### Book Dimension
- **Star Schema:**
  - Represents titles, authors, publishers, and genres.
- **Normalization (Snowflake Schema):**
  - Creates separate tables for authors, publishers, and genres.

### Store Dimension
- **Star Schema:**
  - Includes city, states, and countries.
- **Normalization (Snowflake Schema):**
  - Structures repeating groups differently based on the nature of data.

### Time Dimension
- **Normalization:** Extends days to months, quarters, and more.
  
### Snowflake Schema
- **Consolidation:** All normalized dimensions combined into the snowflake schema.
