
![](resources/reactor-pattern.jpg)

note:
- The whole concept of Vert.x is the Reactor Pattern.

Basicaly, we have:
- One single event-loop (you can see it as single thread)
- Because we have single thread, we cannot never block, otherwise whole application will stop
- To overcome this situation, we have handlers
  - Handler is the way for the blocking model
  - Typical code, extects the result from the function, function need to return it using return statement, so it blocks the thread until the return statement
  - In our case, we have to have objects that we call handler, and when we want to return value from our function, we call it to handle the result from our function
  - The handler can't block, because otherwise we will not handle any more events comming in.
