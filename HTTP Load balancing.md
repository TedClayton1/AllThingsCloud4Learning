

HTTP(S) load balancing is ==a technique that distributes traffic across multiple web or application servers to improve resource utilization and system throughput==. When a user clicks on a URL, the load balancer determines which server in a pool is available to process the request and routes the traffic to that server. This prevents any single server from becoming overwhelmed, which can cause a website to crash during sudden traffic spikes. Load balancing can also improve availability and reduce the risk of server failure by enabling services to fail over to another server instance if the original one is unavailable. 

Load balancers use predefined algorithms to distribute incoming requests across multiple servers. Some common methods include round robin, least connections, and IP hash. For example, round robin load balancing allocates client requests to available servers in a group, then redirects all requests to each server in turn. 

Load balancers can also scale infrastructure by dynamically adding or removing servers in response to traffic levels. For example, an application load balancer might send requests for browsing products to servers that contain images and videos, but shopping cart requests to servers that can maintain many client connections.


