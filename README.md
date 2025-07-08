# MitoSheet
## 🛠 Technologies Used  
- **Python**  
- `pandas` - Data manipulation and analysis  
- `mitosheet` - Interactive spreadsheet for data exploration  
- `numpy` - Numerical operations (implicitly used by pandas)  

## 📌 Key Steps Performed  

1. **Data Loading and Cleaning**  
   - Imported datasets:  
     - `Sleep_health_and_lifestyle.csv`  
     - `SalesTarget.csv` (multiple times)  
     - `survey.csv`  
   - Handled missing values in `Sleep Disorder` column by filling NaN with "No".  

2. **Data Transformation**  
   - Pivoted `Sleep_health_and_lifestyle` to analyze stress levels by occupation and physical activity.  
   - Split the `Blood Pressure` column into two separate columns (`САД` and `ДАД`) and converted them to float.  
   - Created a new binary column `Возраст старше 35` (Age over 35) based on the `Age` column.  

3. **Data Type Conversion**  
   - Converted columns to appropriate data types:  
     - `Stress Level`, `Heart Rate`, `Physical Activity Level`, `Daily Steps`, `Age` → float  
     - `Timestamp` and `Order Date` → datetime  

4. **Data Merging and Concatenation**  
   - Concatenated `SalesTarget` and `survey` dataframes.  
   - Attempted a merge between `SalesTarget` and `survey` on `Order Date`, filtering for unmatched entries.  

5. **Automated EDA (via MitoSheet)**  
   - Used `mitosheet` for interactive exploration and transformations, though the initial import failed due to a missing module.  

## 🔍 Observations  
- The script includes repetitive imports and operations (e.g., loading `SalesTarget.csv` three times).  
- The `mitosheet` dependency installation succeeded, but the module import failed, likely due to a kernel restart or environment issue.  
- The analysis focuses on health metrics (stress, sleep, blood pressure) and sales/survey data, but the two datasets are not directly integrated.  

## Suggested Next Steps  
- Resolve the `mitosheet` import issue to leverage its interactive features.  
- Combine health and sales data (if related) for deeper insights.  
- Add visualizations (e.g., using `matplotlib` or `seaborn`) to explore trends in stress levels or sales performance.
