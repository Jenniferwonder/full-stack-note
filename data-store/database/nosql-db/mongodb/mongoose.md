---
Title: Mongoose
tags: TechSkills
DateStarted: 2023-03-21 
DateModified: 2023-03-21
status:
sr-due: 2023-07-02
sr-interval: 4
sr-ease: 270
---

## Reference

[Mongoose v7.0.2: Getting DateStarted](https://mongoosejs.com/docs/index.html)
[Getting DateStarted with MongoDB & Mongoose | MongoDB](https://www.mongodb.com/developer/languages/javascript/getting-DateStarted-with-mongodb-and-mongoose/)

## What?

Mongoose is an ODM (Object Data Modeling) or Object Relational Mapping (ORM) library for MongoDB.

## How to start

#### 1. Install Mongoose and Nodemon

- `npm init -y`
- `npm i mongoose`
- `npm i -D nodemon`
  - Auto refresh our script file every time we make a change
- change package.json > script
  - We will use ES Modules instead of Common JS, so we’ll add the module `type` as well. This will also allow us to use top-level `await`.

```json
  "scripts": {
    "dev": "nodemon script.js",
    "devBlog": "nodemon mongo.js"
  },
  "type": "module",
```

#### 2. Connect Mongoose to Database

```js
import mongoose from "mongoose";
mongoose.connect("mongodb://127.0.0.1:27017/blog");
```

## Core Concepts

#### 1. Create a Schema

With Mongoose, everything is derived from a [Schema](https://mongoosejs.com/docs/guide.html).

```js
const kittySchema = new mongoose.Schema({
	name: String,
});
```

#### 2. Add Methods (Middleware)

added a custom document method

```js
kittySchema.methods.speak = function speak() {
	const greeting = this.name
		? "Meow name is " + this.name
		: "I don't have a name";
	console.log(greeting);
};
```

#### 3. Compile Schema into a Model

[Mongoose v7.0.2: Models](https://mongoosejs.com/docs/models.html)
A model is a class with which we construct documents.
with `mongoose.model()`

```js
const Kitten = mongoose.model("Kitten", kittySchema);
```

#### 4. Create new Document instances

```js
const silence = new Kitten({ name: "Silence" });
console.log(silence.name); // "Silence"
const fluffy = new Kitten({ name: "fluffy" });
fluffy.speak(); // "Meow name is fluffy"
```

#### 5. Save documents to MongoDB

Each document can be saved to the database by calling its [save](https://mongoosejs.com/docs/api/model.html#model_Model-save) method.

```js
await fluffy.save();
```

#### 6. Find and Filter

If we want to filter our kittens by name, Mongoose supports MongoDBs rich [querying](https://mongoosejs.com/docs/queries.html) syntax.

```js
const kittens = await Kitten.find();
await Kitten.find({ name: /^fluff/ });
// Find a single blog post
const firstArticle = await Blog.findOne({});
// Find by ID
const article = await Blog.findById("64197980b5bae25b76ae3a84").exec();
```

#### 7. Delete

#### 8. Validation

Validators only run on the create or save methods.

#### 9. Other methods

`exists()`

- returns either `null` or the ObjectId of a document that matches the provided query.
  `where()`
- chain and build queries
  `select()`

#### 10. Multiple Schemas

Generally, in MongoDB, data that is accessed together should be stored together. (You should plan this out ahead of time if possible. Nest data within the same schema when it makes sense.)

## Middleware

middleware are functions that run before and/or during the execution of asynchronous functions at the schema level
