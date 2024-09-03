Architecture enables large teams to build scalable applications that composed of many loosely coupled services.

Each microservice have their own database.

Each microservice can expose the REST APIs

Each microservice is loosely coupled.

Each microservice should be developed independently

Deployed independently

scaled independently

distributive tracing - logs

In the microservice architecture, the application is divided into a number of microservices, each hosted on a separate node, like so: Each microservice is responsible for a single functionality. The microservices are loosely coupled and can be developed and managed separately. 

They communicate with each other using APIs. Thanks to that, each microservice can even be developed in a different programming language. When you need to upgrade your application, you can upgrade a single node without affecting other components. By splitting the application into microservices, you also have control when you scale your application. 

You can granularly scale the services that require scaling without touching the others. Finally, microservices allow you to embrace CI/CD and deliver functionalities faster as deployments can be rolled out in a very controlled way.

![[Pasted image 20240709150520.png]]