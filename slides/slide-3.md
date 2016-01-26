## starting a server in node.JS

<pre><code>
    var http = require('http');
    
	http.createServer((req, res) => {
		res.write('hello world');
		res.end();
	}).listen(3000);

</code></pre>

Note:
Writing a simple server hello world in NodeJS is pretty straight forward. NodeJS API provides a built-in http module, which let's you create a server. And here we listen to port 3000.