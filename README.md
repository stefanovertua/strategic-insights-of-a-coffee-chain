# STRATEGIC INSIGHTS OF A COFFEE CHAIN: ENHANCING PROFITABILITY AND EFFICIENCY

## Overview

This document provides an analysis of key performance data for a prominent U.S.-based coffee chain with locations spanning 20 states. <br>

Metrics reviewed include sales, costs, profits, and inventory across multiple locations. <br>

The analysis addresses the following objectives:
+ Evaluating the database structure
+ Calculating sales, profits, COGS, and expenses
+ Analyzing metrics such as sales and profits by market size and region
+ Identifying trends, consumer preferences, and changes over time
+ Delivering actionable recommendations to the company stakeholders

The analysis was conducted using PostgreSQL and Microsoft Excel for data visualization. <br>
The dataset used in this analysis can be downloaded at this [link](https://www.kaggle.com/datasets/amruthayenikonda/coffee-chain-sales-dataset/data).

The SQL code is available [here](Coffee_Dataset_Analysis_SQL_Code.txt).

## **Table of Contents** <br>
- [Dataset](#dataset) <br>
- [Analysis](#analysis)
- [Executive Summary](#executive-summary)
- [Recommendations](#recommendations)
- [Limitations](#limitations)

## Dataset

This dataset, sourced from Kaggle, a widely recognized platform offering copyright-free datasets, contains a single sheet with 21 columns, covering orders from late 2012 through Q3 2015. 

Key metrics include:
+ COGS (Cost of Goods Sold): This is the total expenditure incurred by the coffee chain in producing or purchasing its products, such as coffee, tea, and other items. Monitoring COGS is essential to understanding the true cost of sales and directly impacts the gross profit.
+ Difference between Actual and Target Profit: This attribute indicates the performance gap between the actual profit achieved and the target profit goal. A positive difference means the coffee chain exceeded its profit goals, while a negative one highlights areas where targets were not met, offering insight into the financial performance relative to expectations.
+ Date: The date of each sales transaction, allowing for chronological tracking of sales.
+ Inventory Margin: This metric reflects the profitability of inventory by showing the difference between the costs of maintaining or storing inventory and the revenue generated from selling it. 
+ Margin: This measures the overall profitability of the firm.
+ Market Size: This attribute provides information on the size of the 20 markets, equivalent to the 20 US States where the firm operates. 
+ Profit: This is the net financial gain achieved after deducting the COGS and other operational expenses from the revenue generated. It represents the company's overall earnings and it’s a fundamental measure of financial health and success.
+ Sales: Sales reflect the revenue generated from selling the coffee chain’s products, serving as a direct indicator of financial performance and customer demand. Analyzing sales trends can help in understanding consumer preferences, identifying best-selling products, and adjusting inventory accordingly.

The dataset also categorizes the 20 U.S. States into four regions—West, Central, East, and South—and classifies markets as Major or Small based on the state population.

The dataset met a high standard of accuracy, and no further data cleaning was needed.

## Analysis

I began by importing the Excel dataset and reviewing its structure and contents.

The dataset includes two product lines, Leaves and Beans, across four categories: Coffee, Herbal Tea, Espresso, and Tea, comprising 13 distinct products: Amaretto, Caffe Mocha, Earl Grey, Colombian, Caffe Latte, Chamomile, Mint, Decaf Irish Cream, Green Tea, Lemon, Regular Espresso, Decaf Espresso, and Darjeeling.

The average figures per transaction for key metrics are as follows:
+ Sales: $191.05
+ COGS: $82.40
+ Expenses: $53.84
+ Profit: $60.56
  
Given that we have information on market size and orders segmented by market type, I leveraged this data to analyze sales, profits, and other metrics across different market sizes and regions. Below is a summary, with all values expressed in U.S. Dollars.

![picture1](https://github.com/user-attachments/assets/f7d95b9c-3b84-4cf5-aa83-9d3650d0e267)

Interestingly, major markets do not necessarily correlate with higher sales or profits. Additionally, each year, no state (except for Texas) appears twice in the ranking of top-selling states. See the chart below for details.

![image5](https://github.com/user-attachments/assets/7c44a418-ea5e-4be3-9f22-707a9da50828)


The following are the top and bottom five states by profit. As with sales, there is no apparent geographical correlation or consistent pattern regarding market size, demographic composition, or cultural region. However, there are significant profit differences among states. For example, the combined profits of the bottom five regions are still 20% lower than those of Illinois, the highest-performing state.


![image](https://github.com/user-attachments/assets/f6899486-f35c-477b-a768-c9134bb1cd17)




Having analyzed the geographical distribution, I could now assess the product lines, focusing on sales and profits for each. The results, ranked by profits, indicate that Colombian coffee from the Beans product line has both the highest sales and the highest profits. <br>
I suggest continuing to promote Colombian coffee, as it excels in both metrics. However, it would be worthwhile to explore whether further promotion could lead to saturation in the market.

There is a significant disparity between the top products, both in terms of sales and profits, and those at the bottom. 

Interestingly, Regular Espresso, despite ranking last in sales, performs average in profits, indicating strong profitability potential. Regular Espresso has comparable profits to Decaf Irish Cream, despite selling nearly half as much.

![image1](https://github.com/user-attachments/assets/6492f715-e02b-4756-92b4-13f00db5e6b8)


When sales are broken down by product, there is a relatively equal distribution across both the product lines and individual products. This balanced distribution suggests that no single product or line dominates sales, indicating a diverse customer preference for various offerings.


![Screenshot 2024-11-03 215918](https://github.com/user-attachments/assets/f2242855-e62a-4eab-9c6e-fa8d77f6ddfc)
![Screenshot 2024-11-03 215907](https://github.com/user-attachments/assets/d58d2171-72e9-4faf-b992-29923e0f3f61)


Having previously focused on product performance, I could now evaluate the company’s overall performance against its targets. 
The graph below, enhanced with conditional formatting for clarity, illustrates the results. All values are presented in U.S. Dollars.

In terms of sales, out of 16 entries, only 4 underperformed. Notably, the results from the Leaves product line in the West region are particularly positive. All Leaves products reported positive sales, and most also showed good profit margins, with only a few experiencing marginal losses. <br>
<br> However, only 7 of the 16 entries show overperformance in terms of profits, signaling a need for attention. The performance of Beans in the Central region is concerning, while Leaves continue to thrive. This suggests a need for a strategic change—whether that involves focusing more on the market, withdrawing certain products, or investigating the root causes of underperformance.

Nonetheless, it is encouraging that all products recorded profits.

![picture7](https://github.com/user-attachments/assets/1820a76d-277d-45e8-aeea-65d1b78f8e0d)


Below is the graph depicting the change in profits over time.

Profits plateaued from the beginning of the dataset until the end of 2013. However, a remarkable spike was recorded thereafter. <br>
The last two quarters, however, have shown a significant decline. Despite this decline, profits in Q3 2015, while less than half of the peak reached in Q3 2014, still surpassed any quarter in 2012 and 2013. Notably, profits in 2015, despite missing a quarter, are more than double those in 2013 ($21,954 vs. $9,484).

Since the lowest point in Q3 2013, the company has demonstrated steady improvements for a year. In fact, Q3 2014 alone recorded more profits than the entire year of 2013.

The company has consistently generated profits since the beginning, totaling $64,311 over the analyzed period.

![picture8](https://github.com/user-attachments/assets/bf46601a-4399-4f08-92c1-5c1ceee310d9)

The next chart illustrates the difference between actual and targeted profits by state. Out of the 20 states analyzed, 11 underperformed while 9 exceeded their targets. 
The top three outperforming states are Iowa, New York, and California.

![picture9](https://github.com/user-attachments/assets/0fcd1989-9f32-481c-b00a-008099d4a9a3)

Finally, it is crucial to investigate whether the expenses are effectively contributing to profits in order to evaluate our strategy. To this end, I analyzed the correlation between total expenses, profit, and sales across different markets and product lines. 

![picture10](https://github.com/user-attachments/assets/9029a14d-c160-4e31-ad3f-4fd4cd000d87)

## Executive Summary

+ The coffee chain offers a diverse but focused product range, with 2 product lines encompassing 4 product types and 13 distinct products, allowing for targeted marketing and streamlined operations while still providing variety to customers. This is an asset, meaning that the firm can leverage several different products to target different tastes and demographic sectors. Notably, all product types and lines exhibit nearly equal popularity.
+ With an average profit of $60.56 per transaction and a healthy profit margin (average profit / average sales = 31.7%), the coffee chain appears to be operating efficiently, though there may be room to optimize expenses (28.2% of sales) to further improve profitability.
+ The firm has achieved more sales targets than profit targets overall. This discrepancy suggests that there may be underlying challenges in translating that revenue into actual profits.
+ The West region, particularly in Small Markets, consistently outperforms other regions in total sales ($67,418) and average margin (160.42%), suggesting a strong market presence and efficient operations in this area. However, it also has the highest average COGS ($149.28), indicating potential for cost optimization to further improve profitability.
+ High COGS in specific locations may highlight inefficiencies in supply chain logistics or supplier pricing. The COGS showed an upward trend each year, suggesting the need for optimizing procurement and production processes.

## Recommendations

The recommendations are organized into three key areas: products, markets, and operational efficiency.

**Products**
+ Colombian beans stand out as the clear leader in both total sales ($30,761) and total profit ($12,932) across all products, indicating it's a key driver of the coffee chain's success. This suggests focusing on promoting and potentially expanding the Colombian beans offering could significantly boost overall profitability. In addition to this, there's a notable performance gap between top performers and lower-ranking products like Green Tea, highlighting the need for a strategic review of the product mix to potentially optimize or phase out underperforming items. 
+ Across multiple products, the data reveals distinct seasonal trends and fluctuating profitability, with notable spikes in sales for products like Regular Espresso, Earl Grey, and Colombian during mid to late 2014 and 2015. These patterns suggest potential opportunities for targeted promotions or product launches during these peak periods, while also highlighting periods of declining sales and profits that may require strategic adjustments to maintain profitability and market share.
  
**Markets**
+ The data reveals a significant performance variance across market sizes and product lines. In Major Markets, both Leaves and Beans consistently outperform their targets, with higher profit-expense and sales-expense ratios. However, in Small Markets, while Leaves maintain strong performance (0.87 profit/expense ratio), Beans underperform (0.79 ratio). This suggests that the company should focus on understanding and replicating the success factors from Major Markets, particularly for Beans products, to improve performance in Small Markets and optimize resource allocation.
+ It’s crucial to focus on high-performing regions for expansion opportunities or additional resource investment. By directing resources where demand and profitability are strong, the company can maximize its return on investment. On the other hand, other areas reveal lower profitability, often due to high operational costs or lower customer demand. These regions may benefit from strategies such as adjusting product mixes, improving cost efficiencies, or targeted marketing efforts to boost sales. For underperforming regions, assess the feasibility of revitalization efforts versus potential divestment if long-term prospects seem limited.
  
**Operational efficiency**
+ For the company’s Financial Department, I would investigate and renegotiate with suppliers for high COGS areas to reduce costs and boost profitability. I would evaluate current supplier agreements and explore ways to reduce expenses, especially for high-cost locations. In addition to supplier negotiations, I’d recommend implementing more efficient logistical practices, such as centralized procurement or collaborative buying, to cut down on operational costs where feasible. A cost monitoring system may be needed to track high COGS locations.
+ It’s key to streamline inventory based on sales trends and demand forecasting to improve margins in lower-performing areas. Trends around inventory margin indicate certain locations manage stock effectively, minimizing waste and maximizing sales relative to stored items. Areas with low inventory turnover may need better demand forecasting or inventory adjustments.

In conclusion, a thorough analysis of the coffee chain's sales data has provided valuable insights into sales trends, product performance, and cost management. <br>
<br> Leveraging these insights and implementing the recommendations can significantly contribute to the coffee chain's growth, profitability, and overall success.

## Limitations

Although the study provides useful information, it is subject to a couple of limitations.
+ The dataset lacks data on specific purchase times throughout the day. Knowing this information could help analyze when peak sales times are, and consequently adjust staffing accordingly, in order to reduce labor costs during off-peak hours.
+ A more detailed market analysis is needed to provide better recommendations. It’s therefore necessary to conduct deeper research into customer preferences and competitor activity in high-performing regions to understand the drivers of success. 


