# shrt

A URL shortener, backed by [`squirrel`](squirrel)[^1].

[^1]: A toy persistent key-value store. Used in this project for fun. 

## API

**Add a URL to the service**
```
curl -X POST -d @testdata/add-url.json localhost:9000/api/shorten
```

**Retrieve a shortened URL and be redirected**
```
curl localhost:9000/api/url/$SHRT_HASH
```


[squirrel]: https://github.com/jdockerty/squirrel
