# E-Commerce Sales & Customer Analytics Using SQL

## Business objective
Analyze e-commerce orders, customers, and products to understand revenue trends, customer behavior, product performance, payment preferences, and regional performance.

## Dataset
Synthetic practice dataset created for this portfolio project. It is not real customer data.

- `customers.csv`: customer profile, location, signup date
- `products.csv`: product catalog, category, cost and selling price
- `orders.csv`: order date, customer, order status, payment method
- `order_items.csv`: products and quantities per order

## Suggested workflow
1. Create the database and tables using `01_database_setup.sql`.
2. Import CSV files in this order: customers, products, orders, order_items.
3. Validate row counts and relationships.
4. Perform data-quality checks.
5. Analyze sales, products, customers, payments, and regions.
6. Write business insights based on query results.

## Important metric definition
For this project, gross item sales can be calculated as `quantity * selling_price`. When reporting completed sales, filter to `order_status = 'Delivered'`. Keep cancelled and returned orders separate rather than silently treating them as completed sales. This dataset does not include discounts, shipping fees, or tax.

## Relationships
- `orders.customer_id` -> `customers.customer_id`
- `order_items.order_id` -> `orders.order_id`
- `order_items.product_id` -> `products.product_id`

## SQL skills to demonstrate
SELECT, WHERE, GROUP BY, HAVING, JOINs, CASE, subqueries, CTEs, date functions, aggregate functions, and window functions (RANK, DENSE_RANK, ROW_NUMBER, LAG).
