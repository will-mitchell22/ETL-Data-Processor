SQL Queries to demonstrate functionality

SELECT
  m.merchandise_id,
  m.merchandise_name,
  SUM(i.quantity) AS items_sold,
  SUM(i.price) AS revenue

FROM
  Merchandsise m

JOIN
  Items i ON m.merchandise_id = i.merchandise_id

GROUP BY
  m.merchandise_id, m.merchandise_name;
