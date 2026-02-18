# Bike-sales-Analysis-dashboard---Excel
        BIKE SALES ANALYSIS DASHBOARD — EXCEL 

  

INTRODUCTION: 

The Bike Sales Analysis project is a data-centric initiative designed to bridge the gap between raw datasets and strategic business decision-making within the bicycle industry. By leveraging Microsoft Excel for advanced analytical tools, the project systematically processes customer information — such as income levels, commute patterns, and age — to uncover the key drivers behind bike purchases.  

In a 2025 market characterized by a growing shift toward eco-friendly commuting and e-bike adoption, understanding these consumer nuances is essential for staying competitive. This project serves as a practical demonstration of the data lifecycle, starting with rigorous cleaning to ensure data integrity, followed by transformation and interactive visualization. Ultimately, it provides stakeholders with a dynamic dashboard that simplifies complex demographic trends into clear, actionable insights for targeted marketing and inventory optimization. 

OBJECTIVE: 

Perform End-to-End Data Cleaning: Identify and remove duplicate records, standardize categorical entries (e.g., converting ‘M’ to ‘Married’ and ‘F’ to ‘Female’), and resolve formatting inconsistencies to ensure high data integrity for analysis.  

Analyze Consumer Demographics: Identify high-conversion customer segments by examining the relationship between bike purchases and demographic factors such as average income, gender, and marital status.  

Evaluate Lifestyle and Behavioral Drivers: Quantify how external factors, specifically commute distance and the number of cars owned, influence a customer’s propensity to buy a bicycle.  

Implement Data Segmentation: Enhance raw data granularity by creating custom metrics, such as Age Brackets (Adolescent, Middle Age, Old), to uncover non-obvious purchase patterns across different life stages.  

Develop an Interactive Dashboard: Build a dynamic visualization tool using Pivot Tables, Slicers, and Charts that allows stakeholders to filter sales trends by region, education level, and occupation in real-time for data-driven decision-making.  

DATA SOURCE & DATA PREPARATION: 

This dataset was sourced from Kaggle and contains 1027 rows of customer data related to bike purchases. It includes demographic attributes such as age, income, marital status, education level, and occupation, as well as homeownership, commute distance, and car ownership. 

The13 Columns of the bike sales data 

The dataset provides valuable insights into consumer behavior, helping to analyze who is more likely to purchase a bike based on lifestyle, financial status, and commuting habits. This structured dataset allows for effective data visualization and business intelligence analysis to inform marketing strategies and operational decisions. 

This project involved multiple steps, from data preparation and cleaning to analysis and visualization, ensuring an effective and structured approach to extracting insights. Below is the detailed process: 

Data Cleaning and Data Formatting 

Created Pivot table and Built Recommended Chart based on pivot table 

Created Slicers 

Finally built interactive dashboard 

DATA CLEANING AND TRANSFORMATION: 

To ensure data quality and consistency for analysis, several cleaning steps were performed: 

i. Identified and removed duplicate records using Excel’s ‘Remove Duplicates’ feature to enhance data integrity. 

Select whole data →Data →Remove duplicates 

 

Selected full data (CTRL+A) 

Select All 

Removed Duplicates 

26 duplicates found and removed 

1000 unique values remain 

ii. Standardized categorical variables (Marital Status and Gender) using ‘Find and Replace’ (Ctrl+H) to improve readability, user-friendliness and consistency in reporting. 

Marital Status column- where Married is denoted by M and Single is by S , so we need to replace it with right name because in later stage it may confuse viewers with Gender Column. 

For example, I replaced the following: 

‘m’ in “Marital Status” is replaced with “married” 

‘s’ in “Marital Status” is replaced with “single” 

‘m’ in “Gender” is replaced with “male” 

‘f’ in “Gender” is replaced with “female” 

Select column →CTRL+H(Find and Replace) 

M →Married 

S →Single 

Gender column- Similarly like above do Ctrl+H and name it as Male instead of M and Female instead of F for better understanding of viewers. 

F →Female 

M →Male 

iii. Income column- change the format(removing the decimal point) Reviewed and ensured consistency in the ‘Income’ column’s currency format. 

Income : Removing the decimal points 

iv. Addressed potential sorting issues in the ‘Commute Distance’ column by standardizing the ‘More than 10 miles’ category which improves sorting in the pivot table. 

v. Created a new column named “Age Brackets” to group individual ages into broader categories for more meaningful visualizations. 

vi. Next, I assigned age brackets based on the “Age” column using a nested IF statement. For example: 

If Age is less than 31, the “Age Bracket” is “adolescent” 

If Age is greater than or equal to 31 and less than or equal to 54, the “Age Bracket” is “middle age” 

If Age is greater than 54, the “Age Bracket” is “old” 

