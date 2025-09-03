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

Q3 : why java not have jre after java 8 onwards?
https://stackoverflow.com/questions/63241080/i-am-not-able-to-find-jre-files-in-program-files

 - modular jar file. 
 - In module-info.Java, we can mention all the dependencies/which modules are needed at the run time. [requires module3;
 -  Now at the compile time with the help of module-info.Java, compiler will get to know that what are classes needed to run the application and at the compilation time only compiler will check that the corresponding classes/packages are present inside the module or not. If the required classes are present then the code will compile successfully otherwise it will throw compilation errors at the compile time only.
 -  We can resolve this issue with JPMS. Jigsaw breaks up the JDK itself into many modules e.g. Java.sql contains the familiar SQL classes, Java.io contains the familiar IO classes etc. As per requirement, we can use appropriate module. No need to use the entire JDK.
 -  Version conflicts: [requires module3;]
Security Problems: Assume we have a JAR and inside that jar we have 2 packages.
 exports com.geeksforgeeks.demo.impl;

Q4 : jvm /jre /jdk ?
Q5 : Difference between ClassNotFoundException vs NoClassDefFoundError in Java ?
     missing jar error . 
https://javarevisited.blogspot.com/2011/07/classnotfoundexception-vs.html#google_vignette
List 
https://javagoal.com/copyonwritearraylist-in-java/

https://soshace.com/2020/09/11/spring-cloud-config-refresh-strategies/

In the case of using Spring Cloud Config Server; Spring Cloud offers the following methods to refresh the properties in config clients.
By calling the /actuator/refresh endpoint exposed on the config client via the Spring Actuator.
By calling the /actuator/bus-refresh endpoint exposed on the config client integrated with Spring Cloud Bus.
By calling the /monitor endpoint exposed on the config server integrated with Spring Cloud Bus.


