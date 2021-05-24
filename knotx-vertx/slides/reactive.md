## Reactive

![Reactive Manifesto](http://www.reactivemanifesto.org/images/reactive-traits.svg)

note:
- Message-driven - asynchronous message passing, to establish boundries between components. all communication in vertx is some form of message like event bus
- Elasticity - you need to scale out and scale back based on load/demand to maintain responsivness and sls
- Responsivess - we will respond in a time frame that is expected by our customers/users
- Resilient - if the things fail, the whole system will not colapse upon itself

