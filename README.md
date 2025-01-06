# Car Sales Dashboard
### Car Sales Analysis **by Color** and **Brand** Dashboard using **Power BI**
<p align="left" style="margin-top: 20px; margin-bottom: 20px;">
<img width="40%" src="https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand/blob/main/images/car_sales.jpg" alt="car_sales"></img>
</p>

## Table of Contents:
- [Project Objectives](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand?tab=readme-ov-file#project-objectives)
- [Data Preparation](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand?tab=readme-ov-file#data-preparation)
- [Data Modeling](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand?tab=readme-ov-file#data-modeling)
- [Data Analysis (DAX)](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand?tab=readme-ov-file#data-analysis-dax)
- [Data Visualization (Dashboard)](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand?tab=readme-ov-file#data-visualization-dashboard)
- [Insights & Recommendations](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand?tab=readme-ov-file#insights--recommendations)


## Project Objectives:
- Analyze sales performance across products, customers, regions, and time periods.
- Identify key revenue drivers and profitability trends.
- Support strategic decision-making through data-driven insights.
- Improve inventory management and marketing strategies by understanding sales patterns.


## Data Preparation:
Data transformation was done in Power Query and the dataset was loaded into Microsoft Power BI Desktop for modeling.
- Ensure all columns are formatted correctly (e.g., numeric data as decimals, dates as date types).
- Handle missing or incorrect data using Power Query (replace, remove, or impute values).


## Data Modeling:
After the dataset was cleaned and transformed, it was ready to be modeled.
A star schema data model with the following relationships is shown below:

| Model view |
| ----------- |
|![model](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand/blob/main/images/modeling.png)|


This schema supports analytical queries, providing insights into:
- **Sales performance** by car attributes (`Make`, `Model`, etc.).
- **Client segmentation** based on demographics and behaviors.
- **Time-series analysis** for identifying trends and patterns.




1. Fact Table: `Sales`: stores transactional data; links to all dimension tables (`Cars`, `Clients`, `DateDimension`) through primary keys.
2. Dimension Tables:
    > - 2.1. `Cars`: contains detailed information about cars; linked to `Sales` via `CarID`.
    > - 2.2. `Clients`: provides client-related details; linked to `Sales` via `ClientID`.
    > - 2.3. `DateDimension`: captures date-related attributes; linked to `Sales` via `InvoiceDateKey`.

- **One-to-Many Relationships**: Each dimension table has a one-to-many relationship with the `Sales` fact table, enabling efficient filtering and aggregation.
- **Hierarchies**:
    - In the `Cars` table: `Make Hierarchy` organizes `Make` and `Color`.
    - In the `DateDimension`: Date fields allow for time-series analysis.
  
## Data Analysis (DAX):
Measures used in all visualization are:
<p align="center" style="margin-top: 20px; margin-bottom: 20px;">
<img width="20%" src="https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand/blob/main/images/key_measures.png" alt="key_measures"></img>
</p>


## Data Visualization (Dashboard):
Data visualization for the data analysis (DAX) was done in Microsoft Power BI Desktop:

| Dashboard 1|
| ----------- |
|![dashboard1](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand/blob/main/images/CarSales_dashboard1.png)|

| Dashboard 2|
| ----------- |
|![dashboard2](https://github.com/ThuyTran102/DA__4__dashboard__Sales_Analysis_by_car_brand/blob/main/images/CarSales_dashboard2.png)|


## Insights & Recommendations:
### 1. Comments on the Sales Trend Chart:
- Total Revenue: From 2012 to 2013, revenue increased from $3.2M to $7.2M. In 2014, revenue dropped to $6.4M. By 2015, revenue rebounded strongly, reaching a peak of $15M.
- Total Cost: From 2012 to 2013, costs rose from $2.2M to $4.3M. In 2014, despite the decline in revenue, costs increased to $4.6M. Costs continued to rise sharply in 2015, reaching $9.6M.
- Gross Profit: Gross profit steadily increased, from $1M to $3M during 2012-2013. In 2014, due to lower revenue and rising costs, gross profit dropped significantly to $1.8M. In 2015, although costs were high, gross profit rose to $5.3M due to the significant increase in revenue.
#### Summary:
2014: Although revenue decreased, costs rose, leading to a notable decline in gross profit. This reflects ineffective cost management in the context of declining revenue.
Trend: Revenue and costs experienced considerable fluctuations between 2012 and 2015, with a particular downturn in 2014 and a strong recovery in 2015.
Business Performance: Despite peak revenue in 2015, the high costs reduced profit potential. This may indicate a need for tighter cost control during this period.
#### Recommendations:
- Cost Control: Closely monitor operating costs, especially during periods of declining revenue, such as in 2014.
- Optimize Efficiency: Focus on improving profitability by optimizing sales processes and reducing waste.
- Flexible Forecasting and Response: Develop a strategy for revenue forecasting and risk management to avoid excessive cost increases when revenue declines.


### 2. Comments on the 2015 Business Performance by Car Brand:
- **Aston Martin**:
  - Total Revenue: Around $4M, the highest among the brands.
  - Gross Profit: High, with a clear margin between revenue and costs, achieving a profit margin of approximately 44%.
- **Rolls Royce**:
  - Total Revenue: Nearly $3M.
  - Gross Profit: Highest margin in the group at 50%, indicating effective cost management.
- **Jaguar**:
  - Total Revenue: Around $2M.
  - Gross Profit: Low, with a margin of only 13%, indicating high costs relative to revenue.
- **Bentley**:
  - Total Revenue: Approximately $2M.
  - Gross Profit: Profit margin is 19%, decent but still needs optimization.
- **MGB**:
  - Total Revenue: Low, but with a profit margin of 60%, the highest in the group, showing very efficient cost management.
- **Triumph**:
  - Total Revenue: Low, with a profit margin of 22%, positive but not enough to be competitive.
- **TVR**:
  - Total Revenue: Very low, with a negative profit margin (-19%), indicating significant losses, likely due to revenue insufficient to cover costs.

#### Recommendations:
- Strengthen Business Strategy for TVR and Jaguar: Focus on optimizing costs or improving sales, especially for TVR, to avoid losses.
- Maintain Strong Performance for Rolls Royce and MGB: Continue to optimize costs and maximize revenue potential, as these brands have high profit margins.
- Review Pricing and Cost Strategy for Bentley and Triumph: While the profit margin is reasonable, further improvement is needed to enhance competitiveness.
- Optimize Profit Margin for Aston Martin: Although revenue is high, increasing the profit margin can maximize overall profitability.



### 3. Comments on the 2015 Business Performance by Car Color:
- **Red**:
  - Total Revenue: Around $3M, the highest among all colors.
  - Gross Margin: Despite high revenue, the profit margin is only 36%, indicating relatively high costs.
- **Silver**:
  - Total Revenue: Around $2M.
  - Profit Margin: 40%, relatively high, indicating a good balance between cost and revenue.
- **Black**:
  - Total Revenue: Close to $2M.
  - Profit Margin: 34%, lower than Silver despite similar revenue, suggesting room for cost optimization.
- **Canary Yellow**:
  - Total Revenue: Fairly stable at around $1.8M.
  - Profit Margin: 37%, high and sustainable.
- **British Racing Green**:
  - Total Revenue: Close to $1.5M.
  - Profit Margin: 22%, the lowest in the group, suggesting a need to review cost strategy.
- **Dark Purple**:
- Total Revenue: Around $1.5M.
- Profit Margin: 39%, quite high, indicating stable profitability.
- **Blue**:
  - Total Revenue: Close to $1.5M.
  - Profit Margin: 35%, promising but still has room for cost improvements.
- **Green**:
  - Total Revenue: Around $1.2M.
  - Profit Margin: 40%, the highest in the group, demonstrating strong business efficiency.
- **Night Blue**:
  - Total Revenue: Lowest in the group, around $1M.
  - Profit Margin: 31%, needs improvement to stay competitive.

##### Recommendations:
- Optimize Inventory Based on High-Margin Colors: Control inventory levels for colors with lower profitability or slow-moving items to optimize cash flow and business efficiency:
- Prioritize Inventory for Colors with High and Stable Margins - Silver, Green, and Dark Purple: These colors have high and relatively stable profit margins, so additional stock should be maintained to meet market demand.
- Limit Stock for Low-Margin Colors - British Racing Green and Red: Although they generate revenue, high costs result in low profit margins. Stock levels should be controlled to avoid large inventory risks.
- Maintain Moderate Inventory for Black and Blue: Although not as high in revenue as Red, these two colors still maintain stable profit margins. However, inventory should be carefully monitored to avoid overstocking.
- Reduce Inventory for Night Blue: With the lowest revenue and a modest profit margin, consider reducing orders or only stocking minimum quantities to avoid long-term inventory.
- Consider Promotional or Discount Programs for Slow-Moving Stock: For lower-margin colors like British Racing Green or slow sellers like Night Blue, promotion or discount programs can help reduce inventory and free up storage space.


