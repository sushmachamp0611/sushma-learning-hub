Queue: asynchronous communication , and **decouples** services 

Producer–Consumer Queue Flow
----------------------------

[Producer]
   |
   |  (sends messages)
   v
+-------------------+
|     Message Queue |
|  (Kafka / RabbitMQ) |
+-------------------+
   ^
   |  (reads messages)
   |
[Consumer]


