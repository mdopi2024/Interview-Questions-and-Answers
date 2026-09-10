 # MongoDB Interview Questions & Answers

## Q01. What is MongoDB and what are its main features?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB হলো একটি **NoSQL database**, যেখানে data সাধারণ database-এর মতো table ও row-তে না রেখে **document** আকারে রাখা হয়। এই document দেখতে অনেকটা JSON-এর মতো। MongoDB-এর schema flexible হওয়ায় data structure সহজে পরিবর্তন করা যায় এবং বড় application-এর জন্য এটি সহজে scale করা যায়।

### বাংলা Interview Answer

**MongoDB হলো একটি NoSQL, document-based database। এটি data-কে table ও row-এর পরিবর্তে flexible, JSON-like document আকারে store করে। এর প্রধান বৈশিষ্ট্য হলো flexible schema, high scalability, fast performance, indexing, replication এবং high availability।**

### English Interview Answer

**MongoDB is a NoSQL, document-based database. It stores data in flexible, JSON-like documents instead of tables and rows. Its main features include flexible schema, high scalability, fast performance, indexing, replication, and high availability.**

---

## Q02. How does MongoDB differ from relational databases?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB এবং relational database-এর মধ্যে মূল পার্থক্য হলো **data কীভাবে store করা হয়**। Relational database data-কে **table, row এবং column** আকারে store করে এবং সাধারণত fixed schema ব্যবহার করে। অন্যদিকে MongoDB data-কে **flexible, JSON-like document** আকারে store করে এবং flexible schema ব্যবহার করে।

### বাংলা Interview Answer

**MongoDB একটি NoSQL, document-based database, যেখানে data flexible JSON-like document আকারে store করা হয়। অন্যদিকে relational database data-কে table, row এবং column আকারে store করে এবং সাধারণত fixed schema ব্যবহার করে। MongoDB বেশি flexible এবং সহজে scale করা যায়, যেখানে relational database structured এবং relationship-based data-এর জন্য বেশি উপযোগী।**

### English Interview Answer

**MongoDB is a NoSQL, document-based database where data is stored in flexible, JSON-like documents. On the other hand, relational databases store data in tables, rows, and columns and usually use a fixed schema. MongoDB is more flexible and easier to scale, while relational databases are more suitable for structured and relationship-based data.**

---

## Q03. Can you describe the structure of data in MongoDB?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে data একটি hierarchical structure-এ থাকে। সবচেয়ে উপরে থাকে **Database**, তার ভিতরে থাকে **Collection**, এবং Collection-এর ভিতরে থাকে **Document**। প্রতিটি Document-এর ভিতরে বিভিন্ন **Field এবং Value** থাকে।

**Structure:**

`Database → Collection → Document → Field → Value`

### বাংলা Interview Answer

**MongoDB-তে data Database, Collection এবং Document-এর মাধ্যমে organize করা হয়। একটি Database-এর মধ্যে এক বা একাধিক Collection থাকে, এবং একটি Collection-এর মধ্যে অনেকগুলো Document থাকে। প্রতিটি Document-এর মধ্যে বিভিন্ন Field এবং Value থাকে। Document দেখতে অনেকটা JSON-এর মতো।**

### English Interview Answer

**In MongoDB, data is organized using databases, collections, and documents. A database can contain one or more collections, and a collection can contain many documents. Each document contains different fields and values. A document looks similar to a JSON object.**

---

## Q04. What is a Document in MongoDB?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে **Document** হলো একটি নির্দিষ্ট record বা data-এর একটি unit। এটি **JSON-like structure**-এ data store করে। যেমন, `orders` Collection-এর প্রতিটি আলাদা order একটি **Document**।

### বাংলা Interview Answer

**MongoDB-তে Document হলো data store করার একটি unit, যা JSON-like structure ব্যবহার করে। একটি Collection-এর মধ্যে প্রতিটি record, যেমন একটি order, আলাদা Document হিসেবে store হয়। একটি Document-এর মধ্যে বিভিন্ন Field এবং Value থাকে।**

