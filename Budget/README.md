# Budget <img src="/pics/DAX logo.jpg" align="right" width="30%"/>

Showcase of the two approaches in Budgeting process: top down and bottom up. <br>
## Budget: Top-down 
The scenario is a top-down forecasting scenario. The source data contains a forecast of sales for different scenarios at a _low granularity_. Low granularity means that the information provided is at a very high level: year, store country, and product category. There are no details about individual products, months or stores.<br>
### Allocation based on the previous year
When the forecast needs to be reallocated, we consider the sales in the previous year as an allocation factor. In other words, in order to show the forecast of a subcategory, we reallocate the budget defined at the category level by the percentage of sales of the given subcategory against the corresponding category in the previous year.
- :shipit: this is the best approach for rolling budget when forceasting is derived on for example **R** in Data Science. Testing of the likelihood can be done with Simulations using Monte Carlo simulations.
#### Automation using BI: DAX showcase 

Excellent proof of concept by SQLBI: [DAX Patterns](https://www.daxpatterns.com/budget/)

## Budget: Bottom-up
In this budgeting scenario, we adopt a bottom-up approach, emphasizing detailed planning. The source data encompasses a granular sales plan, offering insights at multiple levels, including month, country, product category, quantity/units, and stores. This methodology involves the creation of sub-budgets by budget holders, with the primary objective being the integration of these mini-budgets.<br>
### 1. ETL: Converting our budget to a tabular format 

<img src="/pics/QueryDependency.JPG" width="50%" /> 

### 2. Creating star schema

<img src="/pics/StarSchema.JPG" width="50%" />

### 3. Creating measures using DAX

### 4. Create visuals and tables

