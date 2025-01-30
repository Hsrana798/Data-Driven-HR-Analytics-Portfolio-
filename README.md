
# **HR Analytical Dashboard – Power BI Project**  

### 📊 **A comprehensive Power BI dashboard for analyzing HR performance, employee satisfaction, attrition trends, and workforce demographics.**  


## **📌 Project Overview**  
This Power BI project provides insights into **HR analytics**, helping organizations track **employee performance, attrition, workforce demographics, and key HR metrics**. By analyzing this data, HR teams can make **data-driven decisions** to improve employee engagement, retention, and workforce planning.  

---

## **🎯 Key Objectives**  
✔️ **Employee Overview** – Track total employees, new hires, attrition rates, and department-wise distribution.  
✔️ **Employee Performance** – Analyze performance ratings and key productivity metrics.  
✔️ **Attrition Analysis** – Identify trends and reasons behind employee turnover.  
✔️ **Demographics & Diversity** – Analyze employee distribution by age, gender, department, and tenure.  
✔️ **Compensation & Benefits** – Compare salary trends and benefits offered.  
✔️ **HR Business Insights** – Provide actionable recommendations for workforce optimization.  

---

## **📂 Dataset Details**  
📄 **File Name:** `HR_Dataset.csv`  
📊 **Records:** Thousands of employee-related data points  
📝 **Fields:**  
- **Employee Details:** Employee ID, Age, Gender, Department, Job Role  
- **Work Details:** Hire Date, Experience, Job Level, Work-Life Balance  
- **Compensation:** Monthly Salary, Benefits, Overtime, Promotions  
- **Performance:** Performance Rating, Training Hours, Job Satisfaction  
- **Attrition:** Status (Active/Resigned), Exit Reason, Last Working Date  

---

## **🛠️ Steps Followed in Power BI**  

### **1️⃣ Data Loading & Cleaning (Power Query)**  
✅ **Loaded dataset (`HR_Dataset.csv`) into Power BI Desktop.**  
✅ **Checked column quality and removed duplicates based on `Employee ID`.**  
✅ **Handled missing values** (e.g., replaced blank `Salary` values with average salary per job role).  
✅ **Converted `Hire Date` column** to a proper date format for time-based analysis.  
✅ **Filtered unnecessary columns** to optimize performance.  

---

### **2️⃣ Data Modeling & Relationships**  
- **Single-table model used for simplicity.**  
- No additional relationships required as all relevant data exists in one table.  

---

### **3️⃣ DAX Measures & Calculations**  
Here are some key **DAX measures** used in the project:  

#### **🔹 Total Employees**
```DAX
Total Employees = DISTINCTCOUNT('HR_Dataset'[Employee ID])
```
#### **🔹 Attrition Rate**
```DAX
Attrition Rate = 
DIVIDE(
    COUNTROWS(FILTER('HR_Dataset', 'HR_Dataset'[Attrition Status] = "Resigned")),
    COUNTROWS('HR_Dataset')
) * 100
```
#### **🔹 Average Salary**
```DAX
Avg Salary = AVERAGE('HR_Dataset'[Monthly Salary])
```
#### **🔹 Employee Satisfaction Score**
```DAX
Employee Satisfaction Score = AVERAGE('HR_Dataset'[Job Satisfaction])
```
#### **🔹 Gender Diversity %**
```DAX
Gender Diversity % = 
DIVIDE(
    COUNTROWS(FILTER('HR_Dataset', 'HR_Dataset'[Gender] = "Female")),
    COUNTROWS('HR_Dataset')
) * 100
```
#### **🔹 Department-wise Employee Count**
```DAX
Department Employee Count = COUNT('HR_Dataset'[Employee ID])
```

---

## **📊 Dashboard Pages & Visualizations**  
This **Power BI dashboard** consists of **six key pages**, each analyzing different aspects of HR performance.

### **1️⃣ Employee Overview 👥**  
✔️ **KPIs:** Total Employees, Active Employees, Attrition Rate  
✔️ **Visuals:**  
- **Card Visuals:** Total Employees, Attrition %, Average Salary  
- **Pie Chart:** Employees by Department  
- **Stacked Bar Chart:** Employees by Job Level and Department  

---

### **2️⃣ Employee Performance 🚀**  
✔️ **KPIs:** Performance Rating, Training Hours, Work-Life Balance Score  
✔️ **Visuals:**  
- **Bar Chart:** Average performance rating per department  
- **Heatmap:** Performance trends by job role  
- **Line Chart:** Training hours vs. job satisfaction  

---

### **3️⃣ Attrition Analysis 📉**  
✔️ **KPIs:** Attrition Rate, Resignation Reasons, Exit Trends  
✔️ **Visuals:**  
- **Pie Chart:** Reasons for leaving (Low Salary, Workload, Career Growth, etc.)  
- **Bar Chart:** Attrition by department and tenure  
- **Line Chart:** Monthly attrition trend  

---

### **4️⃣ Demographics & Diversity 🌍**  
✔️ **KPIs:** Employee Age Distribution, Gender Diversity, Tenure  
✔️ **Visuals:**  
- **Bar Chart:** Employees by age group  
- **Pie Chart:** Gender diversity %  
- **Stacked Column Chart:** Employee tenure distribution  

---

### **5️⃣ Compensation & Benefits 💰**  
✔️ **KPIs:** Average Salary, Salary Distribution, Benefits Utilization  
✔️ **Visuals:**  
- **Gauge Chart:** Average salary vs. industry benchmark  
- **Histogram:** Salary distribution by department  
- **Bar Chart:** Employees using benefits (Health, Education, Retirement, etc.)  

---

### **6️⃣ HR Business Insights 💡**  
✔️ **KPIs:** Overall Workforce Engagement, High-Risk Employees  
✔️ **Visuals:**  
- **Gauge Chart:** Workforce engagement score  
- **Heatmap:** Employee satisfaction by department  
- **KPI Cards:** Key HR takeaways  

---

## **📌 Key Insights & Recommendations**  

### **📈 Workforce Performance & Engagement**  
✅ **Low job satisfaction affects retention**—enhance career growth programs.  
✅ **Departments with high attrition need better employee engagement strategies.**  

### **📉 Attrition Reduction Strategies**  
✅ **Most employees leave due to salary and career growth issues**—introduce performance-based incentives.  
✅ **Work-life balance impacts attrition**—flexible working hours can improve retention.  

### **👥 Diversity & Inclusion**  
✅ **Gender diversity is improving** but needs more efforts in leadership roles.  
✅ **New hires from diverse backgrounds contribute to innovation and performance.**  

### **💰 Compensation & Benefits**  
✅ **Salary disparities exist across departments**—ensure fair pay policies.  
✅ **Employees highly value health and retirement benefits**—increase awareness and usage.  

---

## **🚀 Future Enhancements**  
📌 Add **predictive analytics** to forecast employee attrition risk.  
📌 Implement **AI-based sentiment analysis** on employee feedback.  
📌 Expand **HR analytics with recruitment efficiency metrics**.  

---

## **📥 How to Use This Power BI Report**  
### **🔹 Steps to View & Analyze Data**
1. Download the **Power BI report file** (`HR Analytical Dashboard.pbix`).  
2. Open **Power BI Desktop** (latest version recommended).  
3. Load the dataset (`HR_Dataset.csv`) if required.  
4. Explore the **dashboard pages**, apply filters, and analyze trends.  

---

## **📩 Contact & Support**  
If you have any questions or feedback, feel free to reach out!   
📧 Email: **harshrana8460@gmail.com**  
💬 LinkedIn: **https://www.linkedin.com/in/harsh-data-analyst** 
---
### Contact No: +91 8460199614 (Harsh Rana)
---

**⭐ If you found this project useful, don’t forget to star this repository on GitHub!** 🚀✨  

---
