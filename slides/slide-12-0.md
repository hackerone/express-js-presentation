## Body parser middleware

<pre><code>
	var bodyParser = require('body-parser');
	
	app.use(bodyParser.json());
	app.use(bodyParser.urlencoded({ extended: true }));

	app.post('/', (req, res) => {
		console.log(req.body);
	});

</code></pre>

Note:

But we don't have to write our own middlewares, there's a large number of middlewares out there which can let you accomplish most common tasks.

The express team themselves support a few essential middlewares.

For example, the body parser. So expressJS on its own cannot parse the content of a POST or a cookie, it requires a middle-ware.