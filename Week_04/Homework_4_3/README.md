Now add two more members to the set. Use the 2/ and 3/ directories we created in homework 4.1. Run those two mongod's on ports 27002 and 27003 respectively (the exact numbers could be different).

Remember to use the same replica set name as you used for the first member.

You will need to add these two new members to your replica set, which will initially have only one member. In the shell running on the first member, you can see your replica set status with
```
rs.status()
```
Initially it will have just that first member. Connecting to the other members will involve using
```
rs.add()
```
. For example,
```
rs.add("localhost:27002")
```
You'll know it's added when you see an
```JSON
{ "ok" : 1 }
```
document.

Your machine may or may not be OK with 'localhost'. If it isn't, try using the name in the "members.name" field in the document you get by calling rs.status() (but remember to use the correct port!).

Once a secondary has spun up, you can connect to it with a new mongo shell instance. Use
```
rs.slaveOk()
```
to let the shell know you're OK with (potentially) stale data, and run some queries. You can also insert data on your primary and then read it out on your secondary. Once the servers have sync'd with the primary and are caught up, run (on your primary):
```
homework.c()
```
and enter the result below.

----

5
