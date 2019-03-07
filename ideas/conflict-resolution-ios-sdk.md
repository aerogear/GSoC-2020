# Conflict Resolution for AeroGear Sync iOS SDK

## Summary of idea:

A port of the current JS SDK to iOS. Although porting work seems straightforward, conflict resolution, offline support etc. 
makes this work more complex.

There is an equivalent project idea for Android [here](./conflict-resolution-android-sdk.md)

Our Voyager framework is built on top of Apollo GraphQL implementation.
Our iOS SDK for AeroGear Mobile Services has limited support for Voyager framework at the moment.
One of the big missing things is conflict resolution. Conflict resolution is implemented in the JS SDK 
and this project idea is about porting the JS code to iOS using Swift.

## Technologies

iOS, GraphQL, OpenShift, Docker

## GitHub repos

* https://github.com/aerogear/voyager-server
* https://github.com/aerogear/aerogear-js-sdk
* https://github.com/aerogear/aerogear-ios-sdk

## Skill level

Intermediate, Advanced

## Contact(s) / potential mentors(s): 

Ali Ok (@aliok_tr at Twitter, aliok on IRC)

See [parent page](../README.md) for more information

## How to get ready

* Get familiar with GraphQL by completing the tutorial: https://www.graphql.com/tutorials/
* Get familiar with Apollo: https://www.apollographql.com/
* Get familiar with Voyager: https://github.com/aerogear/voyager-server
* Check out the Javascript SDK for AeroGear Mobile Services: https://github.com/aerogear/aerogear-js-sdk
* Learn more about the iOS SDK for AeroGear Mobile Services: https://github.com/aerogear/aerogear-ios-sdk
* Try out the showcase application: https://github.com/aerogear/ionic-showcase/  