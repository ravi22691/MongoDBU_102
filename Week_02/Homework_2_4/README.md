Create an index on the field for. You might want to first run the following to get some context on what is present in that field in the documents of our collection:

	db.products.find({},{for:1})

After creating the index, query products that work with an "ac3" phone; that is, "ac3" is present in the product's "for" field.

* Q1: How many are there?
* Q2: Run an explain plan on the above query. How many records were scanned?
* Q3: Was an index used?

----

```
db.products.ensureIndex({for:1})
db.products.find({for:"ac3"}).count()
```
4
```
db.products.find({for:"ac3"}).explain()
```
4  
Yes
