## Database

- can use any nodeJS database drivers
- mongoDB, rethinkDB
- mongoose ODM

<pre><code>
	var mongoose = require('mongoose');
	mongoose.connect('mongodb://localhost/library');

	var Book = mongoose.model('Book', { name: String });

	app.post('/book', (req, res) => {
		var book = new Book({
			name: req.body.name
		});

		book.save((err) => {
			if(err) // handle it
			res.redirect('/book/'+book._id);
		})
	});

	app.get('/book/:id', (req, res) => {
		Book.findOne({_id: req.params.id}, (err, book) => {
			if(err) // handle it
			res.render('book', {book: book});
		});
	});

</code></pre>

Note:
You can use expressjs with any of the nodejs database drivers. 

Or you could use an odm like above. Things that we'll need to care about, when handling database operations is
- all the database operations are asynchronous
- we'll be getting into the callback sooner than we think.