
Hello, Tim.

Welcome back.

Welcome to Google Cloud Training.

And today we will discuss about STB STB as load balancer components.

We will see what are the components of the SDB and SDB load balancer and what is the application of

each component so that we can understand the complete functioning of SDB and SDB as load balancer.

So let's start with.

So Team STB and STB as Load balancer have many components.

We have listed out few components, and we have described the function of the components in quite details.

So first one is the forwarding route.

Forwarding rule is something which will specify the external IP address, port and global target STB

Proxy.

Whenever you will create a HTTP or SD based load balancer in the GCP, you need to create a forwarding

rule as well.

Forwarding rule will automatically create an IP.

You need to define the port and if required, then we need to define the proxy server as well.

We can define that all the traffic which is coming from that particular external IP can be lead to the

proxy server.

Clients.

You can say browsers, they can have the IP address in order to connect to the load balancer.

So as we are aware that STB and STB requests or the protocols are required for the browser based application

or for the rest API.

So whenever a client is trying to connect to your application with the help of the HTTP and Stripe's

load balancer, they will connect your application with the help of the forwarding route.

So client will connect the load balancer with the help of the IP address of your forwarding rule and

the port where the application is running.

Each forwarding rule provide multiple single IP address that can be used in DNS record for the application.

So you can create the DNS or the domain specific name that we fully qualified a string.

It can be a URL of your application and you can map your forwarding route with that particular DNS.

It means all the traffic which is coming with the help of the DNS can lead to your application with

the help of the forwarding rules.

The forwarding rule for the HTTP load balancer only referred TCP port eight zero and 8080.

If you are creating the forwarding rule for the HTTP load right, then you can only mention the specific

port in relation to the IPS.

Eight zero and 8080.

But if your traffic is steep, as if your load balancer is a DPS, then you need to define port for

three in the forwarding route.

The types of the forwarding rules required by the external HTTPS load balancer depend on the network

service tier, or we can call it an SD.

So which kind of forwarding rule we are going to define in the HTTPS load balancer?

That depends on the SD.

Now let's try to understand what is the mnst and why we are using A.D when we are defending the forward.

What is the role of NST in the forwarding rule in https load balancer?

So NSD is basically a network layer or a network tier, which can be two type.

The first type is the premium tier, right?

Premium tier network layer.

The premium tier can be used for the highest performance.

Traffic between the Internet and the VM instance of your VPC network is routed by keeping within the

Google network as much as possible.

So whenever you are using the NSD, the premium tier NSD, and you have linked that particular NSD with

your forwarding rule, then all the traffic which is coming from the Internet.

That will travel by the Google internal network whenever that particular traffic is routing to your.

Premium tier.

NSD is the highest performance network tier.

Premium NST is required for the services that needs the global ability, right?

If your service is a global service, you want to connect the global user with your application, with

your service, then definitely you can go with the premium NST.

Every premium nest is unique to Google Cloud.

You cannot create the duplicate or redundant premium A.D. in the Google Cloud.

Premium nest is default nest in GCB.

Whenever you will create the forwarding rule, I will show you in the coming lecture whenever we will

go to the lab, right then, whenever we will create the forwarding rule, we have an option to choose

the standard and the premium.

Honesty and premium is always default.

So Google one does that.

We will use the highest performance network and all the traffic which is coming from the internet.

Once that traffic lent to my once that particular traffic will land on my forwarding rule that traffic

will travel to my VM with the help of the GCP internal network node by the internet.

Now the second nest is the standard tier that is cost optimized, that is cheap as compared to the premium

tier.

Right.

And traffic between the Internet and the VM instance in your VPC network is routed over the Internet

in general.

Right?

Whenever we are using the standard tier, then the traffic which is flowing from the internet to VM

that will use the general internet road.

It means it is not using the fastest Google network.

So you may face some kind of network delay or some kind of delay in your request and response whenever

you are using the standard NIST.

For services hosted entirely within reason.

A standard nst useful for the services which are hosted within reason.

If you have some small business and your business is reasonable and you want to make your business online

right, you want to expose your business to the online customers.

But you know very well that my customers are specific to this particular reason.

