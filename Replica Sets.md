
A replica set object is used to manage the number of Pods that are running at a given time.A replica set monitors how many Pods are running and deploys new ones to reach thedesired number of replicas. To define a replica set, use kind ofReplicaSet. The numberof Pods to run is defined under the replicas parameter:

apiVersion: apps/v1
kind: ReplicaSet
metadata: 
	name: frontend
	 labels: 
		 app: guestbook
		  tier: frontend
	  spec:
	   # modify replicas according to your case
	    replicas: 3
	     selector: 
		     matchLabels: 
			       tier: frontend 
			template:
				metadata:
				 labels: 
					 tier: frontend 
					 spec: 
						 containers: 
							 - name: php-redis 
							 - image: gcr.io/google_samples/gb-frontend:v3
							 - 
Replica sets are successors of replication controller objects