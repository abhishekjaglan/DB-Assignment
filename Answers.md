# Question 1)  Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
Ans) The relationship between the PRODUCT and PRODUCT_CATEGORY tables is a "one-to-many" relationship.

Here's how the relationship works:

-Each row (or record) in the PRODUCT table represents a single product.
-Each row in the PRODUCT_CATEGORY table represents a single product category.
However, a single product category can have multiple products associated with it. This is where the "one-to-many" relationship comes into play.

In terms of foreign keys:

-The PRODUCT table contains a column named CATEGORY_ID, which serves as a foreign key referencing the ID column of the PRODUCT_CATEGORY table.
-This foreign key constraint establishes the relationship between products and their corresponding categories.
-Each product in the PRODUCT table must have a valid CATEGORY_ID that exists in the PRODUCT_CATEGORY table, ensuring referential integrity.
Therefore, each product is associated with exactly one category.

In summary, the relationship between PRODUCT and PRODUCT_CATEGORY can be described as follows:
"Each product belongs to one category, but each category can have multiple products associated with it."



# Question 2) How could you ensure that each product in the "Product" table has a valid category assigned to it?
Ans) To ensure that each product in the PRODUCT table has a valid category assigned to it, we can use a foreign key constraint.

Here's how we can ensure data integrity:

- Foreign Key Constraint: Define the CATEGORY_ID column in the PRODUCT table as a foreign key that references the ID column in the PRODUCT_CATEGORY table.
- ON DELETE CASCADE: Optionally, we can specify ON DELETE CASCADE in the foreign key constraint.
  This means that if a category is deleted from the PRODUCT_CATEGORY table, all associated products will also be deleted automatically.
  However, we've to be cautious with this option, as it might not be desirable in all scenarios.
- Valid Category IDs: Ensure that all entries in the PRODUCT table have a valid CATEGORY_ID that exists in the PRODUCT_CATEGORY table.


