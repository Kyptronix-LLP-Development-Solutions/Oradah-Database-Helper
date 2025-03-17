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
























### 1. **`products` Collection**

This collection stores details about individual products.

```json
{
  "_id": ObjectId("605c72ef1532073e7f98b7b4"),
  "product_name": "Wireless Mouse",
  "sku": "WM12345",
  "category": "Electronics",
  "description": "A high-quality wireless mouse",
  "quantity": 150, // Will Update Everytime based on the inventory transaction
  "price": 25.99,
  "supplier_id": ObjectId("605c72ef1532073e7f98b7b3"),  // Reference to supplier
  "location": "Aisle 3, Shelf B",
  "received_date": ISODate("2025-01-15T00:00:00Z"),
  "last_updated": ISODate("2025-03-10T00:00:00Z"),
  "status": "in_stock",  // Could be 'in_stock', 'out_of_stock', 'discontinued'
  "tags": ["wireless", "mouse", "electronics"],  // Optional: for product filtering
  "image_url": "http://example.com/images/wireless_mouse.jpg"  // Optional: Image URL
}
```

### 2. **`suppliers` Collection**

This collection stores information about suppliers.

```json
{
  "_id": ObjectId("605c72ef1532073e7f98b7b3"),
  "name": "Tech Supplies Co.",
  "contact_name": "John Doe",
  "contact_email": "contact@techsupplies.com",
  "contact_phone": "123-456-7890",
  "address": "123 Tech Lane, Silicon Valley, CA",
  "status": "active",  // Could be 'active', 'inactive'
  "payment_terms": "Net 30"
}
```



### 2. **`inventory_transactions` Collection**

This collection stores all inventory transactions (e.g., purchases, sales, adjustments).

```json
{
  "_id": ObjectId("605c72ef1532073e7f98b7b5"),
  "product_id": ObjectId("605c72ef1532073e7f98b7b4"),  // Reference to product
  "transaction_type": "purchase",  // Could be 'purchase', 'sale', 'adjustment'
  "quantity": 100,
  "unit_price": 25.99,  // Price per unit during this transaction
  "total_value": 2599,  // Quantity * unit_price
  "transaction_date": ISODate("2025-03-10T00:00:00Z"),
  "reference_number": "PO12345",  // Could be purchase order number, sales invoice, etc.
  "transaction_status": "completed",  // Could be 'pending', 'completed', 'cancelled'
  "supplier_id": ObjectId("605c72ef1532073e7f98b7b3")  // Optional: for purchase transactions
}
```

### 3. **`inventory_adjustments` Collection**

This collection is used for adjustments (e.g., stock corrections, damaged goods, returns).

```json
{
  "_id": ObjectId("605c72ef1532073e7f98b7b6"),
  "product_id": ObjectId("605c72ef1532073e7f98b7b4"),  // Reference to product
  "adjustment_type": "damage",  // Could be 'damage', 'theft', 'correction', etc.
  "quantity_adjusted": -10,  // Positive or negative based on the adjustment
  "reason": "Product damaged during shipment",
  "adjustment_date": ISODate("2025-03-11T00:00:00Z"),
  "user_id": ObjectId("605c72ef1532073e7f98b7b7"),  // Reference to the user making the adjustment
  "notes": "Adjusted stock due to damages"
}
```

