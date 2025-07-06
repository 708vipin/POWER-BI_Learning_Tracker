# POWER BI Cartesian Product (Cross Join) Problem.
# 🔁 Power BI Practice: Cross Join – Operating ID × Dates

## 🧠 Problem Statement

You are given two separate tables:
- **Operating ID** – with a single column: `ID`
- **Dates** – with a single column: `Date`

Each table contains **5 rows**. The task is to create a new table where:
- Each **date** is paired with **all 5 IDs**
- Resulting in a final table with **25 rows** and **2 columns**: `Date` and `ID`

---

## 📂 Tables Involved

### Operating ID Table
| ID   |
|------|
| 1 |
| 2 |
| 3 |
| 4 |
| 5 |

### Dates Table
| Date       |
|------------|
| 2025-07-01 |
| 2025-07-02 |
| 2025-07-03 |
| 2025-07-04 |
| 2025-07-05 |

---

## 🛠️ Solution in Power BI - Power Query Editor

### ✅ Step-by-Step

1. Load the tables Operating ID $ Dates in POWER BI.
2. Click -> "Transform Data" Tab -> Power Query Editor.
3. Operating ID table -> Add Column -> General(Custom Column) -> Put any INT in Custom Column Formula.
4. Select Dates table -> Add Column -> General(Custom Column) -> Put the same INT as above in Custom Column Formula.
5. Change the data types of the custom column to whole numbers.
6. The two tables, Operating ID & Dates now have common column and they can now be joined.
7. HOME -> Combine > Merge Queries > Merge Queries as NEW.
8. Select Tables and the Common Columns -> Both Tables are joined.
9. Remove the custom column.
```DAX
CrossJoinedTable = 
CROSSJOIN('Operating ID', 'Dates')
