## Middlewares for Auth

<pre><code>
  var auth = (req, res, next) => {
    if(req.headers['let-me-in'] == true) {
      next();
    } else {
      res.render('error');
    }
  }

  app.use(auth);

  app.get('/', (req, res, next) => {
    res.render('index');
  });

</code></pre>

Note:
Middlewares can also be used for authentication, for example you can have an auth middleware which checks if an auth header is present and blocks the flow.