# 🗄️ Relational Databases (RDBMS)

A **Relational Database Management System (RDBMS)** is a type of database that organizes data into **tables (relations)** consisting of **rows** and **columns**.

---

## 📌 Key Characteristics

### 📐 Fixed Schema
- Data is stored according to a **predefined schema** (table structure).  
- Each table has **well-defined columns** with specific data types.  
- If new data does not match the existing structure, the **schema must be modified** first.  

💡 **Example**:  
If we want to store a new field like `PhoneNumber` for the `Customers` table, we must run:  

```sql
ALTER TABLE Customers ADD PhoneNumber VARCHAR(20);

