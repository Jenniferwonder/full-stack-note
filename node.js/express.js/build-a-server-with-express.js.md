---
title: Build a Server with Express.js
type: D
tags:
  - NodeJS
DateStarted: 2024-01-26
DateModified: 2024-04-17
status: 
---

## Build a Server with Express.js

![z-express-server-example.png](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/z-express-server-example.png)

- Accept json as the data format
- Listen to port 3000
- 2 endpoints
- Unix
  - Launch server
    - `node server.js`
  - `curl`
    - Allow to send data to servers and retrieve data from servers using different protocols
    - Default: get request
      - `curl localhost:3000/hello`
    - Default: post request
      - `curl --header 'content-type: application/json' localhost:3000/hello --data'{"foo":"bar"}'`

## Build a full-stack application and deploy it to the cloud.

Our **Server** will live on a URL. When user makes a request to this URL in the browser, the Server will response with some HTML.

- In our code, we'll first create an instance of an **Express app**, which allows us to <u>create different URLs and endpoints</u> that a user can navigate to in the browser,
- Then we define code in the server to **handle those requests** ("I don't want to get too deep into HTTP"). When the user navigates to a URL inthe browser, it's what's known as a `get` request, meaning they are requesting some data on the server and not trying to modify or update anything.
- With Express, we can set up an endpoint like that by calling `app.get()`,

  - and then **the first argument** is the **URL** that the user will navigate to. We use a forward slash `/` for the root URL but feel free to create **multiple pages** for your web app by creating different URLs.
  - The second argument is our **callback function**. You can think of every request to this URL as an event and then you handle that event with this function.
  - Express gives us two params to make use of, the **request** and **response**.
  - **Request** is the incoming data from the user. In some cases, you might want to look at the **headers** or the **body** of the request to authenticate a user or understand what the user is trying to do.
  - **Response** is your outgoing data

    - At this point,we need to implement the code to handle the request - reading some HTML from our file system and then send it back down to the browser.
    - ![pasted-image-20230301110202.png](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/pasted-image-20230301110202.png)

  - Now we have a way to send HTML from the Server to the Client.

- Now we need to tell our Express app to **start listening** to incoming requests.
  - We do that by defining a port which will normally come from `process.env.PORT`, a node environment variable,
  - Then we call `app.listen()` with that port, and when it starts up, we'll `console.log('App available on http://localhost:3000')`
  - You can start it up by opening the command line and running Node with the current working directory `node .`.
  - If you go ahead and open it in the browser, you should see your HTML returned back to you.
- The callback can be very difficult to work with as your app grows in complexity. It often leads to a state known as **callback hell** where. To avoid this, use `promise`.

- ![pasted-image-20230301111713.png](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/pasted-image-20230301111713.png)
  - ![pasted-image-20230301111654.png](https://cdn.jsdelivr.net/gh/jenniferwonder/bimg/full-stack/pasted-image-20230301111654.png)
