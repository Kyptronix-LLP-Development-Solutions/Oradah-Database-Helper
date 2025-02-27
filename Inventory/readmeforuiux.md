### **User Flow for Inventory Module**

**Overview:**
The Inventory Module is designed to help users manage and organize products, categories, and subcategories in their inventory. The system allows users to create categories and subcategories, add products, specify quantities and prices, and view inventory data.

### **Step-by-Step User Flow:**

---

#### **Step 1: Accessing the Inventory Page**
- **Action:** The user navigates to the **Inventory** section from the main dashboard or menu.
- **Expected Outcome:** The user is directed to the **Inventory Page**, which displays an overview of the inventory and provides options for managing categories, subcategories, and products.

---

#### **Step 2: Creating a Category**
- **Action:** On the **Inventory Page**, the user clicks on the **Create Category** button.
- **Expected Outcome:** A form opens for the user to enter the category details.
  
  **Fields in the Create Category Form:**
  - **Category Name:** Name of the category (e.g., Electronics, Furniture, etc.).
  - **Category Description (optional):** A brief description of the category.
  
- **Action:** The user fills in the required information and clicks **Save** to create the category.
- **Expected Outcome:** The new category is added to the list of available categories.

---

#### **Step 3: Creating a Subcategory**
- **Action:** After creating a category, the user clicks on the **Create Subcategory** button under the desired category.
- **Expected Outcome:** A form appears to enter subcategory details.

  **Fields in the Create Subcategory Form:**
  - **Subcategory Name:** Name of the subcategory (e.g., Smartphones, Laptops under Electronics).
  - **Subcategory Description (optional):** A brief description of the subcategory.
  
- **Action:** The user enters the required details and clicks **Save** to create the subcategory.
- **Expected Outcome:** The subcategory is saved under the relevant category and displayed in the list.

---

#### **Step 4: Adding Products**
- **Action:** Once categories and subcategories are set up, the user clicks on the **Add Product** button.
- **Expected Outcome:** The user is taken to a form to enter product details.

  **Fields in the Add Product Form:**
  - **Product Name:** The name of the product (e.g., iPhone 13, Office Chair).
  - **Product SKU (optional):** A unique identifier for the product (e.g., iPhone-13, OC123).
  - **Category:** A dropdown to select the category (predefined from the earlier step).
  - **Subcategory:** A dropdown to select the subcategory (predefined from the earlier step).
  - **Quantity:** The number of units available for the product.
  - **Unit Price:** The price per unit of the product.
  - **Product Description (optional):** Additional details about the product.
  - **Product Image (optional):** An image of the product (if needed).

- **Action:** The user enters the product information, adjusts the quantity and price, and then clicks **Save** to add the product to the inventory.
- **Expected Outcome:** The product is added to the system and is available for viewing and managing.

---

#### **Step 5: Viewing Inventory Data**
- **Action:** The user can view the existing inventory data from the **Inventory Page**.
- **Expected Outcome:** The page displays an overview of all products, their quantities, prices, and categories. There should be options to **filter** by category, subcategory, or product name.

  **Features Available on the Inventory View:**
  - **Search Bar:** To search products by name, SKU, or category.
  - **Category Filter:** To filter products based on the category.
  - **Subcategory Filter:** To filter products by subcategory.
  - **Stock Overview:** Displays available quantity of each product.
  - **Pricing Information:** Displays unit price for each product.
  - **Edit Button:** Option to edit product details, such as price or quantity.
  - **Delete Button:** Option to remove a product from inventory.
  
- **Action:** The user can click on any product to edit or view more details. They can update the quantity, price, or other product information as necessary.

---

### **Fields Breakdown:**

1. **Category Name:** Defines the main grouping of products (e.g., Electronics, Furniture).
2. **Category Description:** Optional description to provide context to the category.
3. **Subcategory Name:** Refines the category into a more specific grouping (e.g., Smartphones under Electronics).
4. **Subcategory Description:** Optional description for the subcategory.
5. **Product Name:** The name of the individual product.
6. **Product SKU:** Optional unique identifier for each product.
7. **Quantity:** Number of units available for the product in inventory.
8. **Unit Price:** The price per unit of the product.
9. **Product Description:** Optional details about the product’s features or specifications.
  
---
