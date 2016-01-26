## Cookie parser middleware

<pre><code>
	var cookieParser = require('cookie-parser');

	app.get('/', (req, res) => {
		console.log(req.cookies); // undefined
	});

	app.use(cookieParser());

	app.get('/', (req, res) => {
		console.log(req.cookies);
	});

</code></pre>

Note:
This is a cookie parser middleware for getting the cookie information from the request header.