### English Interview Answer

**A Document in MongoDB is a unit used to store data, which uses a JSON-like structure. Each record in a collection, such as an order, is stored as a separate document. A document contains different fields and values.**

---

## Q05. How is data stored in a collection in MongoDB?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে একটি **Collection-এর মধ্যে অনেকগুলো Document** থাকে। প্রতিটি Document একটি আলাদা record হিসেবে data store করে এবং **field-value pair** ব্যবহার করে data রাখে। যেমন, `orders` Collection-এর মধ্যে প্রতিটি order আলাদা Document হিসেবে store হয়।

### বাংলা Interview Answer

**MongoDB-তে data Collection-এর মধ্যে Document হিসেবে store করা হয়। একটি Collection-এর মধ্যে অনেকগুলো Document থাকতে পারে, এবং প্রতিটি Document একটি আলাদা record হিসেবে কাজ করে। Document-এর মধ্যে data field এবং value আকারে থাকে।**

### English Interview Answer

**In MongoDB, data is stored as documents inside a collection. A collection can contain many documents, and each document represents a separate record. The data inside a document is stored as fields and values.**

---
<!--
## Q06. Describe what a MongoDB database is.

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে **Database** হলো এমন একটি container যেখানে application-এর related data রাখা হয়। একটি Database-এর মধ্যে এক বা একাধিক **Collection** থাকে, এবং প্রতিটি Collection-এর মধ্যে অনেকগুলো **Document** থাকে।

উদাহরণ:

`E-commerce Database → orders Collection → Order Documents`

### বাংলা Interview Answer

**MongoDB Database হলো একটি container যেখানে related data রাখা হয়। একটি Database-এর মধ্যে এক বা একাধিক Collection থাকে, এবং প্রতিটি Collection-এর মধ্যে অনেকগুলো Document থাকে।**

### English Interview Answer

**A MongoDB database is a container where related data is stored. A database can contain one or more collections, and each collection can contain many documents.**

---

## Q07. What is the default port on which MongoDB listens?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-এর **default port হলো `27017`**। অর্থাৎ, MongoDB server চালু হলে সাধারণত এটি `27017` port-এ connection-এর জন্য অপেক্ষা করে।

### বাংলা Interview Answer

**MongoDB-এর default port হলো `27017`। MongoDB server সাধারণত এই port-এ client connection-এর জন্য listen করে।**

### English Interview Answer

**The default port of MongoDB is `27017`. MongoDB server usually listens on this port for client connections.**

---

## Q08. How does MongoDB provide high availability and disaster recovery?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB মূলত **Replica Set** ব্যবহার করে high availability দেয়। একটি Replica Set-এ একই data-এর একাধিক copy থাকে—একটি **Primary** এবং এক বা একাধিক **Secondary**। Primary server নষ্ট হলে একটি Secondary automatically Primary হয়ে যায়। Disaster recovery-এর জন্য MongoDB **backup** এবং **replication** ব্যবহার করা যায়।

### বাংলা Interview Answer

**MongoDB Replica Set এবং backup-এর মাধ্যমে high availability এবং disaster recovery প্রদান করে। Replica Set-এ একটি Primary এবং এক বা একাধিক Secondary server থাকে। Primary server ব্যর্থ হলে একটি Secondary automatically Primary হয়ে যায়। এছাড়া backup ব্যবহার করে data loss বা বড় ধরনের failure-এর পর data recover করা যায়।**

### English Interview Answer

**MongoDB provides high availability and disaster recovery through replica sets and backups. A replica set has one primary and one or more secondary servers. If the primary server fails, a secondary server automatically becomes the primary. Backups can also be used to recover data after data loss or a major failure.**

---

## Q09. What are the indexes in MongoDB, and why are they used?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-এর **Index** হলো এমন একটি data structure, যা নির্দিষ্ট field-এর data **দ্রুত খুঁজে পেতে** সাহায্য করে। Index ব্যবহার করলে MongoDB-কে পুরো Collection-এর সব Document একে একে check করতে হয় না। তাই **query দ্রুত হয়** এবং performance ভালো হয়।

