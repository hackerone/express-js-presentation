## Views

<pre><code>
	// index.html
	&lt;html lang=&quot;en&quot;&gt;
		&lt;head&gt;
			&lt;meta charset=&quot;UTF-8&quot;&gt;
			&lt;title&gt;Hello {{name}}&lt;/title&gt;
		&lt;/head&gt;
		&lt;body&gt;
			&lt;h1&gt;Hello {{name}}!&lt;/h1&gt;
		&lt;/body&gt;
	&lt;/html&gt;
</code></pre>

Note:
And that'll render process the handlebars template and renders the output to the client.

Consolidate provides support for most of the famous template engines like jade, handlebars, nunjucks. so you choose whatever flavour you like.

Also, all the layout options and the way you manage layouts will be handled by the template engine.
