Here is a SQL query with a common table expression:

WITH category_name_cte (film_id, rating, category_name) AS
  (SELECT A.film_id,
          A.rating,
          C.name
FROM film A
LEFT JOIN film_category B ON A.film_id = B.film_id
LEFT JOIN category C ON B.category_id = C.category_id)
