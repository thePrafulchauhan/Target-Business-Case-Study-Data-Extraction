# Target-Business-Case-Study-Data-Extraction
This business case has information of 100k orders from 2016 to 2018. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers.

Data is available in 8 csv files:

customers.csv

geolocation.csv

order_items.csv

payments.csv

reviews.csv

orders.csv

products.csv

sellers.csv

Each feature or columns of different CSV files are described below:

The customers.csv contain following features:

Features Description

customer_id Id of the consumer who made the purchase.

customer_unique_id Unique Id of the consumer.

customer_zip_code_prefix Zip Code of the location of the consumer.

customer_city Name of the City from where order is made.

customer_state State Code from where order is made(Ex- sao paulo-SP).

The sellers.csv contains following features:

Features Description

seller_id Unique Id of the seller registered

seller_zip_code_prefix Zip Code of the location of the seller.

seller_city Name of the City of the seller.

seller_state State Code (Ex- sao paulo-SP)

The order_items.csv contain following features:

Features Description

order_id A unique id of order made by the consumers.

order_item_id A Unique id given to each item ordered in the order.

product_id A unique id given to each product available on the site.

seller_id Unique Id of the seller registered in Target.

shipping_limit_date The date before which shipping of the ordered product must be completed.

price Actual price of the products ordered .

freight_value Price rate at which a product is delivered from one point to another.

The geolocations.csv contain following features:

Features Description

geolocation_zip_code_prefix first 5 digits of zip code

geolocation_lat latitude

geolocation_lng longitude

geolocation_city city name

geolocation_state state

The payments.csv contain following features:

Features Description

order_id A unique id of order made by the consumers.

payment_sequential sequences of the payments made in case of EMI.

payment_type mode of payment used.(Ex-Credit Card)

payment_installments number of installments in case of EMI purchase.

payment_value Total amount paid for the purchase order.

The orders.csv contain following features:

Features Description

order_id A unique id of order made by the consumers.

customer_id Id of the consumer who made the purchase.

order_status status of the order made i.e delivered, shipped etc.

order_purchase_timestamp Timestamp of the purchase.

order_delivered_carrier_date delivery date at which carrier made the delivery.

order_delivered_customer_date date at which customer got the product.

order_estimated_delivery_date estimated delivery date of the products.

The reviews.csv contain following features:

Features Description

review_id Id of the review given on the product ordered by the order id.

order_id A unique id of order made by the consumers.

review_score review score given by the customer for each order on the scale of 1–5.

review_comment_title Title of the review

review_comment_message Review comments posted by the consumer for each order.

review_creation_date Timestamp of the review when it is created.

review_answer_timestamp Timestamp of the review answered.

The products.csv contain following features:

Features Description

product_id A unique identifier for the proposed project.

product_category_name Name of the product category

product_name_lenght length of the string which specifies the name given to the products ordered.

product_description_lenght length of the description written for each product ordered on the site.

product_photos_qty Number of photos of each product ordered available on the shopping portal.

product_weight_g Weight of the products ordered in grams.

product_length_cm Length of the products ordered in centimeters.

product_height_cm Height of the products ordered in centimeters.

product_width_cm width of the product ordered in centimeters.

You are given this data to analyze and provide some insights and recommendations from it.

The dataset is uploaded and insights are drawn using SQL queries in Big Query

Actionable Insights:

• The dataset time period is from September 2016 to October 2018. Data of 2 years is given. • It covers 4119 cities across 27 states of Brazil. • There is a growing trend of e-commerce with seasonal spike during the month of November. • Most of the orders are placed during afternoon(max) and nighttime. During dawn very less number of orders are placed. • 38.58% orders are placed during afternoon, 34.29% during nighttime, 22.36% during morning and only 4.76% during dawn. • Most orders is from SP and the number of orders is also increasing over the months and year and least orders is from AC and RR. Overall there is rise in orders in all states over months. • SP has the maximum number of customers with 41.94% customers on the other hand RR has lowest number of customers which is only 0.05% of total customers. • The order value in 2018 is 138.66% more than 2017, which shows a huge increase in e-commerce economy. • Total order value is maximum in SP, but the highest mean price is from PB which is 191.48 and total order value is 115268.08 which is not even in top 10. This may be due to the high mean freight value that is 42.72 (second highest after RR). SP has the lowest mean freight value of 15.15 which maybe the reason for high number of orders from this region. • Average freight value and mean delivery time is highest in RR. Also, there is high mismatch between the estimated delivery time and actual delivery time. On the other hand, SP has lowest freight value and delivery time. This may be one of the reasons of high orders from SP and low orders from RR. • The highest mismatch between the estimated delivery time and the actual delivery time is in AC and this state also has low orders. • Most preferred mode of payment is by credit cards followed by UPI and least preferred is debit card, and this trend remains same over the months. The high use of credit card may be since with-it costumer has the option of installment instead of paying full amount. There is an overall increase in all type of payment modes over the months. • Customers prefer payment through installments and most opted number of installments is 1 (which is full payment). And the number of installments that the customers opted for is from 1 to 24. Most customers prefer to pay whole amount at once but there is a huge number of customers who prefer payment in installments.

For output 1st 10 rows are checked.

Recommendations:

• Since there is a spike of sale in the month of November more discount, offers may be given in this month to further boost the sales. • Most of the orders are during afternoon and nighttime it may be the best time to send notifications or promotional mails to the customers. • In the state of AC, RR and other states where sale is low due to high freight charge and high delivery date, the situation can be improved by improving the infrastructure over there like, establishing an inventory, investing more in delivery system and launching marketing campaigns. In states like SP, from where revenue is high incentives/lucrative deals should be given to convert the customers into loyal customers. • Most of the users uses credit cards to make a payment, so credit cards offers can be given to them to increase the sale. This data can also be used to make a deal with credit card companies. They can give offers if customers use their credit card on our website. • Also many customers opt for installments so lower EMI options would be a great idea to increase the sale.
