
**Retrieve the Book**

```python
# Retrieve and display all attributes of the book
retrieved_book = Book.objects.get(id=book.id)
print(retrieved_book.title, retrieved_book.author, retrieved_book.publication_year)
# Expected output: 1984 George Orwell 1949
