## You can develop in Python

```python
server = vertx.create_http_server()

@server.request_handler
def handle(req):
    req.response
       .end("<html><body><h1>Hello from vert.x!</h1></body></html>")
    
server.listen(8080)
```
