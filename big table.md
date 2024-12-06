Google Bigtable is a sparsely populated table that can scale to billions of rows and thousands of columns, enabling you to store terabytes or even petabytes of data. A single value in each row is indexed; this value is known as the row key. Bigtable is ideal for storing large amounts of single-keyed data with low latency.

As of January 2022, Google Cloud Bigtable was able to handle ==more than 5 billion requests per second==. At peak, Bigtable has been known to process over 6 billion requests per second. Bigtable's performance is predictable and linearly scalable, allowing users to increase or decrease the number of cluster nodes to scale their operations without downtime. Bigtable can also automatically scale up or down to meet changing workload demands. 

Bigtable's approximate throughput depends on the type of storage used by the cluster. For example, an SSD cluster can provide up to 17,000 rows per second for reads, 14,000 rows per second for writes, and 220 MB/s for scans. An HDD cluster can provide up to 500 rows per second for reads, 10,000 rows per second for writes, and 180 MB/s for scans. These estimates assume that each row contains 1 KB of data.

Google Cloud BigTable is a scalable, fully-managed NoSQL wide-column database that is suitable for both real-time access and analytics workload.

Good for:
-Low latency read/write access
-High-throughput analytics
-Native time series support
-Holding "Click Stream" data i.e 10,000 clicks per second and clickstream event messages
Common workloads:
-IoT finance,adtech
-Personlization,recommendations
-Monitoring
-Geospatial datasets
-Graphs

Cloud Bigtable is a fully managed, scalable NoSQL database service for large analytical and operational workloads and lets you store large amounts of single-keyed data with very low latency.

Cloud Bigtable excels as a storage engine for batch MapReduce operations, stream processing/analytics, and machine-learning applications.

https://cloud.google.com/bigtable/docs/overview

As pointed out in this example use case by Google, Google Cloud Bigtable, a high-performance NoSQL database service, integrates with Google Cloud Dataproc to provide a convenient low-latency data store.

https://cloud.google.com/customers/zulily

Domain

2.33

Question 18Incorrect