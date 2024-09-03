
![[Pasted image 20240713175819.png]]

A news feed web service has the following code running on Google App Engine. During peak load, users report that they can see news articles they already viewed.  
What is the most likely cause of this problem?

- A. The session variable is local to just a single instance Most Voted
- B. The session variable is being overwritten in Cloud Datastore
- C. The URL of the API needs to be modified to prevent caching
- D. The HTTP Expires header needs to be set to -1 stop caching

It's A. AppEngine spins up new containers automatically according to the load. During peak traffic, HTTP requests originated by the same user could be served by different containers. Given that the variable `sessions` is recreated for each container, it might store different data. The problem here is that this Flask app is stateful. The `sessions` variable is the state of this app. And stateful variables in AppEngine / Cloud Run / Cloud Functions are problematic. A solution would be to store the session in some database (e.g. Firestore, Memorystore) and retrieve it from there. This way the app would fetch the session from a single place and would be stateless.