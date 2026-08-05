# Object-Oriented Programming — Bookstore

A Python project modeling two objects found in a bookstore: a `Book` and a `Coffee`,
built using object-oriented programming principles including `__init__`, property
validation, and instance methods.

## Setup

1. Clone the repository:
```sh
   git clone <repo-url>
   cd python-oop1-lab
```
2. Install dependencies:
```sh
   pipenv install
```
3. Enter the virtual environment:
```sh
   pipenv shell
```
4. Run the test suite:
```sh
   pytest -x
```
   Or run the two test files individually:
```sh
   pytest -x testing/book_test.py
   pytest -x testing/coffee_test.py
```

## Classes

### `Book` (`lib/book.py`)

Represents a book with a title and page count.

- **Attributes:**
  - `title` — the book's title
  - `page_count` — must be an integer; if set to a non-integer, prints
    `"page_count must be an integer"`
- **Methods:**
  - `turn_page()` — prints `"Flipping the page...wow, you read fast!"`

### `Coffee` (`lib/coffee.py`)

Represents a coffee sold by the store.

- **Attributes:**
  - `size` — must be `"Small"`, `"Medium"`, or `"Large"`; if set to anything else,
    prints `"size must be Small, Medium, or Large"`
  - `price` — the coffee's price
- **Methods:**
  - `tip()` — prints `"This coffee is great, here's a tip!"` and increases the price by 1

## Usage

```python
from lib.book import Book
from lib.coffee import Coffee

book = Book("And Then There Were None", 272)
book.turn_page()  # "Flipping the page...wow, you read fast!"

coffee = Coffee(size="Large", price=3.50)
coffee.tip()  # "This coffee is great, here's a tip!"
print(coffee.price)  # 4.50
```

## Testing

All functionality is covered by pytest tests in the `testing/` directory:

```sh
pytest -x
```

## Screenshot

<!-- Add a screenshot of your passing test output here, e.g.: -->
<!-- ![Passing tests](./screenshot.png) -->