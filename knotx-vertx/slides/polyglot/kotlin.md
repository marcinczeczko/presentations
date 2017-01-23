## You can develop in Kotlin

```kotlin
import io.vertx.core.Vertx
import io.vertx.kotlin.lang.*

fun server(vertx: Vertx) {
    vertx.httpServer { request ->
        contentType("text/html", "utf-8")
        replyText("<html><body><h1>Hello from vert.x!</h1></body></html>")
    }
}
```

