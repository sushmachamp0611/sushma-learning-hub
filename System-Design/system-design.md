1. Core Concepts
Scalability: Ability of a system to handle growth (vertical vs. horizontal scaling).

Reliability: Ensuring system works correctly even under failures (redundancy, replication).

Availability: Percentage of time system is operational (HA setups, failover).

Maintainability: Ease of updates, debugging, monitoring.

2. Key Components
Load Balancer: Distributes traffic across servers.

Caching: Speeds up responses (client-side, CDN, server-side).

Database: SQL vs NoSQL, sharding, replication.

Message Queues: Asynchronous communication (Kafka, RabbitMQ).

API Gateway: Entry point for services, handles routing, auth, throttling.

3. Design Principles
CAP Theorem: Consistency, Availability, Partition Tolerance (choose 2).

Microservices: Independent deployable services.

Event-Driven Architecture: Systems reacting to events asynchronously.

Consistency Models: Strong vs eventual consistency.

4. Common Patterns
Rate Limiting: Control request flow.

Database Indexing: Faster queries.

Sharding: Splitting data across servers.

Replication: Copying data for fault tolerance.

Caching Strategies: Write-through, write-back, write-around.

5. Example Designs
URL Shortener (Bitly): Hashing, database, cache.

Chat App (WhatsApp): Real-time messaging, delivery guarantees, scaling.

Video Platform (YouTube): Storage, CDN, recommendation system.
