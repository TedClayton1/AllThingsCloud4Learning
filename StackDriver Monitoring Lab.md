
1. Select Project
2. We need to create multiple instances so we will create the instance group so that we can easily create multiple VM machines with the same configuration
3. Click on instance group
4. Click create instance group and name it
5. Choose zone
6. Create new instance template/name it
7. Choose machine/std image
8. Allow default access
9. firewall Allow Http/Https
10. Management- use startup script from earleir
11. Networking - default network
12. Network tags (monitoring-sample)
13. Save/continue
14. Scroll down dont touch autoscaling/properties
15. Change the min number of instances to 3 and max to 5.
16. Don't define healthcheck and click create
17. This instance group basically created three instances in my VM instances. When we go to "instance groups" we see 3 instances started .
18. Go to Compute engine and click vm instances. You'll see three instances are running and we have random name of instance group. YOu'll notice random names monitoring-ig-1-tedc-vf8d,w611 and zzjv
19. Let's open any external ip in a new tab.
20. If the web page isn't showing it's because it's hitting https instead of http.
21. Now we need to setup mOnitoring. Go to Operations in Google menu hamburger menu open it-Type in Monitoring and go to overview
22. Go to -Resource Dashboards an notice Firewalls/vm instances 
23. These instances, this disk we just created. firewall rules already exist in my account and I hope this cloud pops up
24. In overview we have the name of project we're getting complete resources, incidents and charts? No charts I see.
25. Go to Dashboards and notice we're getting the dashboards like cloud pops, disk firewall an instance.
26. Create net Dashboard
27. 