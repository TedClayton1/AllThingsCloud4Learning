
What is a query hash?

The query_hash is **a value computed from the canonicalized text of an SQL statement**. This means that queries with exactly the same text will yield the same query_hash. Even queries with minor differences, such as case-insensitive identifiers or variable names, will share the same hash.