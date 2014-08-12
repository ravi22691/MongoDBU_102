Now convert the mongod instance (the one in the problem 4.1 above, which uses �--dbpath 1�) to a single server replica set. To do this, you�ll need to stop the mongod (NOT the mongo shell instance) and restart it with �--replSet� on its command line. Give the set any name you like.

Then go to the mongo shell. Once there, run
```
rs.initiate()
```
When you first ran homework.init(), we loaded some data into the mongod. You should see it in the replication database. You can confirm with:
```
use replication
db.foo.find()
```
Once done with that, run
```
homework.b()
```
in the mongo shell and enter that result below.

----

5002
