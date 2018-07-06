---
title: RabbitMQ At your Service
comments: true  
---  
  
**RabbitMQ** is a message broker that implements **A**dvanced **M**essage **Q**ueuing **P**rotocol(**AMQP**). It is a binary application layer protocol, designed to efficiently support a wide variety of messaging applications and communication patterns. It assists in the development of distributed, fault-tolerant and asynchronous applications.

  
Let’s Have a look at how RabbitMQ works and what kind of components it contains!


  

##Here’s how it works:  

**Producers** send/publish the messages to the broker -> **Consumers** receive the messages from the broker. RabbitMQ acts a communication middleware between both **producers** and **consumers** even if they run on different machines.

 
 While the producer is sending a message to the queue, it will not be sent directly, but sent using the exchange instead. The design below demonstrates how are the main three components are connected to each other.

 
 The **exchanges** agents that are responsible routing the messages to different queues. So that the message can be received from the **producer** to the exchange and then again forwarded to the **queue**. This is known as the ‘Publishing’ method.
 
![image1](img/rabbit1.png)


  
Afterwards, the message will be picked up and consumed from the queue; this is called ‘Consuming’. In this way, if in any case we have one queue the exchange won’t make much difference.
  
  
  
  ![image2](img/rabbit2.png)

 By having a more complex application we would have multiple queues. So the messages will send it in the multiple queues.
  
  
  
  
  ![image3](img/rabbit3.png)

  
  
  
Sending messages to multiple queues exchange is connected to the queues by the binding and the routing key. A **Binding** is a “link” that you set up to connect a queue to an exchange. The **Routing key** is a message attribute. The exchange might look at this key when deciding how to route the message to queues (depending on exchange type).
  
  
  **1.** The producer publishes a message to the exchange and identifies the routing key.
  
  **2.** The exchange receives the message and is now responsible for the routing of the message.
  
  **3.** A binding has to be set up between the queue and the exchange. In this case, we have bindings to three different queues from the exchange. The exchange routes the message into the queues.
  
  **4.** The messages stay in the queue until they are handled by a consumer.
  
  **5.** The consumer handles the message.
  
  
  
  ##Type of exchange:
 
  | EXCHANGE TYPE | BEHAVIOUR |
  | --- | --- |
  | Direct | The binding key must match the routing key exactly - no wildcard support.
 |
  | Topic | Same as Direct, but wildcards are allowed in the binding key. '#' matches zero or more dot-delimited words and '*' matches exactly one such word. |
  | Fanout | The routing and binding keys are ignored - all published messages go to all bound queues. |
 

 ##Let’s Sum up the core concept!

 * **Producers** emits the messages to **exchange**.
 * **Consumers** receive messages from the **queues**.
 * **Binding** connects an exchange with a queue using a **binding key**.
 * Exchange compares **routing key** with binding key.
 * Messages distribution depends on **exchange type**.
 * Exchange type: **fanout, direct, topic** and **header**.
 
 
 ##Why RabbitMQ ?

* You might need messaging if … you need to scale.
* You might need messaging if … you need to monitor data feeds.
* You might need messaging if … you need a message delivered responsibly.
* You might need messaging if … you need things done in order.
* You might need messaging if … you are using the cloud.


“STOP — LOOK — LISTEN — THINK”- _RabbitMQ_
