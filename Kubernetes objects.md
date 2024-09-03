
Kubernetes objects are records of intent that are defined in YAML format. They are declarative in nature. Once created, Kubernetes will take care of keeping them in the state declared in the definition file. Some examples of the most important objects are as follows:

**Pods**
**Replica sets**
**Replication controllers**
**Deployments**
**Name spaces**

It would take hundreds of pages to describe all the available Kubernetes objects, so for the purpose of the exam, we will concentrate on the preceding ones. Let's take a look at an example of a deployment object file. This deployment would basically deploy two Pods with containers using the nginx  image:

apiVersion: apps/v1
kind: Deployment
metadata:
	name: nginx-deployment
	 labels: 
		 app: nginx
	spec: 
	replicas: 3 
	selector: 
		matchLabels:
			 app: nginx 
	 template: 
		 metadata: 
			 labels:
		app: nginx
 spec: 
	 containers:
	  - name: nginx 
	   image: nginx:1.7.9 
	   ports:
	   - containerPort: 80




No matter what kind of object we define, we need to have the following data in it:

*apiVersion*: The version of the Kubernetes API we want to use
*kind*: The kind of object to be created
*metadata*: Data that helps uniquely identify the object, such as its name 
*spec*: The specification of the object, which is dependent on its type

To create or update an existing object, we can use the following command:

**kubectl apply -f definition.yaml**

Here, definition.yaml is the file with an object definition. To run our first deployment, we would save the preceding definition in the definition.yaml file and run the kubectl command.

There are multiple commands you can use to manage Kubernetes. kubectl is the most used as it allows us to create, delete, and update Kubernetes objects. Take a look at the following link to see what operations can be performed using kubectl: [Command line tool (kubectl) | Kubernetes](https://kubernetes.io/docs/reference/kubectl/). Note that kubectl is installed in the GCP Cloud Shell console by default, but if you want to use it from any other machine, it needs to be installed. Now, let's have a look at each object, starting with Pods. 

**Selectors and labels**

You will notice that Kubernetes objects have parameters called **labels** and **selectors** .Those parameters are used to associate different objects with each other. Say you want to associate a Pod with a namespace. In the Pod definition, you would use a property label such as app: myapp and in the namespace you would use a selector such as app: myapp.