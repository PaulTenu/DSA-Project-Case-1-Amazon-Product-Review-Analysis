# Amazon- Product Review Analysis Dashboard(Excel)

## Project Objective
This Project aims to analyse product and customer review data to uncover actionable insights. The primary goal is to support data-driven decision-making across product development, marketing, and customer engagement strategies. By identifying patterns in customer feedback and product performance, the project aims to Highlight areas for product improvement, Inform targeted marketing campaigns and Enhance customer satisfaction and loyalty through better engagement.

## Data Set used

- <a href = "https://github.com/PaulTenu/DSA-Project-Case-1-Amazon-Product-Review-Analysis/blob/main/DSA%20CAPSTONE%20PROJECT_QNS_1_EXCEL.xlsx">Data set</a>

## Analysis Tasks
1. What is the average discount percentage by product category?
2. How many products are listed under each category?
3. What is the total number of reviews per category?
4. Which products have the highest average ratings?
5. What is the average actual price vs the discounted price by category?
6. Which products have the highest number of reviews?
7. How many products have a discount of 50% or more?
8. What is the distribution of product ratings (e.g., how many products are rated 3.0,
4.0, etc.)?
9. What is the total potential revenue (actual_price × rating_count) by category?
10. What is the number of unique products per price range bucket (e.g., <₹200,
₹200–₹500, >₹500)?
11. How does the rating relate to the level of discount?
12. How many products have fewer than 1,000 reviews?
13. Which categories have products with the highest discounts?
14. Identify the top 5 products in terms of rating and number of reviews combined.
15. Dashboard Creation <a href = "https://github.com/PaulTenu/DSA-Project-Case-1-Amazon-Product-Review-Analysis/blob/main/Screenshot_Dashboard.png">view Dashboard</a>

## Exploratory Data Analysis
- Verify data for any missing values and anomalies, and sort out the same
- Made sure data is consistent and clean with respect to data type, data format and values used
- Created pivot tables according to the questions asked. A process that was achieved in the folllowing processes;
  - Average discount percentage by product category was achieved by adding a **calculated column** named *Discout Percentage* by;
    - = (Actual Price - Discounted Price) / Actual Price * 100
    - Then use a Pivot Table: *Rows - Category, Values - Discount % → summarized by Average*
  - How many products have a discount of 50% or more was also achieved by Adding another calculated column, *Discounted Product Count* as follows;
    - =IF(Discount % >= 50, "Yes", "No") Then use a COUNTIF.
  - Number of unique products per price range bucket. This wa handled by Creating a new column, *Price Bucket*:
    - Excel formular=IF(Discounted Price < 200, "< $200", IF(Discounted Price <= 500, "$200–$500", ">$500"))
    - Use a pivot table *Rows: Price Bucket, Values: Product Name → Count*
  - How does the rating relate to the level of discount Was addressed by Creating a *scatter chart*: *X-axis: Discount % Y-axis: Average Rating*.
  - Lastly, Top 5 products by rating + number of reviews combined was achieved by adding a new column thus,
    - =Average Rating + (Rating Count / Scaling Factor), a factor like 1000 was chosen to balance weight) and finally Sorted by descending and the top 5 picked.

## Dashboard

![Screenshot_Dashboard](https://github.com/user-attachments/assets/f33ada72-1f31-4ceb-9d5a-0041ecf5c8fe)


##  Project Insight

- The scattered chart Shows that most products with higher ratings (around 4) have a wide range of discounts, suggesting discounts don't necessarily correlate with rating levels. Meaning high product ratings do not guarantee lower or higher discounts, suggesting that discounting may be driven more by category strategy or competition than customer sentiment.
- There's a concentration of higher-priced items, which could indicate a focus on premium or tech-heavy products on Amazon. This shows the need to consider balancing product offerings with more budget-friendly options if targeting a wider customer base.
- While some products are highly reviewed, a significant number lack engagement, which may indicate poor visibility or newer listings. Hence the need to invest in review-generation strategies (e.g., promotions or early reviewer programs) for underperforming items.
- Findings also revealed that there’s substantial revenue potential from these products, and optimizing pricing/visibility could drive significant returns. Products like *AmazonBasics HDMI Cables and boAt Bassheads Earphones* lead in ratings and reviews.Such products could be used as benchmark products-understaning their traits(price, quality, marketing) could help improve others.
- Categories like Home & Kitchen and Electronics show noticeable gaps between actual and discounted prices. Showing that These categories are likely more price-sensitive and rely heavily on discounting to drive volume. Testing price elasticity and discount strategies carefully in these segments can help balance margin vs. volume.

## Final Concluion
The Amazon Product Sales Dashboard reveals key insights into product performance, customer engagement, and pricing strategies. While top-rated products attract significant attention, discount levels vary independently of ratings, suggesting the need for category-specific pricing tactics. The data highlights both high-revenue opportunities and underperforming products with low reviews, offering clear direction for marketing, product optimization, and strategic pricing to boost overall business performance.