Only then you can use the standard Ernst instead of the premium tier amnesty.

As I told you earlier, performance of the Standard Nest A.D. is comparable to the other cloud providers.

STB and STB DBS load balancer in the premium tier use global external forwarding rules.

It means the forwarding rules which will be created inside the premium amnesty.

That will be the global forwarding rule.

But the forwarding rule, which is basically created inside the standard amnesty that will be the regional

forwarding rule.

So that difference can be easily understand that the standard tier can be used for the regional traffic

and premium tier can be used for the global traffic.

So we have done with the first component, which is forwarding all.

The next component of the STB.

STB base load balancer is the target proxy.

So target proxy is something which will receive a request from the client.

So whenever a particular request is hitting your DNS server, that DNS server is calling a load balancer

IP, right.

Which is the forwarding rule.

And that forwarding rule further sending the traffic to the target proxy.

So targeted proxy is something which is receiving the request from the client.

Then target proxy.

Evaluate that request by using the URL map to make traffic routing decision.

Now we got a new term which is called the URL map and the URL map we have discussed in the backend service.

So target proxy evaluate the request and base of the URL map that it is coming to some specific path

or that request is coming to the general URL.

On that basis of the URL map.

It will further take the decision and send that particular traffic to the specific backend service.

Proxy can also use authentication communication by using the SSL certificate.

So if you want to put the certificate, then you can put the SSL certificate at the proxy layer so that

your proxy server will take the SSL certificate, it will verify your assistant certificate and then

forwarding the traffic to the next hope.

If your user is using the HTTPS load balancing target proxy, use the global SSL certificate to provide

its identity to the clients.

So whenever you are using the HTTPS load balancing, your client is making the https call.

That call first need to be verified.

First need to be authenticated at the level of the proxy, right at the level of the target proxy and

that target proxy server or that private proxy.

If you are using the Google proxy that will identify the request, that will identify the client, and

then particular request can be forward to the next hope.

If that particular request is not a legitimate request, then that request will be rejected at the proxy

and you will not get any response back from the target proxy.

SDP has proxy used a global URL map to make the routing determination based on HTTP attributes such

as request path cookies and the header.

So whenever we are making the request, either we are making the request from the browser, either we

are making the request from the application itself, either we are making the request from any kind

of rest or any tool or any service which can make the HTTP or HTTPS kind of request.

We need to define a few things.

We need to define the URL, what we want to hit, right?

We need to define the particular path in the URL, which particular path we need to put.

We need to define some headers.

Right?

And on the basis of the headers, on the basis of the attribute of your HTTP call, the HTTPS proxy

will identify your request and take the routing decision.

Right.

Because all of the routing map is defined in the global URL map.

So that HTTPS proxy server will take the decision easily and send the traffic to the specific backend

whenever you are putting request to a specific path.

The URL map can specify additional actions such as sending reject to the client.

Let's discuss a bit about the URL map.

So whenever a request arrives at a load balancer, the load balancer root the request to a particular

backend service or backend bucket based on the configuration in the URL map.

So you can define the Google bucket as well.

You can define the backend service as well.

Right?

So if you want to send that particular request to a specific Google bucket, you can route that particular

request to the Google bucket.

But if you want to send your request to a specific backend service, on the backend service, we have

the instance group and behind the instance group we have the VM instances which are executing my application.

So you can redirect the request to the backend service as well.

These all things are defined in the URL map, so this will be pretty much clear when we will create

the HTTPS load balance.

And in the lab your map let set up you the type of host and path based routing.

We have discussed that particular thing as well, that if you have a single DNS value but in your application

you want to route different different kinds of services to the different different kind of machines

which are running behind the instance group.

So you can make it possible, you can define the path in the URL map and based of that particular path,

the request will follow the further traffic.

So in that case, whenever we are defining the URL map, each URL map has the name.

Your map has the same name as the name of the load balancer.

Every world map have the two components.

The first component is the host name and second is the path.

So suppose we are hitting a URL like HTTP example, dot net slash video slash SD.

So over here is CDP, example dot net is your DNS value, right?

This is your website name.

Now after your website name, whatever you are defining in the terms of the rest API that is called

