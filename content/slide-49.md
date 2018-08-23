# Part 2: Querying and Modifying Complex Data

## DML

Documents can be deleted with a DELETE statement. 

This statement deletes one specific document, with primary key "baldwin".

DELETE and UPDATE can take an optional WHERE clause.

DELETE FROM contacts will empty the keyspace!!

<pre id="example">
DELETE FROM contacts 
  WHERE META(contacts).id = "baldwin" 
   RETURNING contacts
</pre>
