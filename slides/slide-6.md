# Advanced Routing

<pre><code>
	app.get('/:name', (req, res) => {
		var name = req.params.name;
		res.write('hello '+ name);
		res.end();
	});
</code></pre>

Note:
Express routing  provides more cool features. You can have a parmeter in the URL.