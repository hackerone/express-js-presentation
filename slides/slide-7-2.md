## Routing module

<pre><code>
	var express = require('express'),
		user = require('./user'),
		book = require('./book');

	var app = express();

	app.use('/user', user);
	app.use('/book', book);

</code></pre>

Note:
In a bigger application, you can separate the routing logic and create controllers and bootstrap the controllers like above.

In the above case, book would export a book router and will handle all the urls starting with /book. while the user router will handle all the urls starting with user.