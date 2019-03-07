# A Node.js library to support GraphQL Subscriptions Powered by Red Hat AMQ
 
## Summary of idea:

The goal of this project is to create a Node.js library that can be used to implement GraphQL subscriptions using Red Hat AMQ 
as the underlying Pub Sub technology. (Upstream project is Apache ActiveMQ Artemis 2.0.0)

There is a huge amount of scope here for the student to learn about GraphQL, Microservices, Asynchronous Messaging, 
Event Driven Architectures and Red Hat technologies. Because the deliverable (A Node.js library) would 
be quite small, The student is also encouraged to write tests, fully featured documentation, and to take ownership of 
the publishing/release lifecycle (on npm).

As a stretch goal, the student could also build an example application e.g. a real time messaging application that uses their new node.js library and the apollo-voyager-server framework as a proof of concept.

In GraphQL, subscriptions is a concept that allows clients to subscribe to events happening on the server. The basic idea is that an event happens on the server and the server has some way to notify any clients that are interested in that event. For example, in a group chat application, all of the clients could subscribe to a new message event. The most common implementation of subscriptions uses websockets between the server and client. This allows the server to send back events to the clients in real time.

In a production environment, there will be several  instances of the backend application running at the same time. The backend servers need a Publish/Subscribe (Pub Sub) mechanism to share events back and forth between each other.

![](https://lh5.googleusercontent.com/wIiGDVvMI5eICoIXFMJOKU1h3g7f7KAyTk0JK7D2kn7M9ezXSPVzxHjwwr-0NoqVkENmSP6v75ROUDKL8fmfCeCG7N9svf1S6yAPqbX7Hb72HGsRxg3Le3bvnQpuYgb0WhmFnKqK)
 

Publish/Subscribe is a is a form of asynchronous service-to-service communication used in serverless and microservices architectures. In a pub/sub model, any message published to a topic is immediately received by all of the subscribers to the topic.

For example, Using Pub Sub, Server 2 can know about an event that happened on server 1 and server 2 can notify its connected clients about the event.

There are many technologies that can be used for Pub Sub. (Examples: RabbitMQ, Apache Kafka, MQTT) and there are many Node.js libraries that allow us to use Pub Sub technologies in GraphQL applications. They would be a great starting point for trying to implement a new one. https://github.com/apollographql/graphql-subscriptions#pubsub-implementations

Red Hat has a messaging product called Red Hat AMQ which can be used to implement a production ready Publish/Subscribe architecture. The goal of this project is to create a node.js library that can be used to implement GraphQL subscriptions using Red Hat AMQ as the underlying Pub Sub technology.

## Technologies

GraphQL, Node, AMQ, ActiveMQ

## GitHub repos: 

https://github.com/aerogear/voyager-server

## Skill level

Beginner, Intermediate

## Contact(s) / potential mentors(s)

Dara Hayes (@darahayess at Twitter, darahayes on IRC)

See [parent page](../README.md) for more information

## How to get ready

* Get familiar with GraphQL by completing the tutorial: https://www.graphql.com/tutorials/
* Get familiar with Apollo: https://www.apollographql.com/
* Get familiar with Voyager: https://github.com/aerogear/voyager-server
* Get familiar with Apache ActiveMQ Artemis: https://activemq.apache.org/artemis/
* Try creating your own application which uses Voyager framework, similar to https://github.com/aerogear/ionic-showcase/tree/master/server
* Experiment with subscriptions with GraphQL (using Apollo)
* Try creating an application which uses ActiveMQ  