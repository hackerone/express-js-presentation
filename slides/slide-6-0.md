# Advanced Routing

<pre><code>
	app.get('/:name', (req, res) => {
		var name = req.params.name;
		res.write('hello '+ name);
		res.end();
	});
</code></pre>

Note:
ExpressJS Routing mechanism doesn't stop here.

we can pass parameters in the URL's and can use them in functions.

so, the code above will match /tom /mary /joe /everyone and prints "hello "+ name