1st ans:-Many-to-one relation (A product can have more than one category here.)

2nd ans:-  To ensure that each product in the "Product" table has a valid category assigned to it, we should set up a foreign key constraint between the "Product" table and the "product_category" table. This constraint would link the "category_id" column in the "Product" table to the "id" column in the "product_category" table. This way, every value in the "category_id" column of the "Product" table must correspond to an existing "id" in the "product_category" table, ensuring a valid category assignment.
