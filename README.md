# AddToSkills
1. multiple version of a application
2. api gateway features
   - load balancing
   - rate limit
   - manipulate request headers : authorization
   - monitoring

spring cloud gateway routes 
   - id ,predicates,filters,url

Resilience 4j 
- https://medium.com/bliblidotcom-techblog/resilience4j-circuit-breaker-implementation-on-spring-boot-9f8d195a49e0
- It provides various resilience mechanisms, including Circuit Breaker, Rate Limiter, Retry, and more.
What is Circuit Breaker?
The concept of a circuit breaker is to prevent calls to microservice when it’s known the call may fail or time out.
This is done so that clients don’t waste their valuable resources handling requests that are likely to fail.
 Using this concept, you can give the server some spare time to recover.

So, how do we know if a request is likely to fail? Yeah, this can be known by recording the results of several previous requests
sent to other microservices. For example, 4 out of 5 requests sent failed or timeout,
then most likely the next request will also encounter the same thing.

