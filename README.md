# Carbon-Emission-Analysis
This report aims to analyze carbon emissions to examine the carbon footprint across various industries. We aim to identify sectors with the highest levels of emissions by analyzing them across countries and years, as well as to uncover trends.

Carbon emissions play a crucial role in the environment, accounting for over 75% of global emissions and posing a significant environment challenge. These emissions contribute to the accumulation of greenhouse gases in the atmosphere, leading to climate change, planetary warming, and involvement in various environment disasters.

Through this analysis, we hope to gain an understanding of the environmental impact of different industries and contribute to making informed decisions in sustainable development.

# Data Soucre: Where Our Data Comes From
Our dataset is compiled from publicy available from nature.com and encompasses the product carbon footprint (PCF) for various companies. PCFs represent greenhouse gas emissions associated with specific products, quantified in CO2 (carbon dioxide equivalent).

# Data Structure
The dataset consists of 4 tables containing information regarding carbon emissions generated during the production of goods.


# 1. Which products contribute the most to carbon emissions?

```sql
SELECT product_name, MAX(carbon_footprint_pcf)
FROM product_emissions
GROUP BY product_name
ORDER BY MAX(carbon_footprint_pcf) DESC
LIMIT 10;
```
| product_name                                                                                                                       | max_carbon_footprint | 
| :--------------------------------------------------------------------------------------------------------------------------------- | -------------------: | 
| Wind Turbine G128 5 Megawats                                                                                                       | 3718044              | 
| Wind Turbine G132 5 Megawats                                                                                                       | 3276187              | 
| Wind Turbine G114 2 Megawats                                                                                                       | 1532608              | 
| Wind Turbine G90 2 Megawats                                                                                                        | 1251625              | 
| Land Cruiser Prado. FJ Cruiser. Dyna trucks. Toyoace.IMV def unit.                                                                 | 191687               | 
| Retaining wall structure with a main wall (sheet pile): 136 tonnes of steel sheet piles and 4 tonnes of tierods per 100 meter wall | 167000               | 
| TCDE                                                                                                                               | 99075                | 
| Mercedes-Benz GLE (GLE 500 4MATIC)                                                                                                 | 91000                | 
| Electric Motor                                                                                                                     | 87589                | 
| Mercedes-Benz S-Class (S 500)                                                                                                      | 85000                | 

Based on the table above, here 
The wind turbines have the highest carbon footprints among the listed products.
- The Wind Turbine G128 5 Megawats: 3,718,044kg CO₂e
- The Wind Turbine G132 5 Megawats: 3,276,187kg CO₂e
- The Wind Turbine G114 2 Megawats: 1,532,608kg CO₂e
- The Wind Turbine G90 2 Megawats: 1,251,625kg CO₂e
We can see that despite being renewable energy infrastructure
