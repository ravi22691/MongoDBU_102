At the beginning of the section, "W Timeout and Capacity Planning", Dwight mentioned something that hasn't yet been touched upon in this class: Batch Inserts.

He mentions that you can find information on them in the docs, but he hasn't used them in the shell during this course.

Your job is to look this functionality up in the documentation, and use it for the following problem:

Please insert into the m102 collection, the following 3 documents, using only one shell query (please use double quotes around each key in each document in your answer):

* { "a" : 1 }
* { "b" : 2 }
* { "c" : 3 }

_Hints: This is not the same as the Bulk() operations, which were discussed earlier in this course. Also, this does not involve semicolons, so don't put any into the text box. You probably want to test this on your machine, and then copy and paste the insert query in the box below. Do not include the > sign from the beginning of the shell._

----

```
db.m102.insert(
   [
     { "a" : 1 },
     { "b" : 2 },
     { "c" : 3 }
   ]
 )
 ```
