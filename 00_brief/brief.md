1. Who has the problem : Olist MarketPlace

2. What the problem is : The main problem is that some orders arrive later than their promised delivery dates, potentially affecting customer satisfaction.

3. Why it matters : Late deliveries may lead to lower review scores and reduce customers' willingness to purchase again.

4. What decision this analysis supports? : This analysis will help Olist identify where delivery problems occur and decide which sellers, locations, or delivery processes need improvement.


## Stakeholders

1. **Head of Operations:** Needs to identify where deliveries are failing, which locations experience the highest delays, and where operational improvements are required.

2. **Seller Success Manager:** Needs to identify sellers with frequent delivery delays and poor customer reviews to determine which sellers require intervention.

3. **Customer Experience (CX) Lead:** Needs to understand customer complaints, identify reasons for dissatisfaction, and measure how late deliveries affect review scores.

4. **Finance / Growth Team:** Needs to understand whether late deliveries affect repeat purchases, customer retention, and long-term business growth.

## Business Questions
a.	**What share of delivered orders arrive after the promised date?**

b.	**How much lower are review scores when delivery is late, and does the gap grow with delay length?**

c.	**Which sellers and customer states have the worst late rates?**

d.	**Do customers whose first order was late come back less?**

e.	**What do unhappy customers actually complain about?**

## KPI Definitions
1. Late Order
- Definition: An order is late if its actual delivery date is later than its estimated delivery date.
- Formula:
  order_delivered_customer_date > order_estimated_delivery_date
- Data Source: olist_orders_dataset.csv
- Condition: Delivered orders only.


2. Late Delivery %
- Definition: Percentage of delivered orders that arrived after the promised delivery date.
- Formula:
  \[
  \frac{\text{Late Orders}}{\text{Total Delivered Orders}}\times 100
  \]
- Data Source: olist_orders_dataset.csv


3. Average Review Score
- Definition: Average customer rating across orders, using the latest review per order.
- Formula:
  \[
  \frac{\text{Sum of Latest Review Scores}}{\text{Number of Orders with Reviews}}
  \]
- Data Source: olist_order_reviews_dataset.csv


4. One-Star %
- Definition: Percentage of reviewed orders that received a rating of 1.
- Formula:
  \[
  \frac{\text{Orders with 1-Star Reviews}}{\text{Total Orders with Reviews}}\times 100
  \]
- Data Source: olist_order_reviews_dataset.csv


5. Score Gap
- Definition: Difference between the average review score of on-time orders and late orders.
- Formula:
  \[
  \text{Average On-Time Score} - \text{Average Late Score}
  \]
- Data Source:
  - olist_orders_dataset.csv
  - olist_order_reviews_dataset.csv

  
6. Repeat Customer %
- Definition: Percentage of customers who have placed more than one delivered order.
- Formula:
  \[
  \frac{\text{Customers with >1 Delivered Order}}{\text{Total Customers}}\times 100
  \]
- Data Source:
  - olist_orders_dataset.csv
  - olist_customers_dataset.csv


## User stories for the dashboard
•	DO: Write these 5 and keep them, because the dashboard will be built against them.
f.	As an Ops head, I want late % by month and state, so I can spot trends.
g.	As a Seller Success manager, I want a ranked list of sellers by late %, so I can pick who to call first.
h.	As a CX lead, I want complaint themes, so I can see what's driving bad reviews.
i.	As an executive, I want 4 headline KPIs on one page.
j.	As an analyst, I want to filter by date, state and delay bucket.

