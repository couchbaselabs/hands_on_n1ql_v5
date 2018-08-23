# Part 1: Setup, Getting Started and Querying

## EXERCISE

Find the top 3 rated products.

Use the product and reviews keyspaces.

Only include products with more than 10 reviews.

<pre id="example"> 
SELECT p, r
  FROM product p INNER JOIN reviews r ON (META(r).id IN p.reviewList)
    LIMIT 3
</pre>
