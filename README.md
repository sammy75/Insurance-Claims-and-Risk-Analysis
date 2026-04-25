# Insurance-Claims-and-Risk-Analysis
This project provides a detailed information about car insurance policyholders, their vehicles, and their claim history. 

<img width="1007" height="598" alt="image" src="https://github.com/user-attachments/assets/f002b7b2-3b59-4fd6-ae5e-0f48ff8f0f96" />
<img width="1008" height="595" alt="image" src="https://github.com/user-attachments/assets/2cd1d7d4-8f12-48eb-a593-6bdd36b139e9" />

BUSINESS REQUIREMENT
An insurance company is looking to better understand its policyholder base and claim patterns to make data-driven business decisions. Currently, policy and claims data are scattered across multiple sources, making it difficult for stakeholders to track performance and identify trends.
The company requires a centralized interactive dashboard in Power BI that can provide a clear overview of the following KPI's:

1.	Total Policies – to measure the size of the active customer base.
2.	Total Claim Amount – to track the overall financial impact of claims.
3.	Claim Frequency – to analyse how often claims are being made.
4.	Average Claim Amount – to assess claim severity and potential risk exposure.
5.	Gender-wise Total Policies – to understand customer distribution across genders for better segmentation and policy targeting.

Chart’s Requirements:
To deep dive into the data, we need to go beyond KPIs and analyse different aspects of insurance policies and claims. Charts help us visually explore patterns, relationships, and anomalies across customer demographics, car details, and claim behaviours. By analysing charts, stakeholders can identify risk factors, understand customer segments, and optimize policy decisions.
For this report, all visualizations are designed around two key dynamic measures:
•	Total Claim Amount
•	Total Policies

These measures provide the foundation to compare, filter, and segment the data effectively.
Visualization Requirements:
1.	By Car Use (Donut Chart) – To analyse policy distribution and claim amounts based on how cars are being used (e.g., personal, commercial).
2.	By Car Make (Bar Chart) – To identify which car brands have higher policies and claims, highlighting brand-based risks.
3.	By Coverage Zone (Donut Chart) – To evaluate policies and claims by geographic zones, useful for regional risk analysis.
4.	By Age Group (Frequency Chart/Histogram) – To assess policyholders’ age distribution and identify which age brackets file more claims.
5.	By Car Year (Area Chart) – To analyse how the car’s age (year of manufacture) impacts policy counts and claim amounts.
6.	By Kids Driving (Ribbon Chart) – To compare the impact of young drivers in households on policy count and claim amounts.
7.	By Education (Pie Chart) – To understand how education levels correlate with insurance policy adoption and claims.
8.	By Education & Marital Status (Matrix Heat Grid) – To explore the combined effect of education and marital status on policies and claims, highlighting customer profiles.

About the Dataset

https://1drv.ms/x/c/5189276a59c32115/IQCn4s9ijYpDSK6ykhYY6ypHAYpMOcjYULl7Q_PJ1qB-w_I?e=ZZuPwX

This dataset contains detailed information about car insurance policyholders, their vehicles, and their claim history. Each record represents an individual customer with demographic details such as birthdate, gender, marital status, education level, household income, and parental status. These attributes provide a strong basis for understanding customer profiles and how personal characteristics may influence driving behaviour and insurance risk.
The dataset also captures rich details about the insured vehicle, including car make, model, colour, year of manufacture, and usage type (personal, commercial, or commuting). Combined with the coverage zone, this information helps in assessing environmental and vehicle-related risk factors. For example, an older car used for commercial purposes in an urban area may carry a different risk profile compared to a new personal car in a rural zone.
On the financial and claims side, the dataset includes claim amount (total cost of claims filed), claim frequency (number of claims filed), and household income. These fields are critical in evaluating customer value and risk. High-frequency claimants may signal higher risk, while high claim amounts could indicate severe accidents or expensive repairs. The Kids Driving field adds another dimension, reflecting household driving behavior, since households with multiple young drivers are typically considered riskier by insurers.
Overall, this dataset offers a comprehensive view of customers, vehicles, and claims. It can be used to build Power BI dashboards for claims analysis, customer segmentation, risk profiling, and premium optimization. Insights derived from the data can help insurance companies design fairer pricing models, identify high-risk segments, detect potential fraud, and improve customer targeting strategies.

1. ID
   
•	Definition: A unique identifier assigned to each policyholder or insurance record.

•	Type: Numeric or text (Primary Key).

•	Details:
o	Ensures each policy/customer record is unique.
o	Not used directly in analysis but essential for data integrity, relationships, and avoiding duplicates.

•	Business Use: Helps track individual policyholders across multiple datasets (e.g., linking claims, payments, or renewals).

2. Birthdate
   
•	Definition: Date of birth of the policyholder.

•	Type: Date.

•	Details:
o	Used to calculate the Age of the policyholder.
o	Age is a strong factor in insurance risk assessment (younger drivers may have more accidents, older drivers may have slower reflexes).

•	Business Use:
o	Segment customers into age groups (e.g., <25, 25–40, 40–60, 60+).
o	Age-based pricing of premiums and risk profiling.

3. Car Color

•	Definition: The exterior color of the insured car.

•	Type: Categorical (text).

•	Details:
o	Although color doesn’t directly affect risk, it can influence car visibility, theft probability, and customer preferences.

•	Business Use:
o	Explore patterns (e.g., some studies suggest red cars might be involved in more speeding cases).
o	Insights for fraud detection (unusual color-claim patterns).

4. Car Make
   
•	Definition: The manufacturer/brand of the car (e.g., Toyota, Ford, BMW).

•	Type: Categorical.

•	Details:
o	Different makes have varying repair costs and accident likelihood.

•	Business Use:
o	Analyze claims by car brand.
o	Identify which brands have higher claim frequency (riskier) vs lower claims (safer).
o	Useful for underwriting and premium adjustments.

5. Car Model
   
•	Definition: Specific model of the car (e.g., Toyota Corolla, BMW X5).

•	Type: Categorical.

•	Details:
o	Provides deeper granularity beyond car make.
o	Claim risk can vary significantly between models of the same make.

•	Business Use:
o	Compare claims for luxury vs economy models.
o	Useful for loss ratio analysis by vehicle type.

6. Car Use
   
•	Definition: The primary purpose of the car (e.g., Personal, Commercial, Commute).

•	Type: Categorical.

•	Details:
o	Commercial and commuting cars usually have higher claim rates due to greater exposure (more time on the road).

•	Business Use:
o	Pricing policies differently for personal vs commercial use.
o	Risk profiling based on usage patterns.

7. Car Year
   
•	Definition: The manufacturing year of the car.

•	Type: Numeric.

•	Details:
o	Helps calculate Car Age = Current Year – Car Year.
o	Older cars may break down more often or have lower resale/repair costs.

•	Business Use:
o	Assess claim likelihood by vehicle age.
o	Create segments like New (<3 years), Mid-age (3–10 years), Old (>10 years).



8. Coverage Zone

•	Definition: The geographic risk area where the policyholder resides/uses the car (e.g., Zone A, Urban, Rural).

•	Type: Categorical.

•	Details:
o	Location impacts accident probability, theft risk, and repair costs.
o	Urban areas → higher claim frequency, rural areas → fewer accidents but possibly more severe damage.

•	Business Use:
o	Compare performance across regions.
o	Useful for mapping dashboards in Power BI.

9. Education
    
•	Definition: The highest education level attained by the policyholder (e.g., High School, Graduate, Postgraduate).

•	Type: Categorical.

•	Details:
o	Education level often correlates with income and risk behavior.

•	Business Use:
o	Check claim frequency by education group.
o	Insights for marketing campaigns and segmentation.

10. Gender
    
•	Definition: Gender of the policyholder (Male, Female, Other).

•	Type: Categorical.

•	Details:
o	Gender differences in claim patterns may exist.

•	Business Use:
o	Risk analysis by gender group.
o	Demographic breakdowns in dashboards.

11. Marital Status
    
•	Definition: Marital status of the policyholder (Single, Married, Divorced, etc.).

•	Type: Categorical.,

•	Details:
o	Married people are often seen as more stable, potentially lower risk.

•	Business Use:
o	Compare claims between singles vs married customers.
o	Factor in pricing and risk adjustment.

12. Parent
    
•	Definition: Whether the policyholder has children (Yes/No).

•	Type: Boolean / Categorical.

•	Details:
o	Parents may drive differently compared to non-parents.

•	Business Use:
o	Segment claims and policies by parent status.
o	Combine with Kids Driving for more detailed household analysis.

13. Claim Amt
    
•	Definition: Total monetary value of claims filed by the policyholder.

•	Type: Numeric (currency).

•	Details:
o	A critical measure of insurance losses.

•	Business Use:
o	Used to calculate total losses, average claim amount, and claim ratios.
o	Identify high-cost claims for fraud detection.

14. Claim Freq
    
•	Definition: The number of claims filed by the policyholder.

•	Type: Numeric (integer).

•	Details:
o	Frequency of claims indicates risk behavior.

•	Business Use:
o	KPI for customer risk assessment.
o	Combined with Claim Amt → identifies whether risk is due to high frequency or high severity.

15. Household Income
    
•	Definition: Annual income of the policyholder’s household.

•	Type: Numeric.

•	Details:
o	Income level affects affordability of premiums and vehicle type.

•	Business Use:
o	Segment customers into income bands.
o	Compare claim patterns across income groups.
o	Target marketing/policy offers (e.g., premium insurance for high-income households).

16. Kids Driving
    
•	Definition: Number of kids in the household who are licensed drivers.

•	Type: Numeric (integer).

•	Details:
o	Values (1, 2, 3…) indicate number of kids driving.
o	More kids driving generally = higher accident probability.

•	Business Use:
o	Analyze claims by number of kids driving.
o	Group into categories (e.g., None, 1 Kid, 2 Kids, 3+ Kids).
o	Helps insurers estimate family household risk.

