# Insertion

Insert the document
```JSON
{ x : 3 , y : 4 }
```
into the temperature collection for the current database.

The collection will initially be empty, but you can (and should) check for your document after insertion. The shell will automatically add an _id field to the inserted document. You should only insert the one document. If you need to start over, click the reset button.

	db.temperature.insert({ x : 3 , y : 4 })

----

# Update

Check all that are true about the _id field:

* It must exist in every document
* It must be unique inside the collection
* It is automatically indexed
