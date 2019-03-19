# Kubernetes Operators for Unified Push Server and AeroGear Digger
 
## Summary of idea:

The goal of this project is to create Kubernetes Operators that can install, update, configure and manage 
Unified Push Servers and AeroGear Digger, using the Operator-SDK.

## Technologies

Golang, Operator Framework, Kubernetes

## GitHub repos

* https://github.com/aerogear/aerogear-digger
* https://github.com/aerogear/aerogear-unifiedpush-server
* https://github.com/operator-framework


## Skill level 

Beginner, Intermediate

## Contact(s) / potential mentors(s)

Wei Li (weil@redhat.com)

See [parent page](../README.md) for more information


## How to get ready

* Get familiar with OpenShift
* Get familiar with Unified Push Server: https://github.com/aerogear/aerogear-unifiedpush-server
* Try running the UPS server locally and send a notification to your own application on your own physical device: https://github.com/aerogear/aerogear-android-cookbook/tree/master/HelloPush
* Get familiar with AeroGear Digger: https://github.com/aerogear/aerogear-digger
* Try running AeroGear Digger on your own OpenShift cluster
* Get familiar with Operator Framework: https://github.com/operator-framework

## Next step

* Create a simple operator. Example: an operator that can managed the number of pods of a service.
