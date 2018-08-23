# Part 1: Setup, Getting Started and Querying

## EXERCISE

Find the customers with the most purchases in the states of California, Texas and New York.

Combine the customer first and last name as a single field.

Modify the query to only include purchases made in the 4th quarter of 2013.

<pre id="example">
SELECT c, p
  FROM purchases p 
       INNER JOIN customer c ON (p.customerId = META(c).id)
    LIMIT 3
</pre>
