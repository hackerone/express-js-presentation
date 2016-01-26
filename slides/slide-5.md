## Routing


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
Express provides an abstraction here. instead of passing your method, you can pass the express instance to the http createServer method, and express will handle your request from there.

If you look at the code there, in the first 2 cases of app.use we tell express to execute that function, if the URL matches /tom, /joe.

There is a third case which doesn't take a URL parameter, this will get executed for all cases, other than tom and joe.
