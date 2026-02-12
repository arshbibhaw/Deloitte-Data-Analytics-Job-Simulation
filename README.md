# 📊 Daikibo Analytics Job Simulation – Complete Implementation Guide

Welcome to the comprehensive guide for the Deloitte Data Analytics Job Simulation on Forage. This step-by-step walkthrough will help you successfully complete both analytical tasks using industry-standard tools like Tableau and Excel.

---

## ✅ Task 1: Machine Downtime Analysis Using Tableau

### 🎯 Objective
Analyze telemetry data to identify patterns in machine downtime and answer critical business questions:
- Which facility experienced the highest frequency of machine failures?
- Which equipment types were most prone to breakdowns at that location?

### 🔧 Implementation Steps

#### 1. Set Up Tableau Environment
- Navigate to [Tableau Free Trial](https://www.tableau.com/products/trial)
- Register using your email address and download the installation package
- Complete the installation process

#### 2. Import Telemetry Data
- Locate and download `daikibo-telemetry-data.json.zip` from the resource section
- Extract the compressed file
- Launch Tableau and select **Connect → JSON File**
- Import the extracted `daikibo-telemetry-data.json` file

#### 3. Build a Calculated Field for Downtime Measurement
- Access the **Data Pane** and right-click to select **Create Calculated Field**
- **Field Name:** `Unhealthy`
- **Formula:**
  ```
  IF [Status] = "Unhealthy" THEN 10 ELSE 0 END
  ```
  *This calculation assigns 10 minutes of downtime for each "Unhealthy" status entry*

#### 4. Develop Visualization: Factory Downtime Comparison
- Create a new worksheet
- Drag **Factory** dimension to the Columns shelf
- Drag **Unhealthy** measure to the Rows shelf
- Configure aggregation as **SUM**
- Apply descending sort by total downtime
- **Rename worksheet:** "Down Time per Factory"

#### 5. Develop Visualization: Equipment Type Analysis
- Create another worksheet
- Drag **Device Type** to Columns
- Drag **Unhealthy** to Rows (using SUM aggregation)
- Apply factory-specific filters as needed
- **Rename worksheet:** "Down Time per Device Type"

#### 6. Create an Interactive Dashboard
- Select **New Dashboard** from the menu
- Drag both worksheets onto the dashboard canvas
- Enable interactive filtering by right-clicking the factory chart and selecting **Use as Filter**
- Test interactivity: clicking on a factory bar should dynamically update the device type chart

#### 7. Document and Submit Results
- Select the factory with maximum downtime
- Capture a screenshot of the complete dashboard view
- Save and submit according to project requirements

---

### 🧪 Expected Output Structure

| Factory | Total Downtime (minutes) |
|---------|-------------------------|
| Meiyo | 32,000 |
| Seiko | 28,900 |
| Shenzhen | 22,500 |
| Berlin | 19,200 |

---

### 📊 Analytical Insights and Business Implications

#### 🔍 Key Findings:

**Facility-Level Performance:**
- **Daikibo-Factory-Seiko** recorded the highest downtime with 480 unhealthy status incidents, indicating critical operational challenges requiring immediate attention
- **Daikibo-Shenzhen** ranked second with 420 incidents, suggesting potential maintenance protocol deficiencies
- **Daikibo-Factory-Meiyo** demonstrated moderate performance with 110 downtime incidents
- **Daikibo-Berlin** exhibited exceptional reliability with only 20 incidents, representing best-in-class operational excellence

**Equipment-Level Performance:**
- **Laser Welder** emerged as the most problematic asset with 480 downtime incidents, followed closely by the **Laser Cutter** at 430 incidents
- Secondary contributors include **Heavy Duty Drill** (70 incidents) and **Furnace** (20 incidents)
- **Metal Press** and **Air Wrench** achieved zero downtime, demonstrating superior reliability metrics

#### 📌 Strategic Recommendations:
- Prioritize maintenance interventions for Laser Welder and Laser Cutter equipment across all facilities
- Conduct root cause analysis at Seiko and Shenzhen facilities to identify systemic issues
- Implement best practices from Berlin operations across the entire manufacturing network
- Develop predictive maintenance schedules for high-risk equipment categories
- Consider equipment lifecycle assessment for assets with persistent reliability issues

---

## ✅ Task 2: Equality Classification Analysis in Excel

### 🎯 Objective
Generate a classification system to categorize equality scores into meaningful business categories based on predefined thresholds.

### 🧰 Required Tools
- Microsoft Excel (Desktop or Online)
- Alternative: Google Sheets

### 🔧 Implementation Steps

#### 1. Access the Dataset
- Open the provided file: `Equality Table.xlsx` (renamed as - Raw_Equality_Table.xlsx)
- Review the existing data structure

#### 2. Create Classification Column
- Navigate to **Column D**
- Enter header: **Equality Class**

#### 3. Implement Classification Logic
- In cell **D2**, enter the following formula:
  ```excel
  =IF(ABS(C2)>20, "Highly Discriminative", IF(ABS(C2)>10, "Unfair", "Fair"))
  ```
  *This nested IF statement evaluates the absolute value of equality scores to assign appropriate classifications*

#### 4. Apply Formula to Dataset
- Select cell D2
- Drag the fill handle down to apply the formula across all data rows

#### 5. Validate Results
Verify classification accuracy with sample checks:
- Score of **-25** → "Highly Discriminative" ✓
- Score of **-15** → "Unfair" ✓
- Score of **5** → "Fair" ✓

#### 6. Save Final Output
- Save the updated file as: `Submitted_Equality_Table.xlsx`

### 🧾 Sample Output Preview

| Factory | Job Role | Equality Score | Equality Class |
|---------|----------|----------------|----------------|
| Daikibo Meiyo | C-Level | -25 | Highly Discriminative |
| Daikibo Seiko | Manager | -21 | Highly Discriminative |
| Daikibo Shenzhen | Engineer | 4 | Fair |

**✅ Verify your output matches this structure before submission**

---

## 📌 Pre-Submission Checklist

| Task Component | Requirement | Status |
|----------------|-------------|--------|
| Task 1 | Interactive dashboard created in Tableau | ✅ |
| Task 1 | Screenshot captured with applied filters | ✅ |
| Task 2 | Classification formula correctly implemented | ✅ |
| Task 2 | Updated file saved with Equality Class column | ✅ |

---

## 📄 [View My Completion Certificate](Deloitte_Data_Analytics_Certificate.pdf)

---

## 🙌 About This Guide

This comprehensive implementation guide was developed by **Aakarsh Bibhaw**, a data analytics professional passionate about making data analytics education accessible to aspiring analysts worldwide.

### 📍 Connect & Collaborate:

- **🔗 GitHub:** [github.com/arshbibhaw](https://github.com/arshbibhaw)
- **💼 LinkedIn:** [linkedin.com/in/aakarsh-bibhaw](https://www.linkedin.com/in/aakarsh-bibhaw/)

---

*If this guide helped you succeed in your simulation, please consider starring the repository and sharing it with others pursuing careers in data analytics!* ⭐