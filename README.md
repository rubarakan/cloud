# cloud
SELECT 
   refresh_date AS Day, 
   term AS Top_Term, 
   rank 
FROM `bigquery-public-data.google_trends.top_terms` 
WHERE 
   rank = 1 
   AND refresh_date
SELECT 
   refresh_date AS Day, 
   term AS Top_Term, 
   rank 
FROM `bigquery-public-data.google_trends.top_terms` 
WHERE 
SELECT 
   refresh_date AS Day, 
   term AS Top_Term, 
   rank 
FROM `bigquery-public-data.google_trends.top_terms` 
WHERE 
   rank <= 3
   AND region = 'UK'
   AND refresh_date >= DATE_SUB(CURRENT_DATE(), INTERVAL 1 MONTH)
GROUP BY Day, Top_Term, rank 
ORDER BY Day DESC;

   rank <= 3
   AND refresh_date >= DATE_SUB(CURRENT_DATE(), INTERVAL 1 MONTH)
GROUP BY Day, Top_Term, rank 
ORDER BY Day DESC;
SELECT 
   t.refresh_date AS Day, 
   t.term AS Top_Term, 
   t.rank, 
   c.category 
FROM `bigquery-public-data.google_trends.top_terms` t
JOIN `bigquery-public-data.google_trends.term_categories` c
ON t.term = c.term
WHERE 
   t.rank <= 3
   AND t.refresh_date >= DATE_SUB(CURRENT_DATE(), INTERVAL 1 MONTH)
GROUP BY Day, Top_Term, rank, category 
ORDER BY Day DESC;
Add region
