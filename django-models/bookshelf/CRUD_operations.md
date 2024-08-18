
**Step 6: Document CRUD Operations**

Create a file named `CRUD_operations.md` and include all the CRUD operations (Create, Retrieve, Update, Delete) documented above. Each operation should be described in its own section.

```md
# ***CRUD_operations.md**

## **Create**
```python
from bookshelf.models import Book

# Create a Book instance
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)

# Output to confirm creation
print(book)
# Expected output: <Book: 1984>

# Retrieve and display all attributes of the book
retrieved_book = Book.objects.get(id=book.id)
print(retrieved_book.title, retrieved_book.author, retrieved_book.publication_year)
# Expected output: 1984 George Orwell 1949

# Update the title of the book
retrieved_book.title = "Nineteen Eighty-Four"
retrieved_book.save()

# Output to confirm update
print(retrieved_book.title)
# Expected output: Nineteen Eighty-Four

# Delete the book instance
retrieved_book.delete()

# Confirm deletion by trying to retrieve all books
books = Book.objects.all()
print(books)
# Expected output: <QuerySet []>


### Step 7: Push to GitHub

Push your code and documentation to the specified GitHub repository:

```bash
git add .
git commit -m "Added bookshelf app and documented CRUD operations"
git push origin main
