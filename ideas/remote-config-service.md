# AeroGear Remote Configuration Service
 
## Summary of idea:

For many client apps, developers sometimes want to change the behaviour or appearance of the apps using 
configurations. However, they do not want to release new apps every time when they 
need to update the configuration. The AeroGear Remote Configuration service will allow developers to update 
the configurations for their client apps remotely, without the need to release a new app.

The main components of this service including:

* A backend server that can manage configurations, probably built based on the AeroGear Voyager GraphQL server
* A UI that will developers to define configurations for their apps, and setup rules about what client/device can get what configurations
* A client side SDK that can manage fetching the configuration, caching and notify developers about configuration changes. Initial 
  target is to have a JavaScript SDK, built based on the AeroGear Voyager client modules.
 

## Technologies

Nodejs, GraphQL, AeroGear Voyager, React

## GitHub repos

https://github.com/aerogear/voyager-server

## Skill level

Beginner, Intermediate

## Contact(s) / potential mentors(s)

Wei Li (weil@redhat.com)

See [parent page](../README.md) for more information


## How to get ready

* Get familiar with GraphQL by completing the tutorial: https://www.graphql.com/tutorials/
* Get familiar with Apollo: https://www.apollographql.com/
* Get familiar with Voyager: https://github.com/aerogear/voyager-server
* Try creating your own application which uses Voyager framework, similar to https://github.com/aerogear/ionic-showcase/tree/master/server  