resource path.

In the terms of the cloud, you can call it the backend service path or the URL path.

So over here we are defining the video.

Then slash SD, it means all the traffic which is coming to this particular URL that consists to property.

First, it consists the host, second, it consists the path.

So once the request will hit the DNS, right, that will decide whether forwarding rule forwarding rule

will further that request to the target https proxy server.

SD Best Proxy server Identify the request.

It will look into the host role, it will find the URL map, and if that particular URL map is matching,

then it will send that particular request to that particular URL map that you are.

MAP will send the request to the backend service.

Behind the backend service we have the instance group.

Or we have the nitro groups.

So request will be moved to next hope as per the configuration.

But at the level of the target proxy, it can be decided that on which particular backhand service,

that request needs to be surveyed.

If you can understand this particular scenario with this particular diagram.

So suppose we have a website and the website name is example dot net.

We have defined the different different URL map at the level of map.

We have defined the example dot net.

We have defined the example dot org.

We have defined the example dot net slash video SD.

We have defined the example dot net slash video slash SD.

Right.

We want to serve the traffic as per the request.

So request will lend to the load balancer.

Then next it will identify the URL map and if the URL map is example dot org.

Right.

So we have defined the different backend service for the OAG kind of traffic that will lead to the traffic

to a specific set of the VMs or a specific set of the instance group.

So that particular request will identify at the level of the proxy server on the basis of the URL map

and lead to a specific backend service which have the name backend service less or the site.

But if the request is example dot net, that's it, then it will lead to the next backend service,

backend service video site.

But if the URL in the request have a specific path, the example dot net slash video, select SD, then

it will identify the respective backend service.

If the backend service is defined, then it will lead to that particular backend service only in the

same way if the request have the different URL like example dot net video less SD and if a vacant service

is defined for that particular URL map, that particular URL map is defined in that target proxy, then

that will lead to that particular backend service.

Otherwise all the traffic will directly lead to the default backend service.

So by this particular way we can categorize then where we want to send the traffic.

So next component after the forwarding rule and the target approx is the backend service.

We have discussed about the back end service in quite details in the last two lectures as well.

So I hope everyone has the idea what is the back end service.

So the use of the back end services to distribute the request to help the back ends, It could be the

instance group containing the compute VM engines or the Google Kubernetes engine containers or the Google

cloud storage bucket.

So you can configure the backend service to anything.

You can configure it to the compute engine VM instance group, you can configure it to the Google Kubernetes

engine containers and you can configure it to the cloud storage bucket.

One or more back end must be connected to the back end service.

So whenever we are defining the back end service, it is required to connect to the back end to that

particular back end service so that there is someone to respond to the request whenever the request

will arrive.

Back end service can be either.

It means the receiver of the back service, it could be the instance group, or it could be the network

endpoint group, which we called an edge.

But we cannot define the combination of any G and instance group as a receiver from the back end service,

we can either define the instance group or the network endpoint.

User can enable the connecting draining to backend service to ensure minimum interruption in your users.

When an instance that is serving the traffic is terminated, removed manually removed via the auto scalar.

So there's a new term which we are hearing, which is called connection training.

You can learn about the connection training on the Google.

There is a there is a complete concept behind this particular term, the connection training.

Right.

But in short, we can understand that connection Training is something where the connection will be

automatically handled whenever whenever the client who is responding, that particular connection is

down.

These the short description of the connection training.

But you can learn about the connection training, you can search around it in the Google, we can have

the option to enable the connection training and it will help us to minimise the interruption in my

system.

Suppose in any case, if my machine got terminated, if my machine got removed, or if my machine got

removed by the auto load balancer.

In that case, if some client is connected to my machine, their connection will be lost.

But if connection training is enabled in my back end service, that particular connection will be shipped

to some other client before the load balancer set down that particular machine or whenever that particular

machine will order, terminate or stop that client connection will internally managed by the other connection.

So on the basis of a single cookie, that particular thing we managed and system can automatically identify,

establish the session with the new instance when whenever a connection will be interrupted or whenever

the machine will be go down.

If you want to change something in the back end service, then change the back end services associated

