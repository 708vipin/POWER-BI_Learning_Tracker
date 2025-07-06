# Power BI Conditional Formatting – City Column with Null Handling

## 📌 Problem Statement
In this Power BI task, I manually created a table with three columns:  
`State`, `City`, and `Total Sales`.

Some of the entries in the `City` column were intentionally left blank to represent missing data. The goal was to:

- Display **Green** background color for cells where the `City` is present.
- Display **Grey** background color for cells where the `City` is **null or blank**.
- Apply this formatting **only** to the `City` column using a **DAX measure**, not calculated columns.

---

## 🛠️ Solution Steps

### 1. Created a table manually with the following structure:

| State | City     | Total Sales |
|-------|----------|-------------|
| UP    | Lucknow  | 1000        |
| UP    | Agra     | 2000        |
| UP    | *(null)* | 2500        |
| MP    | Bhopal   | 3400        |
| MP    | Indore   | 5600        |
| Bihar | Patna    | 500         |
| Bihar | *(null)* | 2500        |
| Bihar | Katihar  | 9000        |
| Bihar | *(null)* | 4300        |

---

### 2. DAX Measure for Background Color Formatting:

```DAX
BG colour = 
IF(
    ISBLANK(MIN('Fact'[City])), 
    "#808080",   // Grey for null
    "#008000"    // Green for non-null
)
