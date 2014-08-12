Referring back to 2.4 above, update those products (products that work with an "ac3" phone) and add 2 to the "price" of each of those items. Then, at the shell prompt type:

----

	homework.c()

	db.products.find({for:{$exists:1},for:"ac3"}).forEach( function(item) { printjson(item) } )
	db.products.find({for:{$exists:1},for:"ac3"}).forEach( function(item) { db.products.update({_id:item._id},{$inc:{price:2}}) } )

89.5954.5
