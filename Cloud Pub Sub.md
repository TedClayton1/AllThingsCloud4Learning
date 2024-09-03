
Google Cloud Pub/Sub, or publish-subscribe, is ==a messaging service that allows applications and services to send and receive messages asynchronously==. Pub/Sub works by separating producers and consumers, which removes the need for real-time synchronization. It can be used for a variety of purposes, including:

- Data integration: Loading and distributing data for streaming analytics and data integration pipelines
- Service integration: As a messaging-oriented middleware
- Task parallelization: As a queue



*What is Cloud Pub Sub*

Asynchronous messaging service means it helps you to send, receive and filter events or data streams. Gives you durable message storage, scalable in order message delivery, consistent high availability and performance at any scale. Pub Sub runs in any Google Cloud region in the world. Thus you can easily use it in Jakarta, Frankfort or Montreal and everywhere else. No need to provision Pub/Sub it scales global data delivery automatically from 0-millions of messages per second. With Pub/Sub data producers don't need to change anything when the consumers of their data change. Just publish once and let us manage distribution. This lets more of your services be entirely stateless. 

*How to set up Pub/Sub?*

You setup Pub/Sub between services or applications by defining topics and then subscriptions which allows services to receive the messages published on those topics. This means one-to-many communications gets much simpler. So you can spread batch image analysis over multiple workers. Or, you can send logs from your security system to archiving, processing, and analytic services. 

*Stream Data into Big Query and Dataflow?*

Or if you have a steady stream of data you can use Pub/Sub to stream the data into Big Query or Dataflow for intelligent processing. Pub Sub is really handy for notifications when something bad happens. You can page the right teams when the system or service goes down. 

*Wrap Up*

The next time you need a way to connect multiple services, applications, or data sources. Take a minute to try out Cloud Pub/Sub