## Routing continued...

<pre><code>
	
	curl http://localhost:3000/tom
	hello tom

	curl -X POST http://localhost:3000/tom
	creating tom...

</code></pre>


Note:
So, when you make a GET request to the url, you get hello tom, while a post will return "creating tom..."