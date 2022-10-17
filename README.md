# Microservices_Concepts

---
##Microservice
   - Well focused, service grained services that exposes light weight protocal such as HTTP.
   - Fine grained refers to service granularity services.

###Service granularity
- The size of the service that it exposes the business functionality.

###Advantages:
 - Independent development and deployment by different teams.
 - Better fault tolerant.
 - Different technologies.
 - Horizontal scaling.
 - Orchestration of microservices.

---
### Clean and hexagonal architecture
- It is also known as Ports and Adapters.
- It basically relies on well-defined interfaces(Ports).
- Clean architecture depends dependency inversion.
  - Dependency inversion : High level modules should not depend on low level modules.
    - They are linked to each other through abstractions.
- DDD (Domain Driven Design) :
  - Each Microservice implements with DDD that provides bounded context, Entities, VO, Domain services and application services.
  - Strategic DDD:
    - Mapping business model and bounded context to domain model.
  - Tactical DDD:
    - Implement domain model with Value Objects, Aggregates, Entities, Services and Events.
- Kafka :
  - It is a event bus.
  - Event store for event driven services.
  - Resilient as it holds the data in persistent disk store.
  - Scalable 
  - Kafka consists of Producers, topics and Consumers.
    - Topics 
      - Topic will have internal partions.
  - Can be used in SAGA, OutBox and CQRS.

####SAGA:
 - The idea of SAGE is to create a local ACID transaction in long running transactions.
 - It keeps data in consistent manner.
 - Communicates events through event bus.
##### Types:
 - Choreography
 - Orchestrator 

####Outbox
 - Help to use local transactions to be consistent.

####CQRS
 - Isolate read and write operations separately.
 - For example, 
   - You can use relational databases to store data.
   - You can send data asynchronously to elastic search.
   - You can query elastic search for read operations more effectively.
   - You can scale write and read systems.
   - It will end up with eventual consistency.
####Kubernates and Docker.
   - Orchestration that automates your deployments, scaling and management of cloud native applications.
    

