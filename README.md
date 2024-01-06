## Introduction
Spring Cloud Stream messaging to asynchronously communicate messages between Spring Boot services.  
Kafka as our message bus to transport messages between our services.

### Project Details:
1.  A Spring Cloud Config server that is deployed as Docker container and can manage a services configuration information using a file system or GitHub-based repository.
2.  A Eureka server running as a Spring-Cloud based service.  This service will allow multiple service instances to register with it.  Clients that need to call a service will use Eureka to lookup the physical location of the target service.
3.  A Zuul API Gateway.  All of our microservices can be routed through the gateway and have pre, response and
post policies enforced on the calls.
4.  A organization service that will manage organization data used within EagleEye.
5.  A new version of the organization service.  This service is used to demonstrate how to use the Zuul API gateway to route to different versions of a service.
6.  A special routes services that the the API gateway will call to determine whether or not it should route a user's service call to a different service then the one they were originally calling.  This service is used in conjunction with the orgservice-new service to determine whether a call to the organization service gets routed to an old version of the organization service vs. a new version of the service.
7.  A licensing service that will manage licensing data used within EagleEye.
8.  A Postgres SQL database used to hold the data for these two services.
9.  A Kafka message bus to transport messages between services.
10. A Redis service to act as a distributed cache.

### Software needed
1.	Apache Maven (http://maven.apache.org)
2.	Docker (http://docker.com)
3.	Git Client (http://git-scm.com)

### Building Docker Image

Run the following maven command.  

   **mvn clean package docker:build**

### Running services 

   **docker-compose -f docker/common/docker-compose.yml up**


### Related Topics

- Asynchronous messages to communicate between applications
- Event Driven Architecture (EDA)
- Message Driven Architecture (MDA)
- Messaging based solutions
- Spring Cloud Stream
- Emit an asynchronous event (message)

- Redis
  - A distributed KEY-VALUE Store database
- Invalidate cache

- Loose Coupling
- Durability
- Scalability
- Flexibility

- A synchronous HTTP response creates a hard dependency between services

- Message handling semantics
- Message visibility
- Message choreography
- Annotation-driven framework

- Message broker
- Message Queue
- Service Client
- Source
- Sink
- Channel
- Binder

- Bind the application to a message broker
- Bind to a message broker
- Distributed Caching
- Use Redis as Distributed Cache
- Increase Resiliency

- Using Messaging/Asyncronous Communication allows your APP. to scale and become more Fault Tolerant
- Abstracting away platform-specific details of the underlying message platform
- Use Kafka as our message bus to transport messages between our services.
