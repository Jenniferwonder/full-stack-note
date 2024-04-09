---
Title: Modules & NPM
Type: D
tags:
  - NodeJS
DateStarted: 2024-01-26
DateModified: 2024-01-26
DateDo: 
DateDone: 
DateDue: 
status:
---
## Modules & NPM
- [Bundlephobia | Size of npm dependencies](https://bundlephobia.com/)  
- A module is a JS file that exports its code  
- Node has a bunch of built in modules

### How to use Modules?
- Tradition way to import a module is to use `require()` function (Common JS). Node also added support for ES modules `import/export`, but most Node.js code written in JS still uses `require()`

#### Use modules in our own code base?

- Create a new file `my-module.js` to serve as your module
- Then go to `index.js` file, create a variable for the module, then import it using `require()`
- In the module file, we can reference the object using `module.exports`, we can add properties to the object or redefine it as a new object, which will be available to use in other file

#### Use modules created by other people?

- NPM (Node package manager) which was acquired by GitHub which was acquired by Microsoft (2020.5).
- When you intall Node, you also install **NPM** which is a tool you can use to install remote packages to use in your own code.
- To use NPM
  - `npm init -y` using y flag to use the default options, which creates a `package.json` file in the root of the application which contains meta data about your project, and keeps track of the dependencies you use here.
  - `npm install express` to install Express, which is a minimal web application framework
  - The dependency object allows you to manage multiple dependencies in a project and then reinstall them all at once on a different system.
  - The actual raw source code for the dependency lives in this `node_modules` directory which should never be modified, because the `package.json` controls how this directory is built. It fetches your remote packages, saves your source code here, which should be able to be repeated on any system.
  - We can import the package installed by name `const express = require('express')`