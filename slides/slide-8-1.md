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
ExpressJS uses consolidate.js library to support template engines. And consolidate.js suppports about 14+ Node.JS template engines

let's go through the snippet,

the app.engine method, tells express use swig template engine if you come across any html file or file with 'html' extension.

then we set 2 app parameters, `view engine` and `views`

