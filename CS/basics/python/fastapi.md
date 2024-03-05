```from fastapi import FastAPI

app = FastAPI()

@app.get('/')
async def first_api():
  return {"message":"Hello Dias" }

                      path parameters & query parameters
localhost:8000/books/authorOne/?category=science
@app.get('/books/{book_author}')
async def first_api(book_author: str,category: str):
  return {"message":"Hello Dias" }


@app.post('/books/create')
async def create_book(new_book=Body()):
Books.append(new_book)

Class Book:
  id: int
  title: str
  description: str

@app.post('/books/create')
async def create_book(book_request=BooksRequest):
new_book =Book(**book_request.dict())   // converting the request to Book object
Books.append(new_book)

@app.post('/books/update')
async def update_book(updated_book=Body()):
  for i in range(len(BOOKS)):
    if BOOKS[i].get('title').casefold()==updated_book.get('title').casefold():
      BOOKS[i]=updated_book
```

To start the server

uvicorn filename:app --reload

To open the swagger docs
127.0.0.1:8000/docs
