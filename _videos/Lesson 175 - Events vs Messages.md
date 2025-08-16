---
title: Lesson 175 - Events vs Messages (en)
date: 2025-08-16T16:15:30.119+02:00
category: videos
tags: [event-driven architecture, events, messages, software architecture, messaging patterns, publish-subscribe, queues, system design]
excerpt: A detailed exploration of the differences between events and messages in event-driven architecture, outlining when to use each communication type for optimal system design.
---

![thumbnail](https://i.ytimg.com/vi/ziuzxxqjgtA/maxresdefault.jpg)
[https://youtu.be/ziuzxxqjgtA?si=6ueXhrgpQB1ilVhE](https://youtu.be/ziuzxxqjgtA?si=6ueXhrgpQB1ilVhE)

## My thoughts

The video clarifies that ownership in event-driven architectures varies: for events, the sender owns the channel and contract, while for messages, the receiver owns them. This distinction affects how components interact and control communication flows. Understanding this ownership difference helps decide when to use events versus messages for effective system design.

## TLDR;
- Event-driven architecture distinguishes between events and messages.
- Events represent something that has happened (past tense) and are usually broadcast via publish-subscribe channels.
- Messages represent commands or queries, typically sent point-to-point via queues.
- The ownership of event channels and contracts lies with the sender; for messages, with the receiver.
- Events are ideal for broadcasting state changes to multiple consumers.
- Messages are useful for controlling processing order and receiving asynchronous responses.
- In complex flows, messaging can orchestrate sequential steps while events handle broad notifications.



## Content

### Understanding Events and Messages in Event-Driven Architecture
In software architecture, particularly event-driven architecture, it's critical to understand the difference between events and messages to design efficient systems. Mark Richards discusses these concepts in detail in his Software Architecture Monday series, focusing on how and when to use each within an event-driven system.

### What is an Event?
Events represent something that has already happened. They are notifications of state changes, expressed in the past tense, such as "Order Placed." Events are essentially broadcast messages that communicate to any interested subscriber that a particular action or change has occurred.

> "An event is something that you're advertising that has already happened... it's a state change."

Events typically use a publish-subscribe messaging pattern through topics, streams, or notification services. The event sender owns the event channel and the contract defining the event's payload. This ownership means if you want to react to an event, you must conform to the sender’s contract.

### What is a Message?
Messages differ from events in that they usually represent commands or queries—requests to perform an action or reply with information. Examples include "Apply Payment" or "Get Payment Type." Messages follow a point-to-point pattern, often leveraging queues.

> "A message is more of a command or a query... I need you to do something for me or I need some information from you."

Unlike events, the receiver of a message owns the message channel and contract. To communicate with that receiver, the sender must conform to the receiver’s contract. Messages typically require a direct, sometimes acknowledgment-based communication pattern.

### Key Differences Between Events and Messages
1. **Nature of communication:** Events announce past actions; messages request actions.
2. **Messaging patterns:** Events use publish-subscribe; messages use point-to-point.
3. **Ownership:** Event channels and contracts are owned by senders; message channels and contracts are owned by receivers.
4. **Contract control:** Senders maintain event contracts; receivers maintain message contracts.

### When to Use Events vs. Messages
In typical event-driven architectures:
- Events are used to inform multiple subscribers of changes, for example, notifying payment, inventory, and notification services when an order is placed.
- Messages can be used to control processing order within complex flows where sequential steps are essential.

> "One area where we might want to use messaging is to control the processing order." 

For example, after placing an order, the system may send a message to payment to "Apply Payment." Upon confirmation, a message is sent to inventory to "Adjust Inventory," followed by sending a notification to the customer.

While events enable loose coupling and parallel processing, messages allow orchestration of sequential workflows and confirmation of actions through asynchronous acknowledgments.

### Combining Events and Messages
Although events dominate typical event-driven architectures due to their decoupling advantages, messages are valuable for scenarios requiring:
- Asynchronous confirmations.
- Controlled sequencing of operations.

It's also possible to subscribe to events instead of waiting for message acknowledgments, illustrating flexibility in implementation.

### Conclusion
Distinguishing events and messages enhances designing event-driven systems, enabling better decisions about communication patterns and system orchestration.

> "Typically most of the time we use events with publish and subscribe, but messaging helps control workflows in more complex scenarios."

This deeper understanding aids architects in building scalable and maintainable systems leveraging the right communication type for the right purpose.

This lesson was part of Software Architecture Monday series, lesson 175, focusing on events versus messages.




> From: [https://github.com/Nikoms/n8n/tree/main/ongoing/382](https://github.com/Nikoms/n8n/tree/main/ongoing/382)