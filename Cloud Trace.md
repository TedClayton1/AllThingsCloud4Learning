
Cloud Trace, a distributed tracing system for Google Cloud, helps you understand how long it takes your application to handle incoming *requests* from users or other applications, and how long it takes to complete operations like RPC calls performed when handling the requests. Cloud Trace can also help you when you are developing a service or troubleshooting a failure. For example, it can help you understand how requests are processed in a complicated microservices architecture, and it might help you identify which logs to examine.

Because Cloud Trace receives latency data from some Google Cloud services, such as [App Engine](https://cloud.google.com/appengine/docs), and from applications instrumented with the [Cloud Trace API](https://cloud.google.com/trace/api), it can help you answer the following questions:

- How long does it take my application to handle a given request?
- Why is it taking my application so long to handle a request?
- Why do some of my requests take longer than others?
- What is the overall latency of requests to my application?
- Has latency for my application increased or decreased over time?
- What can I do to reduce application latency?
- What are my application's dependencies?

If your curious about how you can use Cloud Trace to help you manage your applications, then read the blog [Troubleshooting distributed applications: Using traces and logs together for root-cause analysis](https://cloud.google.com/blog/products/devops-sre/using-cloud-trace-and-cloud-logging-for-root-cause-analysis).

For information about profiling your application, see [Cloud Profiler](https://cloud.google.com/profiler).

## Environment support

Cloud Trace runs on Linux in the following environments:

- [Compute Engine](https://cloud.google.com/compute/docs)
- [Google Kubernetes Engine (GKE)](https://cloud.google.com/kubernetes-engine/docs)
- [App Engine flexible environment](https://cloud.google.com/appengine/docs/flexible)
- [App Engine standard environment](https://cloud.google.com/appengine/docs/standard)
- [Cloud Run](https://cloud.google.com/run/docs)
- Non-Google Cloud environments

Cloud Trace provides client libraries for instrumenting your application to capture trace information. For per-language setup instructions, see [Instrument for Cloud Trace](https://cloud.google.com/trace/docs/setup).

## Configurations with automatic tracing

Some configurations result in automatic capture of trace data:

- App Engine standard environment
    
    Java 8, Python 2, and PHP 5 applications don't need to use the Cloud Trace client libraries. These runtimes automatically send latency data to Cloud Trace for requests to application URIs. The requests include latency data for round-trip RPC calls to App Engine services. Cloud Trace works with all App Engine Admin APIs, with the exception of Cloud SQL.
    
- Cloud Run functions and Cloud Run
    
    For incoming and outgoing HTTP requests, latency data is automatically sent to Cloud Trace.
    

## Language support