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
The same process is replicated for the actuals, where individual actual reports are structured and merged with the master actuals data set using M language, then loaded into a tabular format. :point_right: _Budget/data/Actuals.xlsx_

<img src="/Budget/pic/QueryDependency_Actuals.JPG" width="100%" /> <br>

### 2. Creating the Master Table
The the tables are merged into a master table with a star schema. A star schema is a database design where data is organized into a central "fact" table surrounded by "dimension" tables. The fact table contains the core data, while dimension tables provide context. Benefits include simplified queries, faster data retrieval, and easier data analysis due to clear relationships between tables. :point_right: _Budget/data/Model.xlsx_

<img src="/pics/StarSchema.JPG" width="100%" />

### 3. Creating measures using DAX
A DAX measure is a calculation formula used in Power BI and Excel Power Pivot to perform calculations on data fields. It helps derive new insights from the data by creating custom metrics or aggregations. Benefits include flexibility in analysis, allowing users to create tailored calculations specific to their needs, and enhancing the depth of insights derived from the data.

### 4. Create visuals

### 5. Create reports using MDX/CUBE functions in Excel

<img src="/FinancialSummary/pics/Summary-2.jpg" width="100%" />
<img src="/FinancialSummary/pics/Summary-3.jpg" width="100%" />
<img src="/FinancialSummary/pics/Summary-4.jpg" width="100%" />

