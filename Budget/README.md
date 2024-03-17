# Budget <img src="/pics/DAX logo.jpg" align="right" width="30%"/>
 > Showcase of the two approaches in Budgeting process: top down and bottom up. <br>
## Budget: Top-down 
The scenario is a top-down forecasting scenario. The source data contains a forecast of sales for different scenarios at a _low granularity_. Low granularity means that the information provided is at a very high level: year, store country, and product category. There are no details about individual products, months or stores.<br>
### Allocation based on the previous year
When the forecast needs to be reallocated, we consider the sales in the previous year as an allocation factor.

#### Automation using BI: DAX showcase 

Proof of concept :point_right: Budget/data/Budget - Top Down.pbix

<img src="/Budget/pic/Budget_TopDown.JPG" width="100%" />

## Budget: Bottom-up
In this budgeting scenario, we adopt a bottom-up approach, emphasizing detailed planning. The source data encompasses a granular sales plan, offering insights at multiple levels, including month, country, product category, quantity/units, and stores. This methodology involves the creation of sub-budgets, with the primary objective being the integration of these mini-budgets.<br>
### 1. ETL: Converting our budget to a tabular format 
#### 1.1. Preparing and transfoming Mini-budgets
The ETL stage involves restructuring five mini-budgets stored in separate Excel spreadsheets to accommodate the required level of detail. These individual budgets are then merged with a master budget containing all costs and revenue types. The transformation process utilizes M language and loads the data into a tabular format. :point_right: _Budget/data/Budget.xlsx_
<img src="/pics/QueryDependency.JPG" width="100%" /> 

#### 1.2 Preparing actuals
The same process is replicated for the actuals, where individual actual data sets are structured and merged with the master actuals budget using M language, then loaded into a tabular format. :point_right: _Budget/data/Actuals.xlsx_

<img src="/Budget/pic/QueryDependency_Actuals.JPG" width="100%" /> <br>

#### 1.3 Merging Actuals and Budget

### 2. Creating star schema

<img src="/pics/StarSchema.JPG" width="100%" />

### 3. Creating measures using DAX

### 4. Create visuals and tables
Please check it out:<br>
:point_right: _Budget/data/Model.xlsx_
