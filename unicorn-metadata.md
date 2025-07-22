# Unicorn Metadata

## Database Schema

![Unicorn's Database Schema](/unicorn-database-schema.png)

## customers

| Column Name | Data Type | Description | Example |
| --- | --- | --- | --- |
| **customer_id** | `int` | Unique identifier for each customer | `1` |
| **customer_name** | `text` | Full name of the customer | `Aaron Bergman` |
| **customer_segment** | `text` | Category assigned to a customer based on demographics or spending behavior | `Consumer` |

## orders

| Column Name | Data Type | Description | Example |
| --- | --- | --- | --- |
| **order_id** | `text` | Unique identifier for each order placed | `CA-2015-100004` |
| **customer_id** | `int` | Foreign key linking to the `customer_id` in the `customers` table | `91` |
| **order_date** | `timestamp` | Date when the customer placed the order | `2015-09-06` |
| **shipping_city** | `text` | City where the order is being shipped | `New York City` |
| **shipping_state** | `text` | State or region within the country | `New York` |
| **shipping_region** | `text` | Designated geographical region for logistics | `East` |
| **shipping_country** | `text` | Country where the product is being shipped | `United States` |
| **shipping_postal_code** | `int` | Postal or ZIP code for the delivery address | `10011` |
| **shipping_date** | `timestamp` | Date when the order was dispatched for delivery | `2015-09-06` |
| **shipping_mode** | `text` | Method of shipment | `Same Day` |

## order_details

| Column Name | Data Type | Description | Example |
| --- | --- | --- | --- |
| **order_details_id** | `int` | Unique identifier for each order line item (used to track multi-item orders) | `1` |
| **order_id** | `text` | Foreign key linking to the `order_id` from the `orders` table | `CA-2015-100004` |
| **product_id** | `int` | Foreign key linking to the `product_id` from the `product` table | `122` |
| **quantity** | `int` | Number of units purchased for the product in that order line | `62` |
| **order_discount** | `float` | Discount applied to the order item | `0.1` |
| **order_profits** | `float` | Net profit earned from the product sale after discount and costs | `327.0` |
| **order_profit_ratio** | `float` | Profit divided by sales amount, indicating efficiency of profit margin | `0.39` |
| **order_sales** | `int` | Total revenue from the sale before deducting costs | `837` |

## product

| Column Name | Data Type | Description | Example |
| --- | --- | --- | --- |
| **product_id** | `int` | Unique identifier for each product | `1836` |
| **product_name** | `text` | The name or title of the product as listed on Unicorn’s platform | `Xerox 230` |
| **product_category** | `text` | Broad classification of products based on type or purpose | `Office Supplies` |
| **product_subcategory** | `text` | More specific classification within the category | `Paper` |
| **product_manufacturer** | `text` | Company or brand that produced the product | `Xerox` |
