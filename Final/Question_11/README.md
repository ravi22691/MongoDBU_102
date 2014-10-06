In this problem, we will be testing your ability to use MMS monitoring. You will run a script locally that will generate a certain number of updates per second on your mongod, and will read out your system behavior in MMS.

First, install MMS Monitoring, as instructed in the lesson in chapter 7.

Next, download and run loadGenerator.js in the shell:

```bash
$ mongo --shell loadGenerator.js
```

and run the loadM102() method

```javascript
> loadM102()
```

The loadM102 function will repeatedly update a document in the loadtest collection in the m102 database. If the collection is present when the function is called, it will be dropped and recreated. Demonstrate your proficiency with MMS Monitoring by selecting the number of update operations that occur per second (operations/second are the units that the "opcounters" graph displays) while your database is loaded. You should only need to let the function run for a few minutes before you can see the answer.

The loadM102 function will not perform the same number of updates every second (you can see a more granular view of its behavior by spinning up mongostat), but they will average out to the correct answer over time. In MMS, a one-minute resolution on your time series graph should be a large enough timespan for you to see the answer (though it may jump around slightly), but if you want to smooth things out, go to a 5 minute resolution.

When you have viewed the load in MMS, answer the following question: Roughly how many updates per second does the testMMS() function perform, on average?

*The loadMMS() function will run for about 2 hours if you leave it alone, but when you're done solving the problem, you can exit the mongo shell to terminate it.*
* 0-15 updates per second
* 16-30 updates per second
* 31-45 updates per second
* 46-60 updates per second
* 61+ updates per second

----

* 0-15 updates per second
