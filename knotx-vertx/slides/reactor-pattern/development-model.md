## Asynchronous Development Model

```java
void operation(int param1, int param2, Handler<Integer> handler) {
  int result = param1+param2;
  handler.handle(result);
}
```

And in the Handler object

```java
void handle(Integer value) { 
  //Do something with value
}
```

note:
- we don't use return, as it means when we have it the caller is blocked until the return statement will be called.
- handlers handle the event, and it can be:
  - a message
  - a notification
  - a http request
  - a commond
  - a file
  - a result, an error
- My method computes the result, and when it's done, it calls my handler
- It can still do stuff after calling handler !!

Handler is functional interface
- you need to implement it, and you can use lambda expression in java 8


Look at the bigger code:
- Starting server
- two handlers
  - request handler - will be called on each incomming request (event is request)
  - start server handler (it takes time, and it could fail e.g. port is already used)
    - this handler is asyncResult (vertx structure that it tells you if it failed or succedd and give access to the result)
    - we don't have try/catch here
     - exception will be in the event loop, we can't block it, so we must not kill it neither
     - we don't throw exceptions, we create Future saying failed and with the cause
    - it looks different from regular model, but with java 8 lambdas it easy to understand

Async does not mean thread
- How many threads I need to run this code ?
example with add() and doSomething()
- add(1,1, i-> {}) will be called by my thread
- handler.handle() will be called in the same thread
- and i->{] also in the same thread
