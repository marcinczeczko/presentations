## Distributed

# Demo <!-- .element: class="fragment fade-in" style="color: red;" -->

note:
- out-of-box clustering support
- pluggable clustering manager, default is hazelcast based (in-memory gird)
- high availability mode
  - automatic failover support
  - when a module fails in one node, it will automatically start on another node on the cluster
- each Vertx application can discover each other when running on cluster
- you don't need to do anything except specifing deploy with cluster mode 
