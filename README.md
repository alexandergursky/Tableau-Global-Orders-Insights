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
The methodology for preprocessing the Global-Orders dataset before continuing to Tableau involved several steps. The ETL (Extract, Transform, Load) process began with importing the necessary libraries such as NumPy, Pandas, and the regular expression (re) module. The dataset was loaded using the Pandas library, and column names were standardized by replacing spaces with underscores. Although the standardizing of column names is not a requirement, I find it provides a more fluid and robust overall process. Data cleaning started by focusing on the 'Product_Name' column, using regular expressions to remove the color attributes following the commas. This allowed for the simplification and readability of product names, as colors are not required for actionable insights. Additionally, special characters were removed from the 'Product_Name' column using regular expressions. The remaining parsing and cleaning ensured that usable information could be extracted from the data with as little data loss as possible.
  
To extract the company names, a subset dataframe was created, and non-alphanumeric and special characters were removed from the 'Product_Name' column. Then, a list of unique company names was created by splitting the elements on the first space. Numeric company names were excluded in this report for parsing simplicity purpose. Further manual work was performed to fix company names which contained spelling errors, duplicates from errors, and to handle specific cases. Next, the elements were reformatted, cleaned, and parsed for both companies and products. This involved converting company and product names to proper case, replacing specific names using regular expressions, matching product names with company names, and removing company names from the 'Product_Name' column.
  
Profit values were corrected, and unwanted values such as NaNs and non-printables were removed from the dataset. Finally, the preprocessed dataset was exported as 'preprocessed-Global-Orders.csv' for further analysis in Tableau.
  
## Conclusion and Recomendations
  
The top three regions, in descending order of production, were APAC (Asian-Pacific), EU (European Union), and the United States. Understanding why each region produces its highest product category pertains to current events and knowledge of the regions. For example, most tech companies are concentrated in both APAC and the US. A correlation was observed between shipping priority level and profit earned for Technology and Office Supplies. However, the Furniture category had higher profits for high and medium order priorities. The priority level in relation to shipping cost was as expected.
  
Moving forward, I would recommend that companies in the furniture industry implement additional fees associated with critical priority level items. Alternatively, they could impose a minimum order time window falling into the high and medium categories, which would require orders to go through the established supply chain. Simultaneously, it is important to explore ways to optimize the performance of both categories.
  
Among the top-producing American tech companies were Canon, Hewlett-Packard, Cisco, Samsung, and Brother. Three out of the five companies produce copiers, while the remaining focus on phones. However, phones yield approximately double the profitability in comparison.
  
During Q4, Canon's main target market was observed to be in the northeastern US region. As a result, Canon has various campaign options available to enhance their efforts in that region. These options include targeted marketing, strengthening distribution channels, increasing customer engagement, regional customization, and strategic market expansion. By focusing on these areas, Canon can maximize their sales and capitalize on their dominant position in the market.
