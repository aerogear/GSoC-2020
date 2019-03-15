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

## Good GraphQL Tutorials

* This tutorial is a good introduction to GraphQL - https://medium.freecodecamp.org/graphql-zero-to-production-a7c4f786a57b
* This tutorial is a nice introduction to subscriptions - https://blog.apollographql.com/tutorial-graphql-subscriptions-server-side-e51c32dc2951

## Build a Deeper Understanding of GraphQL Subscriptions in Apollo

Apollo Server has their own approach to subscriptions. One of the concepts they use is `AsyncIterators.` You should research how subscriptions work in Apollo. A great starting point for this research is this repo: https://github.com/apollographql/graphql-subscriptions

It contains an implementation of subscriptions using an event emitter. The Readme has hints on how you might implement your own subscriptions module and it also links to other existing subscription implementations (such as redis, postgres, MQTT, etc). You should follow those links and see how other people have implemented subscription libraries. How did they do it? What could you learn here that would help you use Red Hat AMQ for subscriptions?

## Red Hat AMQ Investigations

Even though most of the AeroGear team members are Red Hat employees, we only have a small amount of knowledge and experience around Red Hat AMQ. We are much more knowledgeable in the areas of GraphQL, mobile development, Node.js, and OpenShift. Your mentor and the wider AeroGear team will do their best to guide you, but it will also be your responsibility to research the Red Hat AMQ technology, build an understanding of it, and bring the relevant knowledge back to the AeroGear team.

Once you have followed some tutorials on GraphQL and gotten familiar with `voyager-server`, you should upskill with Red Hat AMQ.

## Get Red Hat AMQ Running

You should try to figure out how to start the Red Hat AMQ broker on your local machine, either Apache Artemis or using the Red Hat AMQ product. Take a look at the various Red Hat AMQ docs.

* Red Hat AMQ broker getting started docs: https://access.redhat.com/documentation/en-us/red_hat_amq/7.2/html/using_amq_broker/
* Publish Subscribe messaging: https://access.redhat.com/documentation/en-us/red_hat_amq/7.2/html/using_amq_broker/addresses#configuring_publish_subscribe_messaging

Ideally you should figure out how to run Red Hat AMQ using Docker.

## Red Hat AMQ and Node.js

Investigate the various protocols that Red Hat AMQ supports and the different Node.js libraries that could be used. Hint: the [`rhea` module](https://github.com/amqp/rhea) is a good place to start. This is the official Red Hat Node.js client for Red Hat AMQ and it uses the AMQP protocol.

The `rhea` module has some basic [example applications](https://github.com/amqp/rhea#examples) you should attempt to get running on your machine. The ones you should be particularly interested in are `simple_send.js` and `simple_receive.js.` Attempt to get these running and verify that they can send and receive messages. Try running multiple instances of the apps, for example. 1 sender application and 3 receiver applications. Do they all receive the message? Try to modify the code or create your own application that uses this library.

Bonus: Try investigate alternative Node modules and protocols. `rhea` uses the AMQP messaging protocol, however Red Hat AMQ supports other protocols such as JMS, MQTT, and more. Do some research to find if there are any other Node modules out there that could be used with Red Hat AMQ. For example, are there other modules that are much easier to use? Are there other modules that are better maintained/more active/have a larger community? Can you use them to talk to Red Hat AMQ?

## Next Steps

If you have managed to get a decent grasp of GraphQL, GraphQL subscriptions, and you have done some upskilling in Red Hat AMQ, you should have some basic idea on how to answer the following questions.

* What are GraphQL subscriptions?
* What is publish-subscribe messaging?
* What is an AsyncIterator?
* How might I implement GraphQL subscriptions backed by Red Hat AMQ
* What tools/libraries could I use together to make this as simple as possible?
* How could I test my implementation to ensure it works properly?

You don't need to have complete, detailed answers to these questions, but you should start to get some idea of what is needed. Or perhaps you won't know the answers, but you will begin to understand how to break these questions down so you can find the answers.