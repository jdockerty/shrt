# shrt

A URL shortener, backed by [`squirrel`][squirrel][^1].

[^1]: My toy persistent key-value store, used in this project for fun.

## API

**Add a URL to the service**
```
curl -X POST -d @testdata/add-url.json localhost:9000/api/shorten
{
    "id": "xxx",
    "url": "https://example.com",
}
```

**Retrieve a shortened URL and be redirected**
```
curl localhost:9000/api/url/$URL_ID
302 Found
```

**Delete a shortened URL**
```
curl -X DELETE localhost:9000/api/url/$URL_ID
204 No Content
```

[squirrel]: https://github.com/jdockerty/squirrel
