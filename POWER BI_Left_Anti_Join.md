# 🔍 Power BI Practice: Left Anti Join – Sheet1 vs Sheet2

## 🧠 Problem Statement

You are given two tables: `Sheet1` and `Sheet2`.  
Your task is to find the rows that are present in **Sheet1** but **not in Sheet2**, even though both tables contain nearly identical columns and data.

---

## 📂 Input Tables

### 🟦 Sheet1
| First Name | Second Name | Age | City      | State      | Region       |
|------------|--------------|-----|-----------|------------|--------------|
| Ankur      | Singh        | 25  | Patna     | Bihar      | North India  |
| Abhinav    | Shukla       | 28  | Banglore  | Karnataka  | South India  |
| Madhu      | Verma        | 36  | Gangtok   | Sikkim     | East India   |
| Aman       | Jaiswal      | 18  | Jaipur    | Rajasthan  | West India   |
| Shashank   | Singh        | 26  | Gurugram  | Haryana    | North India  |
| Praful     | Tripathi     | 42  | Chennai   | Tamil Nadu | South India  |

### 🟨 Sheet2
| First Name | Last Name    | Age | City      | State      | Region       |
|------------|--------------|-----|-----------|------------|--------------|
| Ankur      | Singh        | 25  | Patna     | Bihar      | North India  |
| Abhinav    | Shukla       | 28  | Banglore  | Karnataka  | South India  |
| Shashank   | Singh        | 26  | Gurugram  | Haryana    | North India  |
| Praful     | Tripathi     | 42  | Chennai   | Tamil Nadu | South India  |

---

## 🛠️ Solution 1 – Power Query (Left Anti Join)

1. Load both Sheet1 and Sheet2 into Power Query : HOME -> Queries( Transform Data )
2. Select all columns in Sheet1 and Sheet2 (except headers)
3. Go to `Home` → `Merge Queries as New` → choose:
   - **Sheet1 as base**
   - **Sheet2 as table to join**
   - Join kind: **Left Anti Join**
4. Click OK → you’ll get only rows **in Sheet1 but not in Sheet2**

✅ Output:
| First Name | Second Name | Age | City    | State     | Region      |
|------------|--------------|-----|---------|-----------|-------------|
| Madhu      | Verma        | 36  | Gangtok | Sikkim    | East India  |
| Aman       | Jaiswal      | 18  | Jaipur  | Rajasthan | West India  |

---

## 🧮 Solution 2 – Using DAX (EXCEPT)

If tables are loaded into Power BI with identical column names and structure:


```DAX
OnlyInSheet1 = EXCEPT(Sheet1, Sheet2)

```


## 📝 Notes
1. A measure always returns a SCALAR value. So if a table is required in output, NEW TABLE should be used not MEASURE.

