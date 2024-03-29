# Special Ks! Intro to distributed applications with Akka.Net and Kafka
Notes from the .NET User Group talk https://www.meetup.com/de-DE/Geneva-NET-User-Group/events/266787969/

Follow-up of the Akka.NET talk some years ago.

The reason for Kafka - see how these systems interact.

Akka.NET is now in the .NET Foundation https://petabridge.com/blog/akkdotnet-dotnet-foundation/

You assume everything is remote, so you may as well just send messages.

Akka.Cluster is a higher level view than Akka.Remote

Seed nodes - the only thing special is that they know where the cluster is.

## Demos
You can instantiate actors as groups or pools.

He's showing us some hocon configuration for Akka.NET

 - Router


The only thing he had to change was the config to make it fully distributed.

Poor man's queue - add a persistent actor.

Persistence - inherit from ReceivePersistentActor. It then lets you implement a Recover action.

## Why Kafka
Persisted log, you can replay from offset.

The real example he had was SSIS sending messages.

Easiest way to try out Kafka-like stuff - use Azure EventHubs supporting the
Kafka protocol.

## Questions
Deployment - how do you do deployment when you have a new version?

Akka has a mechanism to remotely deploy actors. Or roll your own.

For serialization you have to do your own versioning.

Other option - plug in your own Serialization thing (by default it's just JSON.NET) to do some tolerant reader stuff.




