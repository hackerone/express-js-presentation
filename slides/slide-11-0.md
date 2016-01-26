## Middlewares

- a function 
- alters the flow of a request.
- app.use

<pre><code>
	app.use((req, res, next) => {
		req.name = 'tom';
		next();
	});

	app.use((req, res, next) => {
		console.log(req.name); // tom
		res.end();
	});

	app.use((req, res, next) => {
		// this middleware will not be run
		console.log('hello'); 
		res.end();
	});

</code></pre>

Note:
middleware is a function, that alters the flow of the request by modifying the request / response variables. 

it gets 3 parameters, the request, the response and next.

request will have all the request info like the url, headers etc.

response parameter will let you write / output your response.

the third parameter next, calling next will execute the next middleware in the stack.

if you look at the example, we have 3 middlewares added to the flow, the first one adds a key called 'name' and set's it a value 'tom'. since it calls next(). the next middleware in the stack will get executed. 

in this case, the second middleware prints the name set by the first middleware and it ends the request.

since the second one doesn't call next, the third one does not get called.