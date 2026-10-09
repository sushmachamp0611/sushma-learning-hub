**Why System Design is Crucial Today**
**Massive Scale**  
Companies like Google, Amazon, and Netflix serve billions of requests daily. Designing systems that scale horizontally (adding more servers) is essential.

**High Availability & Reliability** 
Users expect services to be available 24/7. System design ensures redundancy, failover mechanisms, and disaster recovery.

**Performance & Latency** 
A few milliseconds can make or break user experience. Good design uses caching, load balancing, and optimized data storage.

**Complex Architectures** 
With microservices, distributed databases, and event-driven systems, design decisions directly affect maintainability and cost.

**Cost Efficiency** 
Cloud infrastructure is expensive if poorly designed. Efficient system design reduces unnecessary compute, storage, and bandwidth usage.

**Security & Compliance** 
Systems must be designed with authentication, authorization, encryption, and compliance (GDPR, HIPAA, etc.) in mind.

----------------------------------------------------------------------------------------------------------------------------------------------------
1. **Core Concepts**
Scalability: Ability of a system to handle growth (vertical vs. horizontal scaling).

Reliability: Ensuring system works correctly even under failures (redundancy, replication).

Availability: Percentage of time system is operational (HA setups, failover).

Maintainability: Ease of updates, debugging, monitoring.

2.** Key Components**

Load Balancer: Distributes traffic across servers.

Caching: Speeds up responses (client-side, CDN, server-side).

Database: SQL vs NoSQL, sharding, replication.

Message Queues: Asynchronous communication (Kafka, RabbitMQ).

API Gateway: Entry point for services, handles routing, auth, throttling.

3. **Design Principles**

CAP Theorem: Consistency, Availability, Partition Tolerance (choose 2).

Microservices: Independent deployable services.

Event-Driven Architecture: Systems reacting to events asynchronously.

Consistency Models: Strong vs eventual consistency.

4. **Common Patterns**

Rate Limiting: Control request flow.

Database Indexing: Faster queries.

Sharding: Splitting data across servers.

Replication: Copying data for fault tolerance.

Caching Strategies: Write-through, write-back, write-around.

