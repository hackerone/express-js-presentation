## Advanced routing

<pre><code>
	app.get('/:name(\\w{3})', (req, res) => {
		var name = req.params.name;
		res.write('hello '+ name);
		res.end();
	});
</code></pre>

Note:
Routing even supports regex matching. So i can be rude and say hello only to people who's names are exactly 3 letters long.
