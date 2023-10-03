### Used Stack
- ExpressJS
- Express-GraphQL
- GraphQL

### Setting up this application
```console
$ git clone https://github.com/MdZillurRahman/graphQL-Basic.git

$ cd graphQL-Basic

$ npm i

$ npm run devStart

```


### What application can do
- Fetch book list according to author using query and vice-versa
- Add new book to book list
- Add new author to author list


### Some examples
- Fetch the book list with the author
```console
query{
	books{
		id
    name
    authorId
    author {
      name
    }
  }
}
```
- Fetch the book list for the author
```console
query{
	authors {
	  id
    name
    books {
      name
    }
	}
}
```
- Add new book to book list
```console
mutation {
  addBook(name:"Journey By Foot", authorId:4) {
    id
  }
}
```