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


