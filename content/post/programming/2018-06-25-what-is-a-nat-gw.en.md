---
title: "What Is a NAT Gateway"
date: 2018-06-25T08:27:38+01:00
draft: true
---

Looking into designing platform and new architectures can be quite intimidating, especially when it's your first time or you come from a software background.
Today I want to speak to you about the NAT Gateways, what is it? How it works? When to use it, etc... It's gonna be quite straight forward, _everyone_ use this component
but I would like to go even deeper and see what happens at the packet level.

## What is a NAT Gateway

So first things first, what is actually a nat gateway?? If we listen to papy wikipedia, he says:

> Network address translation (NAT) is a method of remapping one IP address space into another by modifying network address information in the IP header of packets while they are in transit across a traffic routing device.[1] The technique was originally used as a shortcut to avoid the need to readdress every host when a network was moved. It has become a popular and essential tool in conserving global address space in the face of IPv4 address exhaustion. One Internet-routable IP address of a NAT gateway can be used for an entire private network.

Ok Grandpa, you kinda spoiled everyone and explained everything I wanted to cover in this article. Anyway... So as Grandpa said, it's pretty common to see an infrastructure using NAT Gateways, especially these days with the Cloud. In the cloud, there's one rule. Keep everything private. Then the NAT appears.

Commonly when you start playing with the :cloud:, you'll create one instance, two, etc... but to access directly to these instances, you will setup those with an Ephemeral IP (aka Public IP), it's easier. Then your infra gets a bit more mature (and you as well) and you realise that using Public IPs might turn against you if you get a bit too permissive with firewall rules (or security groups). So you decide to move everything into a private subnet (only accessible inside your virtual private cloud) and use the protagonist of this article. THE NAT  GATEWAY :princess:

We are quite lucky, cloud providers sells specific instances or services to take care of this for us. _too handy_. But at the end, how is this actually working? Let's say you followed the instruction of your cloud providers to have a nat.

Then you have a platform like this:


_Insert drawing here_


As you can see in the diagram, every outbound connection goes through the NAT Gateway and goes back to the specific instance. My question is how? The instance has no public IP, so the server on the internet when he does receive a packet, sees only the NAT instance's IP. So how does a NAT gateway works?


## How a NAT gateway works?