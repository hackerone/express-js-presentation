## Views


<pre><code>
	var express = require('express'),
		cons = require('consolidate'),
		app = express();

	app.engine('html', cons.handlebars);
	app.set('view engine', 'html');
	app.set('views', __dirname + '/views');

	app.get('/', (req, res) => {
		res.render('index', {
			name: 'world'
		});
	});

</code></pre>

Note:
ExpressJS uses consolidate.js library to support template engines. And since consolidate.js suppports about 14+ NodeJS template engines, they can be utilized in the express app.

let's go through the snippet,

then we call app.engine method, which tells express use handlebars template engine to parse all the html files.

we call app.set, which sets let's you manage express config.

then we set 'view engine', 'html' which is the engine we just defined and 'views' to the absolute path of directory which contains all the view files.

then inside our middleware, we call res.render, which takes in 2 parameters, the view and the data that needs to be passed to the view.

the template engine, in our case handlebars will render the view file with the data passed.
