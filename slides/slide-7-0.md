## Routing module

<pre><code>
	var express = require('express');
	var router = express.Router();

	router.get('/profile', (req, res) => {
		res.write('profile');
		res.end();
	});

	router.get('/status', (req, res) => {
		res.write('profile');
		res.end();
	});

	app.use('/user', router);

</code></pre>

Note:
To make the routing modular, express provides a separate smaller router component, which is a middleware itself.