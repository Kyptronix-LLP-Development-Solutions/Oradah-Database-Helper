Database structure for MongoDB's  **inventory management module**. 

#### Collections:
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



### 3. **`inventory_transactions` Collection**

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

### 4. **`inventory_adjustments` Collection**

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

