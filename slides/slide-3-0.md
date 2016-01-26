## starting a server in node.JS

<pre><code>
    var http = require('http');
    
	http.createServer((req, res) => {
		res.write('hello world');
		res.end();
	}).listen(3000);

</code></pre>

Note:
Writing a simple server hello world in NodeJS is pretty straight forward. 
NodeJS API provides a built-in http module, which let's you create a server. 
The createServer takes in a callback, which gets 2 parameters request and response.

as the name suggests, request gives you info about the request and response helps us write a response, in most web apps to the browser.

And here we listen to port 3000.