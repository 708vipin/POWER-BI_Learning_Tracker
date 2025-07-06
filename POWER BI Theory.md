# POWER-BI_Learning_Tracker
I've documented my POWER BI learning in this repository.

# 📊 Power BI Mastery Tracker

A complete, editable roadmap to mastering Power BI — from basics to advanced visuals, DAX, data modeling, and dashboard projects. Built to track my learning, organize concepts, and showcase my skills.

---

## ✅ Progress Checklist

### 🧱 1. Power BI Basics
- [x] Power BI Desktop vs Power BI Service
- [x] Importing Data (Excel, CSV, SQL, Web)
- [x] Data Types & Formatting
- [ ] Data Refresh & Scheduling
- [ ] Saving & Publishing Reports

---

### 🧹 2. Power Query (Data Transformation)
- [x] Remove Columns/Rows
- [x] Replace/Fill/Filter Values
- [x] Split Columns
- [ ] Group By & Aggregate
- [ ] Merge Queries (Joins)
- [ ] Append Queries (Union)
- [ ] Pivot & Unpivot
- [ ] Creating Custom Columns
- [ ] Using M Language (optional)

---

### 🧮 3. DAX (Data Analysis Expressions)
- [x] Calculated Columns
- [x] Measures vs Columns
- [x] SUM(), COUNT(), AVERAGE()
- [ ] CALCULATE(), FILTER()
- [ ] ALL(), ALLEXCEPT()
- [ ] TIMEINTELLIGENCE: DATESYTD(), SAMEPERIODLASTYEAR()
- [ ] SWITCH(), IF(), IFERROR()
- [ ] Variables in DAX

---

### 🧩 4. Data Modeling
- [x] Relationships (One-to-Many, Many-to-Many)
- [x] Star Schema vs Snowflake Schema
- [ ] Cardinality & Cross Filtering
- [ ] Role-playing Dimensions (e.g., multiple Date fields)
- [ ] Normalization/Denormalization

---

### 📈 5. Visualizations
- [x] Bar/Column/Line Charts
- [x] Pie/Donut Charts
- [x] Tables, Matrix
- [x] Slicers & Filters
- [ ] Cards & KPIs
- [ ] Maps (Filled, Shape, ArcGIS)
- [ ] Decomposition Tree
- [ ] Drill Through, Tooltips
- [ ] Bookmarks & Buttons
- [ ] Custom Visuals (Marketplace)

---

### 🛠 6. Report Design & UX
- [x] Themes & Colors
- [ ] Layout Grids
- [ ] Navigation Buttons
- [ ] Interactive Tooltips
- [ ] Mobile View Optimization

---

### 🔐 7. Power BI Service
- [ ] Workspace Management
- [ ] Sharing Reports
- [ ] Dataset Permissions
- [ ] Dashboard Creation
- [ ] Power BI Gateway
- [ ] Row Level Security (RLS)

---

## 🧪 Projects & Dashboards

| Project Name                        | Focus Areas                            | Status |
|------------------------------------|-----------------------------------------|--------|
| Sales Dashboard (Excel Source)     | Visuals, Filters, Slicers               | ✅     |
| HR Attrition Report                | Power Query, KPIs, Cards                | 🕓     |
| Hospital Emergency Analysis        | Matrix, DAX, Time Intelligence          | ✅     |
| E-commerce Sales Trend             | CALCULATE, Custom Measures, UX Design   | ⬜     |

---

## 💡 Notes Section

### 🔸 DAX: CALCULATE() Example
```DAX
Total Sales Last Year = 
CALCULATE(SUM(Sales[Amount]), SAMEPERIODLASTYEAR(Date[Date]))
