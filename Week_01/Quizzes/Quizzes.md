# Quiz: JSON Syntax 
```XML
<person>
  <name>John</name>
  <age>25</age>
  <address>
    <city>New York</city>
    <postalCode>10021</postalCode>
  </address>
  <phones>
    <phone type="home">212-555-1234</phone>
    <phone type="mobile">646-555-1234</phone>
  </phones>
</person>
```
```JSON
{ 
    "name": "John",    
    "age": 25,    
    "address": {        
        "city": "New York",
        "postalCode": "10021"
    },
    "phones": [
        { "phone": "212-555-1234", "type": "home" },
        { "phone": "646-555-1234", "type": "mobile"}
    ]
}
```

----

# Quiz: Cursors Introduction

In order to query a collection in the mongo shell, we can type which of the following?
	db.collection.find() 

----

# Query Language: Basic Concepts

You have a collection where every document has the same fields, and you want to look at the value of the “_id”, "name", and “email” fields in order to see their format. Furthermore, you want to eliminate all other fields from the query results. What query might you write?
	db.collection.find( { } , { name: 1 , email: 1 } ) 

----

# Quiz: Query Language: Projection

You want to query the “people” collection, you want the results of the query to include only documents where age is 50, and you want to look at all fields except “email”. What query should you write?
	db.people.find( { age : 50 } , {email: 0 } ) 

----

# Quiz: Query Language: Advantages of a Dynamic Schema

If you want to add a new key: value pair to the documents in the “shapes” collection, what methods could you use?

	db.shapes.update() 
	db.shapes.save()

----

# Quiz: Shell: Queries 

We have sample documents in our products collection such as:
```JSON
{
  name: "AC1 Case Green",
  color: "green",
  price: 12.00,
  for: "ac1",
  type: ["accessory", "case"],
  available: true
}
```
How would we query in the shell for all products that are cases for an ac9 phone? That is, where type contains the value "case" and for equals "ac9"? 

	db.products.find({for: "ac9",type: "case"})

----

# Quiz: Sorting

If you want to run a query on the collection, “books,” and sort ASCIIbetically by title on the query, which of the following will work?

	db.books.find().sort( { title : 1 } ) 

----

# Quiz: Query Language: Cursors

Recall the documents in the scores collection:
```JSON
{
	"_id" : ObjectId("50844162cb4cf4564b4694f8"),
	"student" : 0,
	"type" : "exam",
	"score" : 75
}
```
Write a query that retrieves exam documents, sorted by score in descending order, skipping the first 50 and showing only the next 20

	db.scores.find({type:"exam"}).sort({score:-1}).skip(50).limit(2)
