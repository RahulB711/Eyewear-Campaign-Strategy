# Eyewear-Campaign-Strategy
A data-driven project to optimize marketing spend across campaign segments using machine learning, simulation, and optimization.

## Problem Statement
The business wants to maximize either customer responses or revenue from marketing campaigns. Given a fixed budget of **$2M** and a mailing cost of **$0.25 per customer**, we aim to identify which segments (defined by product, milestone, month, customer group) to target to achieve the best ROI.

## Objectives
- Predict customer response probability
- Simulate ROI across response score thresholds
- Identify high-performing campaign segments
- Optimize budget allocation using linear programming
- Visualize insights and recommendations using Power BI

  ## Tools & Tech Stack
- Python (Pandas, Scikit-learn, PuLP)
- Excel (initial exploration)
- Power BI for dashboards
- GitHub for version control


  ## Project Workflow
  ### Day 1: Data Understanding & Preprocessing
- Explored the dataset structure
- Identified key columns like `RESPONSE_Rate`, `RESPONSE_SALES_AMT`
- Understood how campaign segments are defined

## Exploratory Data Analysis (EDA) :-Key Insight With Respect To Response_Rate

- 1. Effectiveness of Targeted Campaigns by Product Type
![image](https://github.com/user-attachments/assets/a5187140-0c84-4129-a4e7-d1f045f41823)
Product Type 1 received a significantly better response rate compared to Product Type 2


- 2. Average response rate by milestone
![image](https://github.com/user-attachments/assets/831cd695-8106-426f-8781-055a2fa7fd1e)
The 12-month milestone is receiving an exceptionally high response rate compared to the other durations


- 3. Response rate by target group
![image](https://github.com/user-attachments/assets/4fcefc5f-6741-4e24-a60a-7090f6033032)
The average response rate of the targeted group is only slightly higher—by around 0.2%—but given the context, this difference is considered significant.


- 4. Target vs Control response rate by campaign month
![image](https://github.com/user-attachments/assets/4edb259c-d26b-4876-9234-86ad9acb4947)
The response rates for the campaign months of December and January are significantly higher compared to the other months. Therefore, if we are planning to launch a new campaign, these months should be prioritized


### Day 2: Modeling & ROI Simulation
- Built a Random Forest Classifier to predict `response_flag`
- Scored all segments with `response_score`
- Simulated thresholds (1%, 5%, 10%, etc.) to evaluate ROI
- Visualized results in Power BI

 Top features from a logistic regression model
 ![image](https://github.com/user-attachments/assets/08a26d63-827c-4f93-b786-ca6001d24b9b)
 These features significantly influenced the model’s ability to predict positive responses. They also guided the optimization strategy by highlighting high-potential segments.

Top features from a Random Forest model
![image](https://github.com/user-attachments/assets/bac84e35-27ae-4ce5-9c6d-607dcd41b573)

Simulated thresholds (1%, 5%, 10%, etc.) to evaluate ROI
![image](https://github.com/user-attachments/assets/3361c167-6e91-4096-914b-a5cd27123832)

![image](https://github.com/user-attachments/assets/e5271ba6-e876-4666-9e77-2e68fe5aa44f)
We can clearly observe that the selected records and expected response begin to diverge after the 5% threshold. Based on both ROI and threshold analysis, there is a significant drop in ROI beyond the 5% mark, indicating diminishing returns

Campaign segment performance
![image](https://github.com/user-attachments/assets/5eb458d8-e62e-4dc3-be8f-d3548f013f92)
Scored Campaign Segments using a model (Random Forest) → response_score
The code in the snapshot generates a summary table of segment performance, which serves as a valuable tool for optimizing budget allocation

Dashboard
![image](https://github.com/user-attachments/assets/bc0adde4-9171-4dad-ac2e-6d36f41000b7)


Day 3: Optimization
- Aggregated data by segment
- Modeled the selection problem as a Knapsack optimization
- Used Python (`PuLP`) to maximize revenue under $2M budget
- Selected optimal segments and validated total cost and ROI

  ![image](https://github.com/user-attachments/assets/bbb404a3-dd0a-42e0-bef1-a14c2c1fb273)

Budget Constraint:
Total available budget: $2,000,000
Cost per customer mailed: $0.25
Total potential customers: 10,000,000
Mailing every customer would cost $2.5 million — which exceeds the budget.
By leveraging the response score, we can identify the individuals most likely to respond, and use linear optimization to select the most impactful segments

## Conclusion
Optimal segment selection cost: **$553.50**
- Expected revenue: **$23.75M**
- Expected responses: **1212 segments**
- Most value comes from a few high-efficiency segments



  



