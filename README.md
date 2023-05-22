# apollo-server-example

## Run
```
$ node index.js
```

## Request Sample
```
$ curl -X POST -H "Content-Type: application/json" -d '{ "query": "{ allBooks{title} }" }' http://localhost:4000/
{"data":{"allBooks":[{"title":"Webを支える〜"},{"title":"失敗から学ぶ〜"},{"title":"Vue.js入門"}]}}
```

```
$ curl -X POST -H "Content-Type: application/json" -d '{ "query": "query ($isbn: String!) { getBook(isbn: $isbn) { title author } }", "variables": { "isbn": "978-4-297-10408-5" } }' http://localhost:4000/
{"data":{"getBook":{"title":"失敗から学ぶ〜","author":"曽根 壮大"}}}
```

## Reference
- Software Design 2021年/8月号 p78,79
- https://zenn.dev/saboyutaka/articles/07f1351a6b0049
