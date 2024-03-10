# Budget 

Showcase of the two approaches in Budgeting process: top down and bottom up. <br>
## Budget: Top-down 
The scenario is a top-down forecasting scenario. The source data contains a forecast of sales for different scenarios at a low granularity. Low granularity means that the information provided is at a very high level: year, store country, and product category. There are no details about individual products, months or stores.<br>
### Allocation based on the previous year
When the forecast needs to be reallocated, we consider the sales in the previous year as an allocation factor. In other words, in order to show the forecast of a subcategory, we reallocate the budget defined at the category level by the percentage of sales of the given subcategory against the corresponding category in the previous year.
- :shipit:
#### Automation using BI: DAX showcase 
## Budget: Bottom-up
The scenario is a bottom-up budget (planning) scenario. The source data contains a planning of sales at a high granularity. High granularity means that the information provided is at at various level of detail: month, country, product category, or stores. This approach is based on the production of budget holder sub-budget and the main task is the integration of mini-budgets.<br>
