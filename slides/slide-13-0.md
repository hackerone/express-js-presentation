## Database

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

</code></pre>

<pre><code>
	app.get('/book/:id', (req, res) => {
		Book.findOne({_id: req.params.id}, (err, book) => {
			if(err) // handle it
			res.render('book', {book: book});
		});
	});

</code></pre>

Note:
You can use expressjs with any of the nodejs database drivers. 

Or you could use an odm like mongoose. using an ODM gives you some cool features like input validation, pre-save post-save events and a bunch of cool features.

Things that we'll need to care about, when handling database operations is
- all the database operations are asynchronous
- we'll be getting into the callback sooner than we think.