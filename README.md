# Backend - Database - Basics - Let's MonGO

## Let's monGO

Add your answers directly into this README file.

1. Explain ObjectIDs in MongoDB; what are they? 
    - They are objects, created automatically that contain one unique hexadecimal to identify each newly created entry in the database.
2. You have a collection called "users" with a document like this: `{ _id: 1, name: "Veera" }`. What query would you use to update the name to "Princess Veera Silkenfur"?
    - `db.foods.updateOne({name: "Veera"},{$set: {name: "Princess Veera Silkenfur"}});`
3. How do you make a collection?
    - `db.<collectionName>` adding a new entry in a non existent collection will create the collection as well.
4. So the (old) mongo shell is kind of like a JavaScript REPL. What is a REPL? Which other REPL have we used?
    - Read, Evaluate, Print, Loop. node.
5. So the (old) mongo shell is kind of like a JavaScript REPL. You can use things like variables, try...catch  statements and loops. Experiment with it and find at least three other JavaScript things that we have used that work in the (old) shell. If you can, try to find even more!
    - map, JSON.stringify, toString().
    - filter, indexOf,  doesn't work.
6. (Research) So the old shell is pretty cool. How is the new shell better?
    - It has autocomplete function with tab and better logging.
7. (Research) How can you insert multiple documents at the same time?
    - `db.cats.insertMany([{ name: "Veera" }, { name: "Rauli" }, { name: "BenBen" }])`
8. (Research) You have a collection called `cats` with a documents like this: `{ name: "Veera" }, { name: "Rauli" }, { name: "BenBen" }` - How can you insert the field `cute: true` into all of them with one command?
    - The following command: `db.cats.find().forEach(e => db.cats.update({_id: e._id}, {cute: true}))` will replace their "name" property with "cute" with the value *true*.
    - This will do `db.cats.update({}, {$set: {cute: true}}, false, true)` The 4th argument allows multiple modifications when set to *true*
9. (Task) Start a timer for 30 minutes. Spend all that time getting to know and reading https://docs.mongodb.com/manual/introduction/ - how far did you get? What was the most cool or interesting thing you learned?
    - Besides the fact that is a document (object) database the other concepts (like "redundancy", "Horizontal Scalability" and "Storage Engines") are foreign to me and don't make much sense, all I can say is that it sounds cool. Good job of those who wrote the documentation.
    - After that is the getting started section, which repeated a lot of what we did in the class.
10. Find one SQL Cheatsheet and one MongoDB Cheatsheet and add links to them here.
    - SQL: https://www.sqltutorial.org/wp-content/uploads/2016/04/SQL-cheat-sheet.pdf
    - MongoDB: https://blog.codecentric.de/files/2012/12/MongoDB-CheatSheet-v1_0.pdf


































🌿
