## Other request / response methods

<pre><code>
	res.json({
		message: 'hello',
		name: 'world'
	});

	res.redirect('hello/world');

	res.redirect(301, 'hello/world');

</code></pre>

Note:
Apart from the views, express also offers a bunch of response helper methods for returning a json or redirect header and cookies.