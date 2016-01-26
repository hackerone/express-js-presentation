## Routing middleware

<pre><code>
    npm install express

</code></pre>

<pre><code>
    var http = require('http'),
    	express = require('express');
    var app = express();

    app.use('/tom', (req, res, next) => {
    	res.write('hello tom');
		res.end();
    });

    app.use((req, res, next) => {
    	res.write('hello world');
		res.end();
    });
    
	http.createServer(app).listen(3000);

</code></pre>

Note:

This is where express comes in.

Express provides an abstraction here. instead of passing your method, you can pass the express instance to the http createServer method, and express will handle your request from there.

let's get into the code here.

npm install express will download the express module and it's dependencies into your project. so you can then require it from your code.

Express uses concept of middlewares to control the flow of the request. we'll look at middlewares a bit later. but for now, app.use will add middlewares to the app's request flow.

If you look at the code there, the first middleware which returns hello tom will get executed for '/tom'.

There is case which doesn't have a URL parameter, this will get executed for all cases, other than tom.