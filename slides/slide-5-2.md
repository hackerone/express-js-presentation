## Routing continued...

<pre><code>
    app.get('/tom', (req, res, next) => {
    	res.write('hello tom');
		res.end();
    });

    app.post('/tom', (req, res, next) => {
    	res.write('creating tom...');
		res.end();
    });

</code></pre>

Note:
In most web apps, you would want to differentiate between the type of Request, for a typical website you'd want to handle a GET and a POST differently. and for a RESTful service, you'd want to support GET POST PUT and DELETE and sometimes pre-flight HEADs too.