# Insertion

	show dbs
	show collections
	db
	db.<collection>.insert({a:1})
	db.<collection>.find()
	db.<collection>.find().pretty()
	db.<collection>.find().toArray()

----

# Update

	db.<collection>.update(<where>,<doc_or_partial_update>[,<upsert>][,<multi>])

	> db.test.find()
	> db.test.insert({_id:100,x:"hello world",y:123})
	WriteResult({ "nInserted" : 1 })
	> db.test.find()
	{ "_id" : 100, "x" : "hello world", "y" : 123 }
	> myobj = db.test.findOne()
	{ "_id" : 100, "x" : "hello world", "y" : 123 }
	> myobj
	{ "_id" : 100, "x" : "hello world", "y" : 123 }
	> myobj.y
	123
	> myobj.y = 246
	246
	> myobj
	{ "_id" : 100, "x" : "hello world", "y" : 246 }

----

# Document growth/relocation
