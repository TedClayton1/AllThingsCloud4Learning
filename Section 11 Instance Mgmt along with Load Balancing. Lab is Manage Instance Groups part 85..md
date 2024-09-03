
1. GCP - choose project- Compute Engine - Instance groups
2. Click Create Instance Group
3. Name it and give Description
4. Multi-zone
5. Create new Instance Template-Name,Location/Region(recommended)-choose a disk-Machine Config-Machine type
6. Identity-API access (Allow default access)
7. Firewall-Allow Http,https
8. Disks section-Add new disk
9. Type-Std persistent disk
10. Size-50GB
11. Click -Save
12. Networking-Network tags-default-network
13. Save/Continue *If external Ip was available go with ephermal* Name created automatically.
14. Go back to Create an Instance Group
15. Autoscaling mode-Choose autoscale-If you go with autoscale you can define the metrics under autoscaling signals. On the basis of these metrics Google will decide whether it needs to increase the number of instances or decrease em. Suppose I edit the cpu utilization to 10%. Whenever the CPU utilization of all the nodes will increase 10%, right up to 10%, Google will spin up a new node right again. when it will reach an average of 10%, Google will spin another node. Again, it will reach a average of 10%. Google will spend another one. If you keep it up to 90% or 90% like this. When the avg CPU will jump tump up to %80, Google will spin up a new node on the basis of the same thing.
16. Under new signal -choose http: load balancing utilization
17. Disable autoscaling and use 3 number of instances.
18. Define the min # of nodes and max # of nodes. If you've defined autoscaling you can define the minimum and max number of nodes on hte basis of auto scaling. Suppose I'm not taking the hardcoded node 3 (number of instances) over there right? In that case when traffic will increase it will spend up at a max ten nodes in this particular instance group and the minimum number of nodes would be 1. You can change these as well. At peak time max # of nodes will be 10 ant the min # of nodes i want to keep in my application will be 2.
19. Is the best option to keep it limited or autoscale? Autoscale is best per speaker in course. If you keep it limited , then youll get a static cost of this particular operation. Though you're getting less number of traffic, but at least 3 nodes or the node which you defined in the instance that much of node will always in the execution of your application.
20. Autohealing - We are getting the auto healing inside the health check and we can see that we can create the health check or we can spin up this particular instance group with the no health check. If no healthcheck is define, then it will not identify that application is running or not. 
21. Healthcheck- To create a health check we need to create some protocols. (name), protocol(tcp,80) , proxy protocol (none). If youre defining tcp, then you can say the request is optional and response is optional
22. Health Criteria - check interval (5) timeout (5). This means the health check will wait for the five second response. 
23. Healthy threshold- attempt of consecutive successes (2)and unhealthy threshold will be (3) attempts
24. Author wants to change protocol to http, request path to = /
25. Save 
26. Initial delay- Let's put initial delay to 300 seconds. This means after that particular time, the health check will start working on your machine. This is important because if the initial delay isn't there, then as soon as your instance will have a health check will start on that particular instance. We know very well that any application takes some time to start. That particular health check will fail. It will fail and it will spin up the new instances so that we are putting the initial delay. Let's keep it at 300
27. Autohealing health check- We have defined the http health check. We need to define some application which will execute over the http protocol on port 80 because we have defined the healthceck list that you all can see. So we have defined the http protocol on port 80. So we must need to put some kind of application which will execute on my instance on port 80.
28. Instance template-click edit instance template.
29. Firewall-Allow http traffic and https traffic on my template
30. Lets go to Automation-Startup script and insert it into box . This is a script sudo update which will update all the existing packages.Then it will install Apache two an then this will insert this particular index.html file in my apache server so that I will get the application on the http protocol on port 80. So this will execute the Apache server and this particular HTML page, which will show you the syntax
31. Copy and paste the script inside my instance template, it means all the machine which will create with the help of this particular instance, they must have this particular script at startup script, and all of the machines which will execute from this particular instance template from this which will be the part of this particular instance group. They must have a valid health check on Port 80.
32. Let's save and create this
33. Go to VPC Network-We have chose the default network and by default the http traffic isn't allowed on your instance. We need to modify the firewall rule. Although I already have the firewall rule for HTTP zero. But if you don't have the you need to create a new firewall rule. 
34. Create firewall rule-firewall rules (name) = http-rule . priority is 100 , rules off, 
35. Targets-all instances in the network
36. Source IP range 0.0.0.0/0 which means all ip addresses in world.
37. Ports/protocol-Specified protocols -tcp-port 80 now lets create this firewall rule
38. Once created , go to your compute engines-instance groups
    ***Got stuck as I got error message I didn't create a backend service for instance group. Created a backend service and still got same message. Exercise aborted.***
    