উদাহরণ:

```js
db.users.createIndex({ email: 1 })
```

এখানে `email` field-এর উপর একটি index তৈরি করা হয়েছে।

### বাংলা Interview Answer

**MongoDB-এর Index হলো একটি data structure, যা নির্দিষ্ট field-এর data দ্রুত খুঁজে পেতে সাহায্য করে। এটি query performance improve করার জন্য ব্যবহার করা হয়। Index ব্যবহার করলে MongoDB-কে পুরো Collection scan করতে হয় না, তাই data search করা দ্রুত হয়।**

### English Interview Answer

**An index in MongoDB is a data structure that helps find data quickly based on a specific field. It is used to improve query performance. With an index, MongoDB does not need to scan the entire collection, so data search becomes faster.**

---

## Q10. What is the role of the _id field in MongoDB documents?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-এর **`_id` field** প্রতিটি Document-কে আলাদাভাবে শনাক্ত করার জন্য ব্যবহার করা হয়। প্রতিটি Document-এর `_id` **unique** হতে হয়। আমরা `_id` না দিলে MongoDB নিজে থেকে একটি unique **ObjectId** তৈরি করে।

### বাংলা Interview Answer

**MongoDB-এর `_id` field প্রতিটি Document-কে uniquely identify করার জন্য ব্যবহার করা হয়। এটি প্রতিটি Document-এর জন্য unique হতে হয়। আমরা `_id` না দিলে MongoDB automatically একটি unique ObjectId তৈরি করে।**

### English Interview Answer

**The `_id` field in MongoDB is used to uniquely identify each document. It must be unique for every document. If we do not provide an `_id`, MongoDB automatically creates a unique ObjectId.**

---

## Q11. How do you create a new MongoDB collection?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে Collection তৈরি করার দুটি সাধারণ উপায় আছে। একটি হলো **`db.createCollection()`** ব্যবহার করা। আরেকটি হলো কোনো Collection-এ প্রথমবার Document insert করা—তখন MongoDB automatically Collection তৈরি করে দেয়।

### বাংলা Interview Answer

**MongoDB-তে একটি নতুন Collection তৈরি করতে `db.createCollection()` method ব্যবহার করা যায়। যেমন, `db.createCollection("users")` লিখলে `users` নামে একটি Collection তৈরি হবে। এছাড়া কোনো Collection-এ প্রথমবার Document insert করলেও MongoDB automatically সেই Collection তৈরি করে।**

### English Interview Answer

**In MongoDB, we can create a new collection using the `db.createCollection()` method. For example, `db.createCollection("users")` creates a collection named `users`. We can also insert a document into a new collection, and MongoDB will automatically create the collection.**

---

## Q12. What is the syntax to insert a document into a MongoDB collection?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে একটি Collection-এর মধ্যে নতুন Document যোগ করতে **`insertOne()`** method ব্যবহার করা হয়। একাধিক Document একসাথে যোগ করতে **`insertMany()`** ব্যবহার করা হয়।

### বাংলা Interview Answer

**MongoDB Collection-এ একটি Document insert করার syntax হলো `db.collectionName.insertOne({ ... })`। এখানে `collectionName` হলো যে Collection-এ Document insert করতে চাই তার নাম। একাধিক Document insert করতে `insertMany()` ব্যবহার করা হয়।**

উদাহরণ:

```js
db.users.insertOne({
  name: "Opi",
  age: 18
})
```

### English Interview Answer

**The syntax to insert a document into a MongoDB collection is `db.collectionName.insertOne({ ... })`. Here, `collectionName` is the name of the collection where we want to insert the document. For inserting multiple documents, we use `insertMany()`.**

---

## Q13. Describe how to read data from a MongoDB collection.

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে Collection থেকে data পড়তে **`find()`** এবং **`findOne()`** method ব্যবহার করা হয়। `find()` এক বা একাধিক matching Document খুঁজে বের করে, আর `findOne()` সাধারণত একটি matching Document return করে।

### বাংলা Interview Answer

**MongoDB Collection থেকে data read করার জন্য `find()` এবং `findOne()` method ব্যবহার করা হয়। `find()` দিয়ে এক বা একাধিক matching Document পাওয়া যায় এবং `findOne()` দিয়ে একটি matching Document পাওয়া যায়। আমরা query দিয়ে নির্দিষ্ট condition অনুযায়ী data খুঁজতে পারি।**

### English Interview Answer

**In MongoDB, we use the `find()` and `findOne()` methods to read data from a collection. `find()` returns one or more matching documents, while `findOne()` returns one matching document. We can use a query to find data based on specific conditions.**

---

## Q14. Explain how to update Documents in MongoDB.

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে existing Document-এর data পরিবর্তন করতে **`updateOne()`**, **`updateMany()`**, এবং **`replaceOne()`** method ব্যবহার করা হয়। সাধারণত নির্দিষ্ট field পরিবর্তন করার জন্য `$set` operator ব্যবহার করা হয়।

### বাংলা Interview Answer

**MongoDB-তে Document update করার জন্য `updateOne()` এবং `updateMany()` method ব্যবহার করা হয়। `updateOne()` একটি matching Document update করে, আর `updateMany()` একাধিক matching Document update করে। নির্দিষ্ট field-এর value পরিবর্তন করতে সাধারণত `$set` operator ব্যবহার করা হয়।**

### English Interview Answer

**In MongoDB, we use `updateOne()` and `updateMany()` methods to update documents. `updateOne()` updates one matching document, while `updateMany()` updates multiple matching documents. We usually use the `$set` operator to change the value of a specific field.**

---

## Q15. What are the MongoDB commands for deleting documents?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে Document delete করার জন্য প্রধানত **`deleteOne()`** এবং **`deleteMany()`** method ব্যবহার করা হয়। `deleteOne()` একটি matching Document delete করে, আর `deleteMany()` একই condition-এর সব matching Document delete করে।

### বাংলা Interview Answer

**MongoDB-তে Document delete করার জন্য `deleteOne()` এবং `deleteMany()` command ব্যবহার করা হয়। `deleteOne()` একটি matching Document delete করে, আর `deleteMany()` একাধিক matching Document delete করে।**

উদাহরণ:

```js
db.users.deleteOne({ name: "Opi" })
```

```js
db.users.deleteMany({ age: 18 })
```

### English Interview Answer

**In MongoDB, we use the `deleteOne()` and `deleteMany()` commands to delete documents. `deleteOne()` deletes one matching document, while `deleteMany()` deletes multiple matching documents.**

---

## Q16. Can you join two collections in MongoDB? If so, how?

### সংক্ষিপ্ত ব্যাখ্যা

হ্যাঁ, MongoDB-তে দুইটি Collection-এর data একসাথে আনা যায়। এর জন্য সাধারণত **`$lookup`** aggregation stage ব্যবহার করা হয়। এটি relational database-এর **JOIN**-এর মতো কাজ করে।

যেমন, আমাদের দুটি Collection আছে:

```text
orders
users
```

`orders`-এর `userId` এবং `users`-এর `_id` match করে user-এর information order-এর সাথে আনা যায়।

### বাংলা Interview Answer

**হ্যাঁ, MongoDB-তে দুইটি Collection-এর data join করা যায়। এর জন্য `$lookup` aggregation stage ব্যবহার করা হয়। এটি relational database-এর JOIN-এর মতো কাজ করে এবং একটি Collection-এর সাথে অন্য Collection-এর matching data একসাথে আনা যায়।**

### English Interview Answer

**Yes, we can join two collections in MongoDB. We use the `$lookup` aggregation stage for this. It works like a JOIN in relational databases and allows us to bring matching data from one collection together with another collection.**

---

## Q17. How do you limit the number of documents returned by a MongoDB query?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB query-এর result-এর সংখ্যা সীমিত করতে **`limit()`** method ব্যবহার করা হয়। এটি আমাদের প্রয়োজন অনুযায়ী নির্দিষ্ট সংখ্যক Document return করতে সাহায্য করে।

উদাহরণ:

```js
db.users.find().limit(5)
```

এখানে সর্বোচ্চ **৫টি Document** return করবে।

### বাংলা Interview Answer

**MongoDB query-এর মাধ্যমে return হওয়া Document-এর সংখ্যা সীমিত করতে `limit()` method ব্যবহার করা হয়। এটি query result থেকে নির্দিষ্ট সংখ্যক Document return করে।**

### English Interview Answer

**We use the `limit()` method to limit the number of documents returned by a MongoDB query. It returns a specific number of documents from the query result.**

---

## Q18. What is the difference between find() and findOne() in MongoDB?

### সংক্ষিপ্ত ব্যাখ্যা

`find()` এবং `findOne()` দুটিই MongoDB থেকে Document খুঁজে বের করতে ব্যবহার করা হয়। মূল পার্থক্য হলো **`find()` একাধিক matching Document return করতে পারে**, আর **`findOne()` শুধু একটি matching Document return করে**।

### বাংলা Interview Answer

**`find()` এবং `findOne()` দুটিই MongoDB-তে data খুঁজে বের করার জন্য ব্যবহার করা হয়। `find()` এক বা একাধিক matching Document return করে, আর `findOne()` শুধুমাত্র একটি matching Document return করে।**

### English Interview Answer

**Both `find()` and `findOne()` are used to find data in MongoDB. `find()` returns one or more matching documents, while `findOne()` returns only one matching document.**

---

## Q19. How can you achieve pagination in MongoDB?

### সংক্ষিপ্ত ব্যাখ্যা

MongoDB-তে **pagination** করার জন্য সাধারণত `skip()` এবং `limit()` method ব্যবহার করা হয়। `limit()` কতগুলো Document দেখাবে তা নির্ধারণ করে, আর `skip()` আগের কতগুলো Document বাদ দেবে তা নির্ধারণ করে।

উদাহরণ:

```js
db.products.find()
  .skip(10)
  .limit(10)
```

এখানে প্রথম **১০টি Document বাদ দিয়ে পরের ১০টি Document** পাওয়া যাবে। অর্থাৎ এটি **page 2** হিসেবে কাজ করতে পারে, যদি প্রতি page-এ ১০টি Document থাকে।

### বাংলা Interview Answer

**MongoDB-তে pagination করার জন্য সাধারণত `skip()` এবং `limit()` method ব্যবহার করা হয়। `skip()` আগের কিছু Document বাদ দেয় এবং `limit()` প্রতি page-এ কতগুলো Document দেখাবে তা নির্ধারণ করে।**

### English Interview Answer

**In MongoDB, we usually use the `skip()` and `limit()` methods for pagination. `skip()` skips some previous documents, and `limit()` determines how many documents to show on each page.**

---

## Q20. What are the differences between MongoDB’s insertOne and insertMany methods?

### সংক্ষিপ্ত ব্যাখ্যা

`insertOne()` এবং `insertMany()` দুটিই MongoDB Collection-এ নতুন Document যোগ করার জন্য ব্যবহার করা হয়। পার্থক্য হলো, **`insertOne()` একটি Document** insert করে, আর **`insertMany()` একসাথে একাধিক Document** insert করে।

### বাংলা Interview Answer

**`insertOne()` একটি Document MongoDB Collection-এ insert করার জন্য ব্যবহার করা হয়। অন্যদিকে, `insertMany()` একসাথে একাধিক Document insert করার জন্য ব্যবহার করা হয়। তাই একটি Document insert করতে `insertOne()` এবং একাধিক Document insert করতে `insertMany()` ব্যবহার করি।**

### English Interview Answer

**We use `insertOne()` to insert one document into a MongoDB collection. On the other hand, we use `insertMany()` to insert multiple documents at once. So, we use `insertOne()` for one document and `insertMany()` for multiple documents.** -->