# ExpressWorks

This repository hosts my solutions for the [NodeSchool](https://nodeschool.io)'s workshop [ExpressWorks](https://github.com/azat-co/expressworks)

## Solutions

1. ### Hello World

  Create an Express.js app that outputs "Hello World!" when somebody goes to `/home`.

  The port number will be provided to you by expressworks as the first argument of
  the application, i.e., `process.argv[2]`.

  [Solution](hello-world/)
  
2. ### Static

  This exercise is about serving static assets like HTML files.
  There are many ways to do it, but we want you to apply static middleware to serve the file index.html.

  Please don't use ANY routes like app.get. ONLY static.

  Your solution must listen on the port number supplied by process.argv[2].

  The index.html file is provided and usable via the path supplied by
  process.argv[3]. However, you can use your own file with this content (beware of whitespace):
  ```
  <html>
    <head>
      <title>expressworks</title>
      <link rel="stylesheet" type="text/css" href="/main.css"/>
    </head>
    <body>
      <p>I am red!</p>
    </body>
  </html>
  ```

  [Solution](static/)

3. ### Pug

  Create an Express.js app with a home page rendered by the Pug template engine.

  The home page should respond to `/home`.

  The view should show the current date using `new Date.toDateString()`.

  We use `toDateString()` to simply return the date in a human-readable format
  without the time.

  [Solution](pug/)

4. ### Good Old Form

  Forms are important. This exercise will teach you how to process the traditional (non-AJAX) web form.

  Write a route ('/form') that processes HTML form input
  (`<form><input name="str"/></form>`) and prints the value of str backwards.

  To handle a POST request, use the post() method which is used the same way as get():

    ```
    app.post('/path', function(req, res){...})
    ```

  Express.js uses middleware to provide extra functionality to your web server.

  Simply put, a middleware is a function invoked by Express.js before your own
  request handler.

  Middleware provide a large variety of functionality such as logging, serving
  static files, and error handling.

  A middleware is added by calling use() on the application and passing the
  middleware as a parameter.

  To parse x-www-form-urlencoded request bodies, Express.js can use urlencoded()
  middleware from the body-parser module.

    ```
    var bodyparser = require('body-parser')
    app.use(bodyparser.urlencoded({extended: false}))
  ```

  [Solution](good-old-form/)

