# **Admin Interface Configuration for Book Model**

## **Registering the Book Model**

In `bookshelf/admin.py`, the `Book` model was registered to enable admin functionalities:

```python
from django.contrib import admin
from .models import Book

@admin.register(Book)
class BookAdmin(admin.ModelAdmin):
    list_display = ('title', 'author', 'publication_year')
    list_filter = ('publication_year', 'author')
    search_fields = ('title', 'author')