with the external https load balancer.

Right.

And that change is not instantaneous.

So what we are saying, we are saying if we change something in the back end service, then then we

cannot guarantee that particular change will be in effect immediately.

It can take several minutes to propagate that particular change through the network.

Now let's discuss the another term, which is called the session affinity.

So there is again a complete concept behind the session.

Affinity and session affinity is a very famous term.

The developers write session affinity is a best effort to attempt the sender request from a particular

client to the same back end.

As far as that particular back end is healthy.

It means when we have the multiple instances behind the instance group and that instance group is connected

with the back end service, that backend service is connected with the proxy server.

That proxy server is connected with the forwarding rule.

That forwarding rule is connected with the DNS and that DNS is accepting the request from the user.

So we can take a simple example.

Suppose you are a Facebook user, you are logging into your Facebook account, right?

So whenever you will log in your Facebook account, you will enter the base URL of the Facebook, which

is facebook.com.

That request will land on the DNS right after.

Then if suppose we are assuming that Facebook is using the Google account, although I am not sure about

it, but suppose we are assuming that the Facebook is using the Google cloud, then how that particular

request will travel.

So first you will go to your login page.

That login page have some specific URL path, that particular login page has some specific path.

Then you will enter your login credentials and you will log in.

So once you will log in, what will happen?

Your request will go to the the forwarding rule.

Forwarding rule will send the request to the proxy for proxy will identify the backend service it will

send to the request to the backend service.

Backend service will identify the instance group.

Instance group will send that particular request to the specific client.

That client will accept your request.

Right.

So you have a connection between you and that particular client.

Right.

So suppose if you will refresh your browser, then your request will follow the same route.

But what happens if this time your request will land on another client right through to which you don't

have the connection, to which you don't have the established decision?

In that case, it may possible you will face an authentication issue because in the first request,

your authentication connection will establish with the instance.

Well, whenever you will refresh the browser, you send another request and that is following the same

route.

And it may possible that hundreds of the instances are running, then that request will land on some

another instance.

In that case, you may face the logout or unauthenticated messages.

So we can cater this particular issue, how we can cater to this particular things.

So there is a term which is called station affinity.

So with the help of the Asian affinity, the client and the instance have the specific cookie.

They both will share a specific cookie and on the basis of that particular specific cookie, the request

will identify their route whenever you will send the next request or you will refresh your browser.

So that particular cookie will be established at the client side and at the instance side as well.

This is called the Asian affinity.

It is better.

So that section affinity is an attempt to send the request from a particular client to the same back

end as long as the back end is healthy.

Google Cloud has the deepest load balancer offer the types of session affinity we can have, the multiple

kind of session affinity in the Google Cloud store https load balancer.

The first is none, right?

Such an affinity is not set for the load balancer if you don't need the session affinity.

Suppose your users are not using the session, you are using the static website.

You are just serving the traffic.

You don't bother about the authenticity of the users.

You can use the non session affinity.

Another one is the client IP affinity.

Client IP affinity sends a request from a same client IP address to the same backend.

If you have the strict application you want, that same backend service will authenticate my IP request

and if you want that same backend service every time will authenticate or every time received the request

from a client.

Then you can configure the client IP affinity that will send the request from a specific client IP address

through a specific backend service.

And next one is the generated cookie affinity.

We have discussed about it that it will set a client cookie when the first request is made and then

send request to the cookie to the same backend.

And that cookie will be the based between the connection between your client and the backend service.

So these are the components of the HTTP load balancer team, right?

I hope I have explained each and every component in quite details if I still have you some doubt in

the components or the function of the IDPs load balancer In the coming lecture, I will show you how

we can create the HTTPS load balancer in Google Clouds so that it will cater your other doubts regarding

the STP and HTTPS load balancer.

So thank you, Tim.

Thanks for your time.

If you have any doubt, any question in this lecture, please let me know.

I will try to answer your questions.

Autoscroll

## Course content

## Overview

## Q&AQuestions and answers

## Notes

## Announcements

## Reviews

## Learning tools

[Back to All Questions](https://www.udemy.com/course/google-cloud-specialization/learn/#questions)