# eecs484-project-3--mangodb-solved
**TO GET THIS SOLUTION VISIT:** [EECS484 Project 3- MangoDB Solved](https://www.ankitcodinghub.com/product/eecs-484-projects-p3-mongodb-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;121169&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EECS484 Project 3- MangoDB Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Project 3: MangoDB

Introduction

In Project 3, we will use a similar dataset as in Project 2 and explore the capabilities of MongoDB (a NoSQL DBMS). There are two parts to the project. Part A of the project does not use MongoDB. You will be extracting data from tables in the Fakebook database and exporting a JSON file output.json that contains information about users. In Part B of the project, you will be importing output.json (or a sample.json that we give you) into MongoDB to create a mongoDB collection of users. You will then need to write 8 queries on the users collection. You can start on Part A right away without knowing anything about MongoDB, whereas Part B will require you to use MongoDB.

Submissions

This project is to be done in teams of 2 students. Be sure to create your team on the Autograder.

Part A: Export Oracle Database to JSON

Introduction to JSON

JSON (JavaScript Object Notation) is a way to represent data in a key-value format, much like a std::map in C++. JSON differs from maps in C++ in that the values do not have to be consistent

in terms of data type. Here is an example of a JSON object (initialized in JavaScript):

1 var student1 = { “Name” : “John Doe”, “Age”: 21, “Major”: [“CS”, “Math”] }

In student1 , Name, Age and Major are the keys. Their corresponding value types are string, integer and array of strings. Note that JSON objects themselves can be values for other JSON objects. Below is an example of retrieving the value for a key:

With multiple JSON objects, we can create a JSON array in JavaScript:

Export to JSON

Your job for Part A is to query the Project 3 Fakebook Oracle database (tables are prefixed with project3.public_ ) to export comprehensive information on each user. The results should be

stored in a JSONArray , containing 800 JSONObjects for 800 users. It is suggested that you use multiple queries to retrieve all the information. This should feel very similar to Project 2. Each JSONObject should include:

user_id ( int ) first_name ( String ) last_name ( String ) gender ( String ) YOB ( int )

MOB ( int ) DOB ( int )

friends ( JSONArray ) that contains: all of the user ids of users who are friends with the current user, and has a larger user id than the current user. Note that Friends relationship is assumed to be symmetric. If user 700 is friends with user 25, it will show up on the list for user 25 but will not show up on the list for user 700.

current ( JSONObject ) that contains:

city state country

hometown ( JSONObject ) that contains:

city state country

Below is an example of one element of this JSONArray . It is possible that a user might have no list of friends, current city, or hometown city. In this case, put an empty JSONArray([]) as the value for the “friends” key of that user or an empty JSONObject({}) as the value for the “current” or “hometown” key of that user. See sample.json for the correct output.

Starter Files

Download the starter files (p3-starter_files.tar.gz).

For Part A, you only need to be concerned about the following files

GetData.java

Main.java Makefile sample.json

json_simple-1.1.jar, json-20151123.jar, ojdbc6.jar

GetData.java

Submit this file. Implement toJSON() by querying the users, friends, and cities tables to retrieve data from the Oracle Database. The writeJSON() function will take care of converting your output (a JSONArray ) into a JSON string stored in output.json . Feel free to use the SQL*Plus CLI; the table names are listed in the beginning of this file.

Main.java

This file provides the main driver function for running Part A. You should use it to run your program, but you donʼt need to turn it in. When Main.java is run, an output file named output.json should be generated. Modify the oracleUserName and password static variables,

replacing them with your own Oracle username and password.

1 static String oracleUserName = “uniqname”; // replace with your uniqname

2 static String password = “password”; // replace with your Oracle password (defau

Makefile

Once you have implemented GetData.java and modified Main.java , you can compile and run your program.

If your username/password combination is incorrect in Main.java , you will get an error message java.sql.SQLException: ORA-01017: invalid username/password; logon denied . If you need

to reset your password, refer to Tools.

sample.json

GetData.java . Please do not validate your output using diff output.json sample.json because JSON arrays are likely to come out in different orderings between any two runs. However,

output.json and sample.json should contain the same elements in the JSON array. There are

command line json processors that allow you to diff the contents properly. jd (github and online) and deepdiff are both valid options.

json_simple-1.1.jar, json-20151123.jar, ojdbc6.jar

These jar packages help compile your code. Do not modify them.

Wrapping Up

If youʼd like, you can also submit GetData.java from Part A on the Autograder without completing Part B.

Part B: MongoDB Queries

Introduction to MongoDB

MongoDB is a document-oriented noSQL DBMS. Each document in MongoDB is one JSON object, with key-value pairs of data, just like how a tuple in SQL has fields of data. Each collection in MongoDB is one JSON array of multiple documents, just like how a table in SQL has multiple tuples. Refer to the following table for some high-level differences between SQL and MongoDB.

SQL MongoDB

Tuple Document. Represented as a JSON object

Relation/Table Collection. Represented as a JSON array

SELECT * FROM Users;

db.users.find();

SELECT * FROM Users

WHERE name = ‘John’ AND age = 50;

db.users.find({name: ‘John’, age: 50});

SELECT user_id, addr FROM Users

WHERE name = ‘John’; db.users.find({name: ‘John’}, {user_id: 1, addr: 1, _id: 0});

Logging into MongoDB

Local MongoDB

To use MongoDB on your local machine, refer to MongoDBʼs installation instructions. Once you have installed it, you should be able to execute mongod (without a ‘bʼ) to start a private mongod server. To connect to your private server, you will generally type mongo with the database name in a Terminal window:

CAEN MongoDB

To use MongoDB on CAEN, we have set up a MongoDB server on the host eecs484.eecs.umich.edu . To connect to this server, ssh into CAEN. Double check that you have

the mongodb module loaded (see Class Modules).

Then, fill in the uniqname and password fields in the Makefile . The default MongoDB password is your uniqname. If you have the wrong login credentials, you will get the error message Error:

Authentication failed .

1 uniqname = uniqname # replace with your uniqname

2 password = password # replace with your mongoDB password (default: your uniqname

Then, login into the mongo shell. You can use this interactive shell to test queries directly on your database, similar to the SQL*Plus CLI in Projects 1 and 2.

The mongo shell will open up in your terminal. You can update your password with the following command, which will take effect when you log out.

Import JSON to MongoDB

Now that you have access to a MongoDB database, the next step is to load data into it. Open a terminal in the folder where you have sample.json (or output.json ) and Makefile . Update the Makefile with your new password and run either of the following

Refer to the Makefile for the details on the actual commands. Please do not modify the – collection users field. On success, you should have imported 800 user documents. As a reminder, sample.json is correct and given in the starter files. output.json is generated by your code from Part A.

Testing Your Queries

In the next section, you will implement 8 queries in the given JavaScript files. The file test.js contains one simple test on each of the queries. In test.js , you will need to set the dbname variable equal to your uniqname, as that will serve as the name of your database.

1 let dbname = “uniqname”; // replace with your uniqname

To run test.js , use the following Makefile command

Queries

Query 1: Townspeople

In this query, we want to find all users whose hometown city is the specified city . The result is to be returned as a JavaScript array of user ids. The order of user ids does not matter.

Query 2: Flatten Friends

In Part A, we created a friends array for every user using JDBC. Each user (JSON object) has friends (JSON array) that contains all the user_id s representing friends of the current user

who have a larger user_id . In this query, we want to restore the friendship information into a friend pair table format.

Create a collection called flat_users . Documents in the collection follow this schema:

For example, if we have the following user in the users collection:

1 { “user_id” : 100, “first_name” : “John” , … , “friends” : [ 120, 200, 300 ] }

The query would produce 3 documents (JSON objects) and store them in the collection flat_users :

You do not need to return anything for this query.

Query 3: City Dwellers

Create a collection named cities . Each document in the collection should contain two fields: a field called _id holding the city name, and a users field holding an array of user_id s who currently live in that city. The user_id s do not need to be sorted but should be distinct. For example, if users 10, 20 and 30 live in Bucklebury, the following document will be in the collection

cities :

1 {” _id” : “Bucklebury”, “users” : [ 10, 20, 30] }

You do not need to return anything for this query.

Query 4: Matchmaker

Find all user_id pairs (A, B) that meet the following requirements:

user A is “male” and user B is “female” the difference between their year of births ( YOB ) is less than the specified year_diff user A and user B are not friends

user A and user B are from the same hometown.city

Your query should return a JSON array of pairs, where each pair is an array with two user_id s. In other words, you should return an array of arrays.

Query 5: Oldest Friends

Find the oldest friend for each user who has friends. For simplicity, use only the YOB field to determine age. In case of a tie, return the friend with the smallest user_id .

Your query should return a JSON object: the keys should be user_id s and the value for each user_id is their oldest friendʼs user_id . The order of your results does not matter. The number

of key-value pairs should be the same as the number of users who have friends. The schema should look like:

Query 6: Average Friend Count

Find the average number of friends a user has in the users collection and return a decimal number. The average friend count on users should also consider those who have 0 friends. In order to make this easier, weʼre treating the number of friends that a user has as equal to the number of friends in their friend list. We are not counting users with lower ids, since they arenʼt in the friend list. Do not round the result to an integer.

Query 7: Birth Months using MapReduce

MapReduce is a powerful parallel data processing paradigm. We have set up the MapReduce calling point in test.js and you need to implement the mapper, reducer and finalizer.

Find the number of users born in each month. Note that after running test.js , running db.born_each_month.find() in the mongo shell allows you to bring up the collection showing the

Query 8: Birth Friendly Cities using MapReduce

In this query, use MapReduce to find the average friend count per user where the users have the same hometown.city . Instead of getting only one number for all usersʼ average friend count, we will have an average friend count for each hometown city.

The average calculation should be performed in the finalizer. Note that after running test.js , running db.friend_city_population.find() in mongo allows you to bring up the collection with per city average friend count. For example, if users whose hometown is Breredon have an average friend count 27.2, the document below would be in the collection:

Mapreduce Tips for Query 7 and 8

Since the output of a reducer can be fed into another reducer (reducers can take input from both mappers and reducers), the value emitted from your mapper (where the mapper emits (key, value)) should have the exact same form as what is returned by your reducer. The reducer must satisfy the following conditions:

the type of the return object must be identical to the type of the value emitted by the map function. the reduce function must be associative. The following statement must be true:

1 reduce(key, [ C, reduce(key, [ A, B ]) ] ) == reduce( key, [ C, A, B ] )

For query 8, the average calculation must be performed in the finalizer because the reducer function must be associative.

Submitting

The deliverable for Part A is GetData.java . This is worth 20 points. The deliverables for Part B are query[1-8].js . Each query is worth 10 points, with a total of 80 points. The entire project is worth 100 points. There are no private tests.

All files should be submitted to the Autograder. All test cases are graded separately, so you can submit just the files you want to have graded.

Remember to remove any print statements, as your submission will fail on the Autograder even if it compiles on CAEN.

Each team will be allowed 3 submissions per day with feedback; any submissions made in excess of those 3 will be graded, but the results of those submissions will be hidden from the team. Your highest scoring submission will be used for grading, with ties favoring your latest submission.

Acknowledgements

This document is licensed under a Creative Commons Attribution-NonCommercial 4.0

See an issue? Improve this page.
