Database structure for MongoDB's **budgeting module** and **inventory management module**. 

### **1. Budget Module - MongoDB Structure**

#### Collections:

**a. Budgets**
```json
{
  "_id": ObjectId("..."),
  "name": "Annual Budget 2025",            // Name of the budget
  "description": "Budget for 2025 operations",  // Description
  "start_date": ISODate("2025-01-01T00:00:00Z"),  // Start date of the budget
  "end_date": ISODate("2025-12-31T23:59:59Z"),    // End date of the budget
  "total_budget": 500000,              // Total budget allocated
  "created_at": ISODate("2025-02-01T10:00:00Z"),  // Timestamp when the budget was created
  "updated_at": ISODate("2025-02-15T14:00:00Z")   // Timestamp for the last update
}
```

**b. Budget_Items**
```json
{
  "_id": ObjectId("..."),
  "budget_id": ObjectId("..."),          // Link to Budgets collection
  "category": "Marketing",               // Category of the budget (e.g., Marketing, Operations)
  "allocated_amount": 10000,             // Allocated budget for this category
  "actual_spent": 7500,                  // Actual spending in this category
  "variance": 2500,                      // Difference between allocated and actual
  "forecasted_spend": 8000,              // Predicted spending (can be updated over time)
  "created_at": ISODate("2025-02-01T10:00:00Z"),  // Timestamp when the item was created
  "updated_at": ISODate("2025-02-15T14:00:00Z")   // Timestamp for last update
}
```

**c. Transactions**
```json
{
  "_id": ObjectId("..."),
  "budget_item_id": ObjectId("..."),     // Link to the Budget_Items collection
  "amount": 2000,                        // Amount spent in this transaction
  "transaction_date": ISODate("2025-02-10T14:00:00Z"), // Date of the transaction
  "description": "Marketing campaign",   // Description of the transaction
  "transaction_type": "Expense",         // Type of transaction (e.g., Expense, Income)
  "created_at": ISODate("2025-02-10T15:00:00Z")   // Timestamp when the transaction was recorded
}
```

**d. Users (for Roles and Permissions)**
```json
{
  "_id": ObjectId("..."),
  "username": "john_doe",
  "role": "Manager",                    // Role of the user (e.g., Manager, Accountant)
  "email": "johndoe@example.com",       // User's email
  "password_hash": "hashedpassword",    // Password (hashed)
  "permissions": ["create_budget", "view_reports"], // List of actions this user can perform
  "created_at": ISODate("2025-01-01T10:00:00Z")   // Timestamp for user creation
}
```

---

### **2. Inventory Management Module - MongoDB Structure**

#### Collections:

**a. Products**
```json
{
  "_id": ObjectId("..."),
  "name": "Laptop",                   // Name of the product
  "description": "Dell XPS 13",        // Product description
  "category": "Electronics",           // Category of the product (e.g., Electronics, Furniture)
  "price": 1200.00,                    // Price per unit
  "sku": "DLXPS13",                    // Unique product identifier (Stock Keeping Unit)
  "supplier_id": ObjectId("..."),      // Link to Supplier collection
  "created_at": ISODate("2025-01-01T10:00:00Z"),  // Timestamp when the product was added
  "updated_at": ISODate("2025-02-15T14:00:00Z")   // Timestamp for last update
}
```

**b. Inventory_Levels**
```json
{
  "_id": ObjectId("..."),
  "product_id": ObjectId("..."),       // Link to Products collection
  "location_id": ObjectId("..."),      // Link to Locations collection (optional if multiple warehouses)
  "quantity": 50,                      // Current stock level
  "minimum_stock": 10,                 // Minimum stock level before reorder
  "maximum_stock": 100,                // Maximum stock level
  "created_at": ISODate("2025-01-01T10:00:00Z"),  // Timestamp when inventory was updated
  "updated_at": ISODate("2025-02-15T14:00:00Z")   // Timestamp for last update
}
```

**c. Transactions (Inventory Movement)**
```json
{
  "_id": ObjectId("..."),
  "product_id": ObjectId("..."),       // Link to Products collection
  "transaction_type": "Sale",          // Type of movement (Sale, Purchase, Transfer)
  "quantity": 5,                       // Quantity of items moved
  "transaction_date": ISODate("2025-02-10T14:00:00Z"), // Date of transaction
  "location_id": ObjectId("..."),      // Location or warehouse
  "created_at": ISODate("2025-02-10T15:00:00Z")   // Timestamp when transaction was logged
}
```

**d. Suppliers**
```json
{
  "_id": ObjectId("..."),
  "name": "Tech Supplies Inc.",         // Supplier name
  "contact_name": "Jane Doe",           // Contact person at the supplier
  "contact_email": "jane@techsupplies.com",  // Contact email
  "contact_phone": "+1234567890",      // Contact phone number
  "address": "123 Tech St, City, Country", // Supplier address
  "created_at": ISODate("2025-01-01T10:00:00Z")  // Timestamp for when the supplier was added
}
```

**e. Locations (optional)**
```json
{
  "_id": ObjectId("..."),
  "name": "Warehouse A",               // Location name (e.g., Warehouse A, Store 1)
  "address": "456 Warehouse Ave",      // Physical location address
  "created_at": ISODate("2025-01-01T10:00:00Z")  // Timestamp for when the location was created
}
```

---