=IF(L3>54,” Old”, IF(L3>=31,” Middle Age", IF (L3< 31, “Adolescent", "Invalid”))) 

Age Bracket 

CREATE PIVOT TABLE AND RECOMMENDED CHARTS: 

Purpose of Pivot Tables 

Pivot tables were utilized to aggregate and summarize the cleaned data, enabling the extraction of key relationships and trends. This powerful Excel feature allows for dynamic data exploration and the creation of insightful summaries. 

Select Table/Range →whole cleaned data (Worksheet) 

Pivot table creation 

1st Pivot table: Average income of Male and female who purchased bike or not. 

 

Pivot Table 1: Average Income by Gender and Purchase Status 

Analytical Objective 
	The goal was to examine the relationship between customer demographics (specifically gender) and purchasing behavior, with a focus on income. The analysis aimed to identify patterns in average income based on gender and whether or not a customer purchased a bike. 

Pivot Table Configuration 

Rows: Gender (Female, Male) 

Columns: Purchased Bike (Yes, No) 

Values: Income (calculated as Average) 

Key Insights 

Among those who did not purchase a bike, the average income was $53,440 for females and $56,208 for males. 

Among those who did purchase a bike, the average income rose to $55,774 for females and $60,124 for males. 

The data indicates a trend where individuals with slightly higher incomes are more likely to purchase bikes. 

Additionally, males consistently have a higher average income than females across both buyer groups. 

 

2nd Pivot table: Purchase of Bike on basis of distance 

 

Pivot Table 2: Customer commute distance and Bike purchase count 

Analytical Objective 
	This analysis aimed to explore the potential relationship between a customer’s commute distance and their likelihood of purchasing a bike. The goal was to identify which distance groups are more or less likely to make a bike purchase. 

Pivot Table Configuration 

Rows: Commute Distance (0-1 Miles, 1-2 Miles, 2-5 Miles, 5-10 Miles, More than 10 Miles) 

Columns: Purchased Bike (Yes, No) 

Values: Count of Records (each row representing a customer) 

Key Insights 

The highest number of customers, regardless of bike purchase, falls within the 0–1 Miles commute distance category. 

To ensure accurate sorting in the visualization, the “More than 10 miles” category was adjusted for consistency and clarity. 

The resulting pivot table and visualization help reveal purchase trends by commute distance, offering insight into how distance from work or school may influence the decision to buy a bike. 

3rd Pivot table: Purchase of bike on basis of age, gender, Marital status. 

 

Pivot Table 3: Home ownership, Gender, Marital status and Bike purchase count 

Analytical Objective 

This analysis explores how personal demographics and living situations influence purchasing behavior. By cross-referencing home ownership, gender, and marital status, the goal is to identify high-conversion segments and determine if stability (home ownership/marriage) correlates with bike ownership. 

Pivot Table Configuration 

Rows: Homeowner (Yes, No), Marital Status (Married, Single) 

Columns: Gender (Male, Female), Purchased Bike (Yes, No) 

Values: Count of Customer ID (or Count of Records) 

Filters (Optional): Region or Education (to further drill down into specific markets) 

Key Insights 

Stability and Purchasing: Analyze whether homeowners — who may have more storage space for a bike — show higher purchase rates compared to non-homeowners. 

Gender Parity: Evaluate if there is a significant “gender gap” in bike purchases across different marital statuses. 

Marital Status Influence: Identify if single individuals are more likely to purchase bikes for commuting/leisure compared to married individuals, or vice versa. 

Target Segment: This table helps marketing teams decide whether to tailor advertisements toward “Active Singles” or “Outdoor-Oriented Families”. 

4th Pivot table: Purchase of bike on basis of age 

 

Pivot Table 4: Customer Age Brackets and Purchase Count 

Analytical Objective 
	This analysis examined how purchasing behavior varies across different age groups by segmenting customers into defined age brackets. The aim was to uncover patterns in bike purchases based on age demographics. 

Pivot Table Configuration 

Rows: Age Bracket (Adolescent, Middle Age, Old) 

Columns: Purchased Bike (Yes, No) 

Values: Count of Records (each representing one customer) 

Key Insights 

The “Middle Age” group (ages 31–54) had the highest number of bike purchases, indicating a stronger interest or ability to buy within this segment. 

The “Adolescent” group (under 31 years) showed the lowest count of bike purchases. 

Segmenting the data into age brackets made it easier to identify trends and compare purchasing behavior than using raw individual ages. 

 

5th Pivot table: Income by Region and Purchased bike 

 

Pivot Table 5: Income by Region and Purchased Bike 

Analytical Objective 

This analysis aimed to determine the relationship between a customer’s geographic location (Region) and their average income, and how these two factors together influence the likelihood of purchasing a bike. The objective was to identify if higher income levels, regardless of region, correlate with increased bike purchases. 

Pivot Table Configuration 

Rows: Region (Europe, North America, Pacific) 

Columns: Purchased Bike (Yes, No) 

Values: Average of Income 

Filters (Applied implicitly): None visible in the provided image. 

Key Insights 

Income as a Predictor: A strong positive correlation is observed: customers who purchased a bike consistently had a higher average income than those who did not purchase a bike in all three regions. 

Regional Disparities: Average incomes in North America and the Pacific regions (\$60k+) are significantly higher than in Europe (\$40k+). 

Overall Trend: The highest overall average income corresponds to the North America and Pacific regions. The “Yes” category for bike purchases has a higher overall average income (\$57,963) compared to the “No” category (\$54,875). 

CREATE SLICER: 

Slicer- are visualization that allow viewers to refine the data for themselves 

Steps to create Slicer: 

Click anywhere on the table or PivotTable. 

On the Insert tab, select Slicer. 

In the Insert Slicers dialog box, select the check boxes for the fields you want to display, then select OK. 

A slicer will be created for every field that you selected. 

With the following steps, created 3 slicers i.e. Marital Status, Home ownership and Region. 

 

Slicers: Marital Status, Home ownership and Region 

BUILD INTERACTIVE DASHBOARD: 

Charts which we prepared during pivot table brought at one place and put slicers and choose design to give it a look -which gives an overall very decent interactive dashboard. 

Bike sales analysis dashboard 

The provided dashboard offers several key insights into bike sales across different customer demographics and regions: 

Overall Performance Summary 

The business has generated a robust \$56,360,000 in total sales from 1000 units sold to 1000 customers. The overall average customer income is \$56,360. 

Key Analytical Insights 

Income and Purchase Behavior 

Income Correlation: There is a clear positive correlation between income and bike purchase likelihood. In every region and across gender groups, customers who purchased a bike consistently reported a higher average income than those who did not. 

Gender and Income: Average income is slightly higher for males (\$56,208) than females (\$55,774), with male buyers showing a particularly high average income (\$60,124). 

Customer Demographics 

Age Bracket: The highest concentration of sales volume comes from the Middle Age customer bracket (383 units sold), followed by Adolescents (around 130–150 units). The ‘Old’ age bracket has the lowest volume. 

Customer Profile (Segmentation): The largest segments of customers are Female Married No (homeowner) at 58.6% and Male Married No (homeowner) at 39.4%. However, the actual purchase counts vary, indicating specific high-value segments. 

Regional Analysis 

Top Regions: North America and the Pacific regions drive the highest average incomes (around \$63k–\$65k) and likely the bulk of high-value sales, given their high average income per purchase. 

Europe: This region has a significantly lower average income (around \$40k) compared to the others. 

Commute Distance 

Highest Volume: The majority of customers, regardless of purchase, fall into the 0–1 Miles commute distance category. 

Purchase Trends: While the 0–1 miles segment has the most customers, the chart shows various commute distances contribute significantly to purchases, with noticeable peaks in specific mileage brackets, indicating that commute need drives purchases. 

CONCLUSION AND KEY LEARNINGS: 

Project Summary 

This project transformed a raw bike sales dataset into a fully interactive Excel dashboard that offers clear insights into customer demographics and purchasing behavior. Key accomplishments included cleaning and preparing the data, using pivot tables to uncover trends, creating intuitive visualizations, and building a dynamic dashboard with slicers that allow users to filter and explore the data in real time. 

Excel Skills Demonstrated 

This project showcased proficiency in several essential Excel skills: 

Data Cleaning & Transformation: 
	Techniques such as removing duplicates, using ‘Find and Replace’ to standardize values (e.g., gender and marital status), and creating new columns (e.g., Age Brackets using nested IF formulas) were used to prepare the data for analysis. 

Pivot Table Creation & Manipulation: 
	Multiple pivot tables were developed to summarize data by gender, purchase behavior, commute distance, and age group. Value field settings were customized to calculate both averages and counts. 

Data Visualization: 
	Column and line charts were used to present key trends. Visuals were formatted with clear chart titles, axis labels, and clean number formatting (e.g., removing decimal places, adding commas) to enhance clarity and professionalism. 

Interactive Dashboard Development: 
	Slicers for Marital Status, Region, and Education were added to enable dynamic filtering. These slicers were connected to all pivot tables using the Report Connections feature, allowing users to explore specific customer segments and immediately see how the charts update based on their selections. 

Potential Improvements: 

To enhance the project further, future improvements could include: 

Integrating additional data sources, such as detailed sales metrics or product types. 

Creating calculated fields within pivot tables to derive new metrics (e.g., purchase rate per demographic). 

Leveraging Excel’s Power Query for more robust and automated data transformations. 

Refining the dashboard design with more advanced formatting or visual elements to improve user experience. 

 
 
