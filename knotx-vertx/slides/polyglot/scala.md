## You can develop in Scala

```scala
vertx.createHttpServer.requestHandler { req: HttpServerRequest =>
  req.response.end("This is a Verticle script")
}.listen(8080)
```

