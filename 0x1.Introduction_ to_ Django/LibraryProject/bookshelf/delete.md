**Delete the Book**

```python
from bookshelf.models import Book
# Delete the book instance
retrieved_book.delete()

# Confirm deletion by trying to retrieve all books
books = Book.objects.all()
print(books)
# Expected output: <QuerySet []>
