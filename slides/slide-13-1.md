## Database with promise

<pre><code>
	var mongoose = require('mongoose');
	mongoose.connect('mongodb://localhost/library');

	var Book = mongoose.model('Book', { name: String });

	app.post('/book', (req, res) => {
		var book = new Book({
			name: req.body.name
		});

		var operation = book.save();

		operation.then((book) => {
			res.redirect('/book/'+book._id);
		});

	});

	app.get('/book/:id', (req, res) => {
		var query = Book.findOne({_id: req.params.id});
		
		query.then( (book) => {
			res.render('book', {book: book});
		});
	});

</code></pre>

Note:

Try to use promise whenever possible. this makes the code maintainable.

