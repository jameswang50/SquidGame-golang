# SQUID GAMES

Distributed system using Kubernetes, gRPC, PubSub, Kafka, RabbitMQ, Golang, NoSQL DB, Sockets io, etc.

---

## General information
- Course: Operating Systems 1
- Second Semester 2021
- Languages: Golang, Javascript.
- Group 18

&nbsp;
---


## Description

It is requested to build a generic system of distributed architecture that shows statistics in real time using Kubernetes and service mesh such as Linkerd and other Cloud Native technologies. In the last part, a service mesh will be used to divide the traffic. Additionally, Chaos Mesh will be added to implement Chaos Engineering. This project will be applied to the visualization of the results of games implemented by the students.


## Explanation

Ingress receives the traffic and is redirected to an API that writes to a queue. Before that, receive the number of players and randomly choose a game from
algorithm, to choose the winner of the current game, then write the necessary data to the queue. The Go Queue Worker will read this data first, then
will be written to the databases, Redis for the real-time data in the dashboards and MongoDB for the transaction logs.

