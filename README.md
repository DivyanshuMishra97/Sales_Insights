
# Sales and Revenue Dashboard

## Problem Statement

This dashboard helps the IT company gain deeper insights into sales performance, revenue trends, and customer behavior. By analyzing data across multiple dimensions, such as top-performing markets, customers, products, and regions, it empowers the company to make informed decisions to improve overall business outcomes.

Through detailed visualizations, the dashboard identifies revenue drivers and highlights areas needing attention, such as underperforming regions or product categories. It consolidates sales data in multiple currencies into a unified INR-based view, providing clarity and simplifying financial reporting. The trends and breakdowns presented in the dashboard enable the company to create data-driven strategies to maximize revenue and optimize market performance.


### Steps followed 

- Step 1: Connected to the company's MySQL database via Power BI to import sales and revenue data directly.

- Step 2: Loaded the dataset into Power Query Editor, and under the View tab, enabled "Column Distribution," "Column Quality," and "Column Profile" to validate and clean the data.

- Step 3: Addressed multi-currency values in the dataset:

    Created a calculated column in Power BI using DAX to convert revenue and sales amounts into INR using predefined exchange rates:
    DAX
    Copy code
    Adjusted Revenue = 
    SWITCH(
    [Currency],
    "USD", [Revenue] * 83,
    "EUR", [Revenue] * 90,
    [Revenue] -- Default case for INR or already converted values
    )
    Ensured null and blank values were excluded from calculations.

- Step 4: Designed key visuals in the Report View:

    Two card visuals: Displayed total revenue (₹984.88M) and total sales quantity (2M units).
    Bar charts: Represented revenue and sales distribution by markets.
    Line chart: Showcased revenue trends over time (from 2017 to 2020).
    Bar charts: Highlighted top 5 customers and top 5 products contributing to revenue.

- Step 5: Added interactive slicers for:

    Time period (year, quarter, month).
    Market/region.
    Product category.

- Step 6: Enhanced dashboard design:

    Used the company’s theme and color palette for branding.
    Inserted text boxes for the company's name and tagline.
    Added the company logo in the header.

- Step 7: 
    Published the dashboard to Power BI Service, allowing stakeholders to access it online. Configured automatic data refresh for real-time updates.
    Snapshot of the Dashboard:


# Insights

- A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Revenue and Sales Quantity

    Total Revenue: ₹984.88M
    Total Sales Quantity: 2M units

- Insight: Revenue and sales are distributed across multiple markets and customers, with significant contributions from top-performing regions and clients.

![1](https://github.com/user-attachments/assets/d2c12dd6-3032-46e8-962d-1e4bf2505b9f)
         
### [2] Revenue by Markets

   - Top Revenue-Generating Markets:

    -Delhi NCR: ₹519.58M (52.74%)
    -Mumbai: ₹150.08M (15.23%)
    -Ahmedabad: ₹132.31M (13.44%)
    -Bhopal: ₹58.61M (5.94%)
    -Nagpur: ₹55.03M (5.59%)

   - Low Revenue Markets:

    -Kochi: ₹18.11M (1.84%)
    -Chennai: ₹18.04M (1.83%)
    -Bengaluru: ₹0.37M (0.03%)

- Insight: Delhi NCR generates over half of the total revenue, making it the most critical market, while Bengaluru and Kochi show room for growth.

![2](https://github.com/user-attachments/assets/d4e11b30-0805-4406-8225-15503166aaec)
  
### [3] Sales by Markets
  
  - Top Sales Markets:

        -Delhi NCR: 988K units (49.4%)
        -Mumbai: 384K units (19.2%)
        -Nagpur: 262K units (13.1%)
        -Kochi: 255K units (12.8%)
        -Ahmedabad: 207K units (10.4%)
    
- Insight: Delhi NCR also leads in sales quantity, indicating high demand and engagement in this market.

![3](https://github.com/user-attachments/assets/fdd18929-2082-45bc-8a7a-71b0a18bddf6)

 ### [4] Revenue Trends
 
    -Peak Revenue Period: Mid-2018 with monthly revenue reaching ₹40M.
    -Lowest Revenue Period: Late 2019 with monthly revenue dropping to ₹10M.

- Insight: The sharp revenue decline after mid-2018 may require analysis to identify the reasons and replicate successful strategies from the peak period.

![4](https://github.com/user-attachments/assets/fe058def-1e6d-4bf0-8166-aade25a646c2)

 ### [5] Top Customers
 
    -Electricalsara Stores: ₹413.33M (41.97%)
    -Electricalytical: ₹49.64M (5.04%)
    -Excel Stores: ₹49.12M (4.99%)
    -Premium Stores: ₹44.97M (4.57%)
    -Nixon: ₹43.89M (4.46%)
    
- Insight: Electricalsara Stores dominates revenue contributions, making it a key customer to prioritize and retain.

![5](https://github.com/user-attachments/assets/58557fa5-a5e3-4398-8e2c-bf0cde11351f)
         
### [6] Top Products

    -(Blank): ₹468.96M (47.63%)
    -Prod040: ₹23.58M (2.39%)
    -Prod159: ₹17.66M (1.79%)
    -Prod005: ₹16.26M (1.65%)
    -Prod018: ₹15.6M (1.58%)
    
- Insight: A significant portion of revenue falls under the "(Blank)" category, which requires data validation to ensure accurate reporting.

![6](https://github.com/user-attachments/assets/4f5664cf-c896-46af-a8ff-9a8833dabdde)

### [7] Other Insights

- Revenue Contribution by Market:
    -Top 3 Markets (Delhi NCR, Mumbai, Ahmedabad) contribute 81.41% of the total revenue.
    -Remaining markets contribute less than 20%.
- Product Performance:
    -While specific products contribute steadily to revenue, the missing product name issue affects visibility and requires immediate attention.
- Customer Dependency:
    -The top customer (Electricalsara Stores) alone accounts for over 40% of the total revenue. Diversifying the customer base can reduce revenue dependency on a single client.

# Report Snapshot (Power BI DESKTOP)

![Screenshot 2024-12-13 163709](https://github.com/user-attachments/assets/aeab5037-d36d-465c-9039-e27543a916c5)

### Recommendations:

- Strengthen Top Markets: Focus on Delhi NCR and Mumbai to maintain and increase revenue.
- Investigate Data Gaps: Resolve the "(Blank)" product issue to ensure accurate reporting and uncover potential revenue sources.
- Boost Low-Performing Markets: Create targeted campaigns for markets like Kochi, Chennai, and Bengaluru to increase revenue share.
- Customer Retention: Build loyalty programs for Electricalsara Stores and other high-value customers to ensure long-term revenue stability.
- Analyze Peak Trends: Investigate factors behind the revenue peak in mid-2018 to replicate those strategies in future campaigns.
