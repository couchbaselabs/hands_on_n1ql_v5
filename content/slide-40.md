# Part 2: Querying and Modifying Complex Data

## EXERCISE

What category has the highest rating of reviews from the year 2014?

<pre id="example">
SELECT cat, product, reviews
  FROM product 
          UNNEST product.categories AS cat
            INNER JOIN reviews ON (META(reviews).id IN product.reviewList)
     LIMIT 5 
</pre>
