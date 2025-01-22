# 🛒 Sales and Profitability Analysis - Power BI

## 📌 Table of Contents  
1. [Project Overview](#project-overview)  
2. [Data Sources](#data-sources)  
3. [Tools Used](#tools-used)  
4. [Data Cleaning & Preparation](#data-cleaning--preparation)  
5. [Exploratory Data Analysis](#exploratory-data-analysis)  
6. [Data Analysis](#data-analysis)  
7. [Results & Findings](#results--findings)  
8. [Recommendations](#recommendations)  
9. [References](#references)

## 📌 Project Overview  
This project focuses on analyzing sales and profitability data to uncover key revenue drivers, optimize sales strategies, and enhance business performance. The objective is to evaluate sales trends, customer segments, regional performance, and discount impacts to provide actionable insights.  

Key goals include:  
- Identifying **high-margin products**  
- Assessing **regional sales performance**  
- Analyzing **customer segments and their contributions to sales**  
- Evaluating **the impact of discounts on profitability**  
- Understanding **shipping mode efficiency**  
- Providing an interactive **Power BI dashboard** for decision-making  

---

## 📊 Data Sources  
- **Dataset:** The sales dataset was sourced from [Insert Source Here]  
- **File Format:** Excel (`.xlsx`)  

The dataset includes:  
- **Sales Data:** Transactional records (Order ID, Sales, Profit, Quantity, Discount, etc.)  
- **Customer Data:** Customer ID, Name, and Segment  
- **Product Data:** Product ID, Category, Subcategory, Product Name  
- **Geographical Data:** Region, State, Country  
- **Order Details:** Order ID, Order Date, Ship Date, Ship Mode  

---

## 🛠️ Tools Used  
- **Power BI** (For visualization and dashboard creation)  
- **Excel** (For initial data exploration)  
- **DAX (Data Analysis Expressions)** (For custom calculations and measures)  
- **Power Query** (For data transformation and cleaning)  

---

## 🧹 Data Cleaning & Preparation  
Before analysis, several preprocessing steps were taken:  
1. **Removed Unnecessary Columns**: Dropped Row ID as it was not relevant to analysis.  
2. **Handled Missing Values**: Checked for and addressed missing values.  
3. **Created a Calendar Table**: Built a date table to support time-based analysis.  
4. **Normalized Data Structure**: Separated data into **fact** and **dimension** tables to establish a star schema.  
5. **Data Type Adjustments**: Ensured correct data types for calculations and mapping.  

---

## 📊 Exploratory Data Analysis  
Exploratory analysis was conducted to understand trends and patterns:  
- **Sales Trends Over Time:** Monthly and yearly trends identified.  
- **Regional Performance:** Evaluated total sales and profit distribution by region.  
- **Customer Segmentation:** Assessed sales contributions across customer groups.  
- **Top Products by Profitability:** Identified key revenue-generating products.  
- **Impact of Discounts on Profit:** Analyzed correlation between discount rates and profit margins.  

---

## 📈 Data Analysis  
Several **DAX measures** were created to calculate key metrics:  
1. **Total Sales:** `SUM(Sales[Sales])`  
2. **Total Profit:** `SUM(Sales[Profit])`  
3. **Total Quantity Sold:** `SUM(Sales[Quantity])`  
4. **Profit Margin (%):** `DIVIDE([Total Profit], [Total Sales], 0)`  
5. **Average Discount:** `AVERAGE(Sales[Discount])`  
6. **Total Orders:** `COUNT(Sales[Order ID])`  
7. **Year-to-Date Sales (YTD):** `TOTALYTD([Total Sales], 'Calendar Table'[Date])`  

---

## 📊 Results & Findings  

### **1️⃣ High-Profit Products**  
- **Canon ImageCLASS Printers**, **Cisco Telepresence Systems**, and **Fellowes Paper Shredders** were among the highest profit-generating products.  

### **2️⃣ Regional Performance**  
- **Top Performing States:** California ($76,381), New York ($74,038), Washington ($33,402)  
- **Underperforming States:** Texas (-$25,729), Ohio (-$16,971), Pennsylvania (-$15,559)  

### **3️⃣ Customer Segments**  
- **Consumer Segment**: Highest profit ($134,119), driven by West and East regions.  
- **Corporate Segment**: Strong performer, with high sales in the West ($34,437).  
- **Home Office Segment**: Lowest profit ($60,298), mainly from the East region.  

### **4️⃣ Impact of Discounts on Profitability**  
- The **average discount was 15.62%**, reducing the **profit margin to 12.47%**.  
- Higher discount rates correlated with **lower profitability**, indicating a need for better discount control.  

### **5️⃣ Shipping Mode Efficiency**  
- **Standard Shipping** contributed the highest sales and profit.  
- **Same-Day Shipping** showed minimal impact, requiring review for cost-effectiveness.  

---

## 🎯 Recommendations  

### **1️⃣ Focus on High-Profit Products**  
- Prioritize sales of **Canon ImageCLASS Printers**, **Cisco Telepresence Systems**, and **Fellowes Paper Shredders**.  
- Optimize inventory for these products to avoid stockouts in high-performing regions.  

### **2️⃣ Strengthen Sales in Top-Performing Regions**  
- **California, New York, and Washington** should receive increased marketing investments.  
- Expansion strategies should target these regions to maximize profitability.  

### **3️⃣ Address Challenges in Underperforming Regions**  
- **Texas, Ohio, and Pennsylvania** require a deep dive into pricing, marketing, and customer demand.  
- Strategies such as localized promotions or logistics improvements can be tested.  

### **4️⃣ Optimize Discounting Strategy**  
- Reduce the overall **discount rate (15.62%)** to improve profit margins.  
- Implement **targeted discounts** rather than general discounts across all products.  

### **5️⃣ Improve Shipping Strategy**  
- **Standard Shipping** should remain the default for cost-effectiveness.  
- **Same-Day Shipping** should be limited to high-demand, high-margin products only.  

---

## 🔗 References  
1. **Dataset Source**: [Insert Dataset Source]  
2. **Power BI Documentation**: [https://docs.microsoft.com/en-us/power-bi/](https://docs.microsoft.com/en-us/power-bi/)  
3. **DAX Function Guide**: [https://dax.guide/](https://dax.guide/)  
