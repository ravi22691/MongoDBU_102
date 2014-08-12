How many products have a voice limit? (That is, have a voice field present in the limits array.)

	db.products.find({"limits.voice":{$exists:1}}).count()
	> 3