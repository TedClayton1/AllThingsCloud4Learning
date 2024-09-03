CDN- Content Delivery Network
CDN Function: CDN Cache Website and application content closer to users for better performance.
Low Cost, low latency content delivery using Google's global Network.
The closer data to user location, the better performance in serving. 
CDN caches website/application data closer to user via Cloud CDN Locations-
	* Referred to as Point of Presence (POPS)*
	* Currently over 100 locations worldwide.
	* Hop off Point between Google's private network and the public Internet.



Cloud CDN            Load Balancer                vm instance(3 to load bl)
(connected to users)

So load balancer further is connected by a cloud CDN and and cloud CDN is connected to users. So over here the application is running on the VM instances and the user traffic to VM instances is 
basically routed via load balancer. 

Between the user and the load balancer, there's one more thing called "Cloud CDN". The users are accessing your website from the public internet. Public internet will send the request to the Cloud CDN, and that Cloud CDN will render the request to the load balancer.

Let's suppose all these three users from the North America and any of them is basically submitted,  they get called for some kind of content. Then as a first request, that content will be served by the backend. This means the request will further go to the load balancer, then it will be processed by the [[VM instance]].

Then the response will get back to the load balancer, that response will get back to the [[Cloud CDN]] and then that response will get back to the end user(s). However, after that, if any of the user will hit the same request, then that request will not be processed by the VM instances/backend.

That request will be processed by the Cloud CDN itself because CDN has cashed the last response. So the same response will be returned to the next user who is going to submit the exact same request.

Cloud CDN is a cache system for your web application or your application

CDN Terminology-

Cache Miss- First time content request not at cache location. As stated before, when you will hit the first request, if that request is not in the season then the request will be processed by the backend application that is called cache miss. This means first time the content request noted cache location.

Cache Fill- Subsequent request will pull content from cache. This means once you have processed the first request, if the same request will be hit by the user again, then that request will not be processed by the backend, but the complete content of that request will be pulled from the cache system .

Cache Key-Identifier for cached content. The identifier for cache content. In the CDN you have the data in the key value pair. in the key you will get the [[URI]] (Uniform Resource Identifier).

So the request URI or request URL will work as a key in the cache management system and the request response will be the value of that particular key for the cache management system. The request will be exact match. This means cache mgmt system will create a unique key unique request when you are going to put some kind of extra query parameter or extra parameter in your request, that will be a cache missed for the CDN. That request will be processed by Backend. For the Cache management system, the request should be exact match.