# Learn-MongoDB
Here we can learn About MongoDB

//mongoDB basic code -> document base collection -> store data as JSON -like format.
sql         mongo
Database =dataBase
Tables = collections
Row =Document
col =field

command
DATABASE
help -> here you can find any command
show dbs-> show list of dbs
use databaseName ->create and switch to new database .
db + Enter -> check which database you are in.
db.dropDatabase()->delete database.

COLLECTIONS
show collections
db.createCollection(name,options)
db.createCollection("std")

Db.collection.insertOne()
Db.collection.insertMany()
Db.collection.insert()

example:
show dbs
use studentsDB
db.std(collection).insertOne({name:"anis",email:anis@gmail.com,age:31,laguages:["bangla","english"]})
db.std.insertMany([{name:"anik chy",age:23,language:["bangla","Hindi"]},{name:"raj",age:23,language:["bangla","Hindi"]}])

//Read documents
db.std.find().pretty();
db.std.find({age:23}).limit(2).pretty()
db.std.find({name:"anik"})

//update document:
db.std.update({name:"anik chy"},{$set: {age : 24}})
db.std.update({age:"23"},{$set: {age : 27}})