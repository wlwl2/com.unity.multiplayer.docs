---
id: online-stack
title: OnlineStack
---

Netcode for GameObjects (later on Netcode) allows you to connect to a host by its IP and port. However, if the host is not on the same network as you (i.e. somewhere over the Internet), you will need some extra services to achieve a successful connection and thus a successful game.
There are two ways of achieving such a connection : 
- NAT punching: an advanced technic that allows you to directly connect to the host computer even if it is on another network. Many factors impact how you will connect to the remote host, and it can be tricky to implement. 
- Usage of a Relay server: the relay is on the Internet with a public-facing IP that you and the host can reach. After the connection to the relay, it will relay all the messages sent to it to all the other party members connected.

Netcode does not offer tools to help you do a successful punch through a NAT. But, Unity Services provide a Relay Service that can relay all Unity Transport based technology, like Netcode.
