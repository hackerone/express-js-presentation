## starting a server in node.JS

<pre><code>
    var http = require('http');
    
	http.createServer((req, res) => {
		if(req.url == '/') {
			res.write('hello world');
		} else if(req.url == '/tom'){
			res.write('hello tom')
		} else if(req.url == '/joe'){
			res.write('hello joe')
		}
		res.end();
	}).listen(3000);

</code></pre>

Note:
But a web app has multiple end points or pages. So,when we need more URLs, we tend to add a logic inside the callback and that makes the code a bit ugly and makes it un-maintainable. We need an abstracted layer which let's us build web apps in a more manageable way.