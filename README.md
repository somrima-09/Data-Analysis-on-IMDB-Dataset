# IMDB Movie Analytics (SQL)
Analyzed IMDB datasets using MySQL to provide insights and recommendations for RSVP Movies on profitable genres, directors, and actors.

## Tech Stack
- MySQL (Joins, Views, Subqueries, Window Functions)

## Key Analysis
- Merged multiple tables for clean relational data
- Analyzed ratings, revenues, and audience trends
- Identified top 5 ROI genres and high-performing directors/actors

## Sample Query
```sql
SELECT genre, ROUND(AVG(r.avg_rating),2) AS avg_rating
FROM movies m
JOIN ratings r ON m.id = r.movie_id
GROUP BY genre
ORDER BY avg_rating DESC;
