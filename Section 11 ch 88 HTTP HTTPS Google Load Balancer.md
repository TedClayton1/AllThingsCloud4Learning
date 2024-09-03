
HTTP(S) load balancer is external global load balancer. 
➤  HTTP(S) load balancer uses multiple backend types. 
➤  Using the same Base URL request can be forward to multiple Backend Services. 
➤  HTTP(S) load balancer evaluates the request according to the URL map and sends the request to the correct service. 
➤  Clients can communicate with the load balancer by using the HTTP 1.1 or HTTP/2 protocol.  
➤  When HTTPS is used, modern clients default to HTTP/2. This is controlled on the client, not on the HTTPS load balancer. 

Welcome to Google Cloud Training.

And today we will discuss about a step and steps load balancer in Google Cloud.

So we will see what is the application of HTTP and SDB as load balancer and where we can apply the HTTP

and https load balancer in the Google cloud.

So let's start with.

So very first in this chart, we need to understand that GDP or GDP is load balancer or the external

global load balancer.

They are not GCP internal load balancer.

These load balancer are falling the external global load balancer category.

So when I'm saying that it's a global load balancer, it means it will present at a global layer, not

a regional or zonal layer.

So you can get that question in your Google Cloud associate certification exam that is HTTP or HTTPS

is a reasonable global or zonal.

So please make sure HTTP and HTTPS load balancer are external global load balancers.

As trips, load balancer, use multiple backend types.

What does it mean?

So team, whenever we will create a load balancer in the Google cloud that will have the two other component

as well.

One is called backend load balancer and another is called frontend load balancer.

So as load balancer use multiple backend types.

It means you can create a single SDP and SDP as load balancer, but that load balancer may have multiple

back end type of load balancer and every load balancer is associated with a particular URL map.

We will discuss about it in the next slide.

I will show you a complete diagram that how it can work.

But right now we need to understand that STP as load balancer, use multiple backend types and each

backend type may have the unique URL map.

We can understand this particular example.

Suppose you are working on some e-commerce site and that e-commerce site have the different different

modules that have the user card, that have the user orders, that have the home page, or that may

have the user management page, right?

So there could be the multiple kind of page on any e-commerce website.

So what do you need to do?

Although you are using a single DNS value to route to your traffic.

But in the back end you have mapped that particular DNS value to the STP or SDP as load balancer, and

you are executing different machines like you are executing three set of machines which are only serving

the traffic for the home page.

And another reason you are executing some machines which are only serving the traffic for the.

Other page in the another user and you have set up the machine which are only serving the traffic for

the.

Payment page or for some other page.

So what do you need to do?

You need to put a load balancer on the top of that machine, and that load balancer is accessing the

machines on a specific URL map.

So.

Suppose your website DNS values w w w dot test my website dot com.

Right now you can have multiple URL paths for the user accounts.

You can have the URL like w w w dot test my website dot com less user.

You can have the another url part like w w w dot test my website slash orders less home, less registration.

So we have the different different URLs and with the help of the https load balancer, what you can

do, you can map the URLs to a specific backend services, right?

And these backend load balancer or the services will be mapped to the steps load balancer.

So whenever a particular URL will hit a load balancer directly, send that particular traffic to the

specific backend service and specific backend service directly send the traffic to the machines which

are executing that kind of application.

Or it's specifically configured to serve only that particular traffic, right?

So we can configure multiple backend services with the HTTP and IPS load balancer in the Google Cloud.

So as I told you, using the same base URL request can be forwarded to the multiple backend services.

You can forward the request to the multiple services on the basis of the resource path.

S GDP and base load balancer.

Evaluate the request according to the URL map and send the request to the correct service.

As I told you, if you have different different set of services in different, different reasons.

So whenever a particular request will land on a https load balancer that will identify the unique backend

service for that particular URL map and send that particular traffic to that backend service, that

backend service or backend logical entity of the HTTPS load balancer.

Further, send the traffic to the machines which are configured to serve that traffic.

In the SDP and SDP as load balancer client can communicate with the load balancer by using HTTP 1.1

or HTTP two protocol.

Here the client is user's browser because HTTP and HTTPS are the load balancer, which comes first in

the OCI layer, which is the application layer.

So HTTP and UDP are the more powerful load balancer which can accept the traffic or the protocol of

HTTP 1.1 or HTTP to.

So when we are using the apps, so the modern clients or the modern browsers are used the HTTP two protocol.

We have already seen that in earlier lecture when I was trying to ping the external IP, the Google

Chrome was automatically sending the traffic on HTTPS, although I was not intended to send the request

on steps, but Google Chrome was automatically added the steps over there.

So by default the modern clients are using the HTTP two protocol.

This protocol or this kind of control is only available at the client side and not on the load balancer

site.

So you can't configure that.

A client can only send me the strip or Steve's request.

This all kind of configuration can be controlled at the client side.

You can't control that particular thing at the load balancer site.

So here we can understand the working of STP as a load balancer with this particular diagram.

So suppose you are a user, right?

So you are using the Internet to accessing some particular site.

So whenever you will hit the DNS value or the URL of that particular website, that request will directly

lend on the HTTPS load balancer, right?

And https load balancer will send that particular request to the global forwarding rules.

Forwarding rule is something which will forward your request and which will deny your request.

Then forwarding rule identify the request and it will send the request to the proxy server because the

request is coming from the internet.

So sometimes it is required to send the request to a specific proxy server or a specific VPN tunnels.

Once the request will be received at the proxy server, proxy server will evaluate that particular request

and further send that particular request to the URL map.

If you have defined some URL map in your https load balancer, URL map will send that particular request

to the backend services.

Suppose you have defined a number of URL maps, so backend service will identify that in which particular

backend service I need to send that particular request.

If the service have the URL map and have the URL path like the users and you have defined a specific

backend service for the slash users, that request will go to that particular backend service only if

you have the particular URL path like account like like card orders and you have defined the specific

backend service for these kind of URL maps, then the request will directly go to the specific backend

service.

And from that particular backend service, that request will directly go to the nodes.

After the backend service, that request will directly go for the health check.

Right, and help check further evaluate that the application is it is responding or not.

So this is the complete workflow of STP and STP as load balancer.

In the coming lecture, I will show you all details like the forwarding rule, proxy server, URL map,

backend service and the health check and other component of the HTTP industry like slash infinity and

the rules.

So this is about some application of the HTTP and load balancer.

We will discuss about all of these components in quite details in the coming lecture.

So thank you, Jim.

Thanks for your time.

Autoscroll

## Course content

## Overview

## Q&AQuestions and answers

## Notes

## Announcements

## Reviews

## Learning tools

[Back to All Questions](https://www.udemy.com/course/google-cloud-specialization/learn/#questions)