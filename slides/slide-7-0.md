## Routing module

<pre><code>
	var express = require('express');
	var router = express.Router();

	router.get('/profile', (req, res) => {
		res.write('profile');
		res.end();
	});

	router.get('/status', (req, res) => {
		res.write('active');
		res.end();
	});

	app.use('/user', router);

</code></pre>

Note:
When the app grows, you'd want to manage the routes in a modular way.

And express provides a separate smaller router component to achieve this.

In case of the example above, we're adding a sub-router for /user

so, any url's that has /user as the first part will be handed over to the router.
