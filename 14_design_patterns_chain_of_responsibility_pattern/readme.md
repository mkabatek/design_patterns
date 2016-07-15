#Chain of Responsibility Pattern
 
As the name suggests, the [chain of responsibility pattern](http://www.tutorialspoint.com/design_pattern/chain_of_responsibility_pattern.htm) creates a chain of receiver objects for a request. This pattern decouples sender and receiver of a request based on type of request. This pattern comes under behavioral patterns.

In this pattern, normally each receiver contains reference to another receiver. If one object cannot handle the request then it passes the same to the next receiver and so on.