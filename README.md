# Motorcycle Parts Sales Analysis

![motorcycle](https://github.com/user-attachments/assets/4923eae3-9484-487a-8b0c-97ded8f8aa45)

## Analyzing Wholesale Revenue

This report details an analysis of sales data for a motorcycle parts company. The company operates three warehouses, **North**, **Central**, and **West**, and serves both retail and wholesale clients. The board of directors requested a deeper understanding of wholesale revenue performance across different product lines, broken down by month and warehouse.
The primary objective was to calculate the net revenue for each product line for wholesale orders, providing a granular view of performance from June to August 2021.

## The Dataset

The analysis was performed using a single table from the company's database named `sales`. This table contains detailed information about each transaction.

### `sales` table schema

| Column | Data type | Description |
|---|---|---|
| `order_number` | `VARCHAR` | Unique order number. |
| `date` | `DATE` | Date of the order, from June to August 2021. |
| `warehouse` | `VARCHAR` | The warehouse that the order was made from. |
| `client_type` | `VARCHAR` | Whether the order was `Retail` or `Wholesale`. |
| `product_line` | `VARCHAR` | Type of product ordered. |
| `quantity` | `INT` | Number of products ordered. |
| `unit_price` | `FLOAT` | Price per product (dollars). |
| `total` | `FLOAT` | Total price of the order (dollars). |
| `payment` | `VARCHAR` | Payment method—`Credit card`, `Transfer`, or `Cash`. |
| `payment_fee` | `FLOAT` | Percentage of `total` charged as a result of the `payment` method. |

## Analysis and Findings

To meet the board's request, a single, comprehensive SQL query was executed. This query was designed to:

1.  Filter the data to include only `Wholesale` transactions.
2.  Extract the month from the `date` column and represent it as a name (e.g., 'June', 'July').
3.  Calculate the `net_revenue` by summing the order totals and subtracting the sum of the payment fees.
4.  Group the aggregated results by `product_line`, `month`, and `warehouse`.
5.  Order the final output for readability.

The query successfully generated a detailed breakdown of wholesale net revenue. The results provide a clear view of how different product lines performed at each location over the three-month period.
For example, the analysis reveals that the **Engine** product line generated the highest net revenue in a single period, bringing in **$9,528.71** at the **Central** warehouse in **August**. In contrast, the **Suspension & traction** product line had its best performance in **June** at the **North** warehouse, with a net revenue of **$8,065.74**.

## Conclusion

The analysis provides the board of directors with the exact data requested, showing a clear, month-by-month breakdown of wholesale net revenue for each product line and warehouse. This granular report can be used to identify top-performing product lines, assess warehouse efficiency, and inform strategic decisions regarding inventory, marketing, and sales targets for the wholesale segment of the business.

## Tools Used

  * **SQL**
