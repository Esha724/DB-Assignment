1st ans:-Many-to-one relation (A product can have more than one category here.)

2nd ans:-  To ensure that each product in the "Product" table has a valid category assigned to it, we should set up a foreign key constraint between the "Product" table and the "product_category" table. This constraint would link the "category_id" column in the "Product" table to the "id" column in the "product_category" table. This way, every value in the "category_id" column of the "Product" table must correspond to an existing "id" in the "product_category" table, ensuring a valid category assignment.

3rd ans:- // Product_Category collection
db.createCollection("product_category")
db.product_category.insert({
    _id: 1,
    name: "Category 1",
    description: "Category description",
    created_at: ISODate("2022-01-01T00:00:00Z"),
    modified_at: ISODate("2022-01-01T00:00:00Z"),
    deleted_at: ISODate("2022-01-01T00:00:00Z")
});

// Discount collection
db.createCollection("discount")
db.discount.insert({
    _id: 1,
    name: "Discount 1",
    description: "Discount description",
    discount_percent: 10.5,
    active: true,
    created_at: ISODate("2022-01-01T00:00:00Z"),
    modified_at: ISODate("2022-01-01T00:00:00Z"),
    deleted_at: ISODate("2022-01-01T00:00:00Z")
});

// Product_Inventory collection
db.createCollection("product_inventory")
db.product_inventory.insert({
    _id: 1,
    quantity: 100,
    created_at: ISODate("2022-01-01T00:00:00Z"),
    modified_at: ISODate("2022-01-01T00:00:00Z"),
    deleted_at: ISODate("2022-01-01T00:00:00Z")
});

// Product collection
db.createCollection("product")
db.product.insert({
    _id: 1,
    name: "Product 1",
    description: "Product description",
    SKU: "SKU123",
    category_id: 1,
    inventory_id: 1,
    price: 50.99,
    discount_id: 1,
    created_at: ISODate("2022-01-01T00:00:00Z"),
    modified_at: ISODate("2022-01-01T00:00:00Z"),
    deleted_at: ISODate("2022-01-01T00:00:00Z")
});
