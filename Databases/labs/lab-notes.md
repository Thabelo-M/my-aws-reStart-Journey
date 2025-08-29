# Database Lab: Writing SQL Queries

## Objective
Use SELECT, WHERE, and JOIN clauses on multiple tables

## Sample Query
```sql
SELECT users.name, orders.amount
FROM users
JOIN orders ON users.id = orders.user_id
WHERE orders.amount > 100;
```

## Reflection
JOINs were tricky at first. The key is understanding how tables relate to each other using foreign keys.
