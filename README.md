# Tableau-Global-Orders-Insights

**Global Orders Dataset Metric Overview**
- Size: (51290, 24)
- Columns: 'Row ID', 'Order ID', 'Order Date', 'Ship Date', 'Ship Mode', 'Customer ID', 'Customer Name', 'Segment', 'City', 'State', 'Country', 'Postal Code', 'Market', 'Region', 'Product ID', 'Category', 'Sub-Category', 'Product Name', 'Sales', 'Quantity', 'Discount', 'Profit', 'Shipping Cost', 'Order Priority'
  
## Purpose and Scope
The dataset was chosen due to its complexity and the potential insights it could offer. The objective was to answer various questions such as identifying the regions that produce the most goods, exploring correlations between order priority on profit and on shipping cost, determining the leading American tech companies, understanding their specialization, and analyzing Canon's target market and formulating potential strategies for capitalizing on it.  
  
**Project Goals**
1. What Regions Produce the most goods?
2. Why might these regions produce their good(s)?
3. Is there a correlation between priority level in orders and the profit earned?
4. Is there a correlation for priority level of an orders and the associated shipping cost? 
5. What American Tech companies produce the most?
6. What products do the American Tech companies specialize in?
7. What/where is Canon's target market?
8. How can Canon capitalize on this market?
  
## Methodology
The methodology for preprocessing the Global-Orders dataset for Tableau involved several steps. The ETL (Extract, Transform, Load) process began with importing the  necessary libraries such as NumPy, Pandas, and the regular expression (re) module. The dataset was loaded using the Pandas library, and column names were standardized by replacing spaces with underscores. Although the standardizing of column names is not a requirement, I find it provides more fluidity throughout the process, and often I recommend doing so. Data cleaning started by focusing on the 'Product_Name' column using regular expressions. The color attributes following the comma were removed to simplify the names as they are not required. Additionally, special characters were removed from the 'Product_Name' column using regular expressions.

To gather company names, a subset dataframe was created, and non-alphanumeric and special characters were removed from the 'Product_Name' column. Then, a list of unique company names was extracted by splitting the names at the first space. Numeric company names were excluded, resulting in a dataframe containing a list of companies. Further manual work was performed to fix company names, drop duplicates, and handle specific cases.

Next, the company names were reformatted, cleaned, and parsed for both companies and products. This involved converting company and product names to proper case, replacing specific names using regular expressions, matching product names with company names, and removing company names from the 'Product_Name' column.

Profit values were corrected, and unwanted values such as NaNs and non-printable or non-ASCII characters were removed from the dataset. Finally, the preprocessed dataset was exported as 'preprocessed-Global-Orders.csv' for further analysis in Tableau.
  
  
## Outcomes and Recomendations
  

