**Create the Book**

```python
from bookshelf.models import Book

# Create a Book instance
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)

# Output to confirm creation
print(book)
# Expected output: <Book: 1984>
