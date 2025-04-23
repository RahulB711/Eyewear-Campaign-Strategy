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






