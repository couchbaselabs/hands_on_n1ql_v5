# Part 1: Setup, Getting Started and Querying

## Joins

The product keyspace has a list of the primary keys of its reviews.

This can be used to join a product with review detail. The query on the right shows a specific product joined with all its review ratings.

<pre id="example">

SELECT p.name, r.rating
  FROM product p INNER JOIN reviews r ON (META(r).id  IN p.reviewList)
    WHERE META(p).id  = "product320"

</pre>
