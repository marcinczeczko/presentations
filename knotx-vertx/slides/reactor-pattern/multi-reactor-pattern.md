
![](resources/multi-reactor-pattern.jpg)

note:
  - Sometimes, you have really lots of events. What's then ?
  - In node.js you tried to fork the process to utilize all the cores.
  - When Vert.x starts, it first checks how many cores the machine have, and spawns as many event-loops as CPU has cores.
  - E.g. If I run some Node.js app, on my laptop, it will use only one core, but in Vert.x all cores will be utilized.
  - In Vert.x it's called Multi-reactor pattern
