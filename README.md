# Client Data Analysis

## Overview

This project analyzes a client dataset to identify patterns in client purchasing behavior, profitability, and shipping costs. The analysis includes calculating key metrics, confirming specific order totals, and summarizing top clients' performance based on total units ordered, revenue, shipping costs, and profit.

## Data

The dataset includes information on client orders such as unit prices, quantities, shipping prices, and profits. The dataset was analyzed using Python and Pandas.

### Columns:
- `client_id`: Unique identifier for each client
- `category`: Product category of the item purchased
- `subcategory`: More specific categorization within each category
- `unit_price`: Price per unit of the item purchased
- `qty`: Number of units ordered
- `unit_weight`: Weight per unit of the item ordered
- `unit_cost`: Cost to produce the item per unit
- Other calculated columns: `line_subtotal`, `total_weight`, `shipping_price`, `line_price`, `line_cost`, `line_profit`

## Steps

### Part 1: Explore the Data

1. **View Column Names**: Examined the column names in the dataset.
2. **Descriptive Statistics**: Used the `describe()` function to gather basic statistics.
3. **Top Categories and Subcategories**: Identified the top three item categories by total entries and the top subcategory within the largest category.
4. **Top 5 Clients**: Identified the five clients with the most entries and calculated total units for the top client.

### Part 2: Transform the Data

1. **Subtotal Calculation**: Created a column for the subtotal by multiplying `unit_price` and `qty`.
2. **Shipping Price**: Applied conditional shipping price logic based on weight.
3. **Total Price with Tax**: Calculated total price, including shipping price and a 9.25% sales tax.
4. **Cost Calculation**: Calculated total line cost using `unit_cost`, `qty`, and `shipping_price`.
5. **Profit Calculation**: Calculated profit for each line by subtracting cost from total price.

### Part 3: Confirm Order Totals

The following orders were confirmed against known totals:
- **Order ID 2742071**: Confirmed total price of \$152,811.89
- **Order ID 2173913**: Confirmed total price of \$162,388.71
- **Order ID 6128929**: Confirmed total price of \$923,441.25

### Part 4: Summarize and Analyze

1. **Top 5 Clients by Revenue**: Calculated total revenue for the top 5 clients.
2. **Summary DataFrame**: Created a summary DataFrame with total units purchased, total shipping price, total revenue, and total profit for the top 5 clients.
3. **Currency Conversion**: Converted monetary columns to millions and reformatted the column names.
4. **Sorting**: Sorted the summary DataFrame in descending order by total profit.

## Summary of Findings
Client 24741 was the most profitable, generating over $82 million in total revenue and over $36 million in profits, with 239,862 units purchased. Clients with higher order quantities benefited from reduced shipping costs per unit, likely due to bulk shipping rates. This trend contributed to a strong correlation between total units purchased and overall profitability across all clients.

## How to Run the Code

1. Install Python and Pandas.
2. Clone this repository to your local machine.
3. Place the dataset in the `Resources` folder.
4. Run the Python code to explore, transform, and analyze the data.

## Technologies Used

- **Python**: Version 3.10.14 or later
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Jupyter Notebook**: Code execution and exploration
