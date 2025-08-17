# 📊 Excel Practice Lab — SUMIF/COUNTIF, Sorting/Filtering, Conditional Formatting, Data Validation, Pivot, Lookup

A hands-on collection of **Excel practice questions** that build real-world skills in formulas, analysis, data quality checks, dashboards, and lookups. Ideal for students, interview prep, or anyone leveling up analytics.

---
## 🧭 Topics & Tasks

### 1) Formulas & Functions — **SUMIF / COUNTIF**
- **Q1**: Total Units sold in the *East* region  
- **Q2**: Total **Revenue** generated from *Binder*  
- **Q3**: Total **Revenue** for *Central* region where **Item = Pencil**  
- **Q4**: Units sold by **Jones** with **Unit Cost > 4**  
- **Q5**: Units **Jones** sold **excluding Pencil**  
- **Q6**: Number of times **Gill** made a sale  
- **Q7**: Number of times **Gill** sold **Pencils**

> 🧩 *Hint formulas:*  
> `=SUMIF(Region,"East",Units)`  
> `=SUMIF(Item,"Binder",Revenue)`  
> `=SUMIFS(Revenue,Region,"Central",Item,"Pencil")`  
> `=SUMIFS(Units,Rep,"Jones",UnitCost,">4")`  
> `=SUMIFS(Units,Rep,"Jones",Item,"<>Pencil")`  
> `=COUNTIF(Rep,"Gill")`  
> `=COUNTIFS(Rep,"Gill",Item,"Pencil")`

---

### 2) Sorting & Filtering
- **Q1**: Sort dates **Newest → Oldest**  
- **Q2**: Custom sort **Area** in order: *S. County → Central → N. County*  
- **Q3**: Filter all houses in **Central**  
- **Q4**: Central **with Pool** and S. County **without Pool**  
- **Q5**: Agents in **N. County**, **2 bedrooms**, **Single Family**  
- **Q6**: List price **between 4,500,000 and 6,000,000**

> 🧩 *Steps:* Data → Sort / Filter; for custom order use **Custom List**.

---

### 3) Conditional Formatting
- **Q1**: Highlight salespeople with **Revenue > 10,000**  
- **Q2**: Apply **Three-Color Scale** to Revenue  
- **Q3**: Show **Top 10** and **Bottom 10** Revenues  
- **Q4**: **Gradient Fill** for a column or a multi-column comparison  
- **Q5**: **Icon Sets** to flag Greater / Lesser / Static revenues

> 🧩 *Steps:* Home → Conditional Formatting → (Rules/Color Scales/Top-Bottom/Icons).

---

### 4) Data Validation
- **Q1**: Name ≤ **15 characters**  
- **Q2**: Email must contain **"@"**  
- **Q3**: Salary **> 50,000**  
- **Q4**: Rank **between 100 and 200**  
- **Q5**: **City** dropdown (List)  
- **Q6**: **Dependent dropdown**: City → Training Location

> 🧩 *Hints:*  
> Length: `=LEN(A2)<=15` (Use **Custom** validation)  
> Email: `=ISNUMBER(SEARCH("@",A2))`  
> Numeric: **Whole number/Decimal** with limits  
> List: `Data Validation → List` using a named range  
> Dependent list: Use **Named Ranges** + `INDIRECT()`.

---

### 5) Pivot Tables & Charts
- **Q1**: Total sales **by Category**  
- **Q2**: **Max-selling Subcategory** under each Category  
- **Q3**: **Top 3 States** by **avg profit** within each Region  
- **Q4**: **% contribution** of Subcategories to Category Sales  
- **Q5**: Customer with **lowest profit** in **Home Office** per State  
- **Q6**: Sales by **Quarter of 2016** for all Regions; add **Order Year Slicer** and a **Pivot Chart**

> 🧩 *Steps:* Insert → PivotTable → Build fields; Insert → Slicer; Insert → PivotChart.  
> For % contribution: **Value Field Settings → Show Values As → % of Parent Row/Column Total**.

---

### 6) Lookup (VLOOKUP / XLOOKUP / INDEX-MATCH)
- **Q1**: Employee name for **Emp ID 107**  
- **Q2**: Job title of **Fred Stone**  
- **Q3**: Job title for **Emp ID 105**  
- **Q4**: Salary of **Hank Saunders**  
- **Q5**: Emp ID for **Owen_Lindop4826@womeona.net**  
- **Q6**: Job Title of **Javier Power**  
- **Q7**: Emp ID of **Peter_Daniells7930@guentu.biz**  
- **Q8**: Job title & salary of **Eduardo Dale**  
- **Q9**: Show **"Name not found"** for Emp ID **121**  
- **Q10**: Salary of **Peter Daniells**  
- **Q11**: Emp ID with **salary = 10000**  
- **Q12**: Check for **James Bond** → if missing, display **"Not Found"**

> 🧩 *Modern Excel (recommended):*  
> `=XLOOKUP(107, EmpID, Name, "Not Found")`  
> `=XLOOKUP("Fred Stone", Name, JobTitle, "Not Found")`  
> `=XLOOKUP(105, EmpID, JobTitle, "Not Found")`  
> `=XLOOKUP("Hank Saunders", Name, Salary, "Not Found")`  
> `=XLOOKUP("Owen_Lindop4826@womeona.net", Email, EmpID, "Not Found")`  
> `=XLOOKUP("Javier Power", Name, JobTitle, "Not Found")`  
> `=XLOOKUP("Peter_Daniells7930@guentu.biz", Email, EmpID, "Not Found")`  
> `=LET(r,XLOOKUP("Eduardo Dale",Name,CHOOSE({1,2},JobTitle,Salary),"Not Found"),r)`  
> `=IFERROR(XLOOKUP(121, EmpID, Name), "Name not found")`  
> `=XLOOKUP("Peter Daniells", Name, Salary, "Not Found")`  
> `=FILTER(EmpID, Salary=10000, "Not Found")`  
> `=IFERROR(XLOOKUP("James Bond", Name, EmpID), "Not Found")`

> 🧩 *Classic Excel:* Use `VLOOKUP`, `INDEX/MATCH`, and `IFERROR`.

---

## 🚀 Getting Started

1. **Download/Clone** this repo.  
2. Open **Practice-Questions.xlsx** in Excel (365/2021 recommended).  
3. Work through each sheet’s tasks.  
4. (Optional) Compare with solutions or submit a PR with your approach.

---

## ✅ Skills You’ll Practice

- Conditional aggregation with **SUMIF(S)** / **COUNTIF(S)**  
- Data cleaning & validation rules  
- Visual analysis via **Conditional Formatting**  
- Building **Pivot Tables/Charts** & using **Slicers**  
- Fast lookups with **XLOOKUP** / **INDEX-MATCH**  
- Sorting, filtering, and custom sort orders

---

## 🧪 Sample Dataset Notes

- Columns commonly used: `OrderDate, Region, Rep, Item, Units, UnitCost, Revenue, Area, Bedrooms, Pool, Type, State, Category, Subcategory, Segment, Email, EmpID, Salary`.  
- If you see `#####` in Revenue, widen the column or recompute: `=Units*UnitCost`.

---

## 🤝 Contributing

- Add new question sets or datasets (CSV/XLSX).  
- Include a short **README** inside `/solutions` if you add answer files.  
- Open issues for corrections or new ideas.

---

## 📄 License

MIT — use, modify, and share freely. Consider crediting this repo if you remix it.

---

## 🙌 Acknowledgements

Created for learners practicing Excel for academics, internships, and analytics roles. Happy spreadsheeting! ✨
