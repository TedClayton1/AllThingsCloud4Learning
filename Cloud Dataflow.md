Exactly once processing
Dataflow is a Google Cloud service that provides unified stream and batch data processing at scale. Use Dataflow to create data pipelines that read from one or more sources, transform the data, and write the data to a destination. Fully managed service for transforming and enriching data in stream(real time) and batch (historical) modes with equal reliability and expressiveness- no more complex workarounds or compromises needed.

Typical use cases for Dataflow include the following:

- Data movement: Ingesting data or replicating data across subsystems.
- [ETL](https://cloud.google.com/learn/what-is-etl) (extract-transform-load) workflows that ingest data into a data warehouse such as BigQuery.
- Powering BI dashboards.
- Applying ML in real time to streaming data.
- Processing sensor data or log data at scale.

Dataflow uses the same programming model for both batch and stream analytics. Streaming pipelines can achieve very low latency. You can ingest, process, and analyze fluctuating volumes of real-time data. By default, Dataflow guarantees [exactly-once processing](https://cloud.google.com/dataflow/docs/concepts/exactly-once) of every record. For streaming pipelines that can tolerate duplicates, you can often reduce cost and improve latency by enabling [at-least-once mode](https://cloud.google.com/dataflow/docs/guides/streaming-modes).

## Advantages of Dataflow

This section describes some of the advantages of using Dataflow.

### Managed

Dataflow is a fully managed service. That means Google manages all of the resources needed to run Dataflow. When you run a Dataflow job, the Dataflow service allocates a pool of worker VMs to execute the pipeline. You don't need to provision or manage these VMs. When the job completes or is cancelled, Dataflow automatically deletes the VMs. You're billed for the compute resources that your job uses. For more information about costs, see [Dataflow pricing](https://cloud.google.com/dataflow/pricing).

### Scalable

Dataflow is designed to support batch and streaming pipelines at large scale. Data is processed in parallel, so the work is distributed across multiple VMs.

Dataflow can autoscale by provisioning extra worker VMs, or by shutting down some worker VMs if fewer are needed. It also optimizes the work, based on the characteristics of the pipeline. For example, Dataflow can [dynamically rebalance work](https://cloud.google.com/dataflow/docs/dynamic-work-rebalancing) among the VMs, so that parallel work completes more efficiently.

### Portable

Dataflow is built on the open source [Apache Beam](https://beam.apache.org/) project. Apache Beam lets you write pipelines using a language-specific SDK. Apache Beam supports Java, Python, and Go SDKs, as well as [multi-language pipelines](https://beam.apache.org/documentation/programming-guide/#multi-language-pipelines).

Dataflow executes Apache Beam pipelines. If you decide later to run your pipeline on a different platform, such as Apache Flink or Apache Spark, you can do so without rewriting the pipeline code.

### Flexible

You can use Dataflow for relatively simple pipelines, such as moving data. However, it's also suitable for more advanced applications, such as real-time streaming analytics. A solution built on Dataflow can grow with your needs as you move from batch to streaming or encounter more advanced use cases.

Dataflow supports several different ways to create and execute pipelines, depending on your needs:

- Write code using the Apache Beam SDKs.
    
- Deploy a [Dataflow template](https://cloud.google.com/dataflow/docs/concepts/dataflow-templates). Templates let you run predefined pipelines. For example, a developer can create a template, and then a data scientist can deploy it on demand.
    
    Google also provides a [library](https://cloud.google.com/dataflow/docs/guides/templates/provided-templates) of templates for common scenarios. You can deploy these templates without knowing any Apache Beam programming concepts.
    
- Use [JupyterLab notebooks](https://cloud.google.com/dataflow/docs/guides/interactive-pipeline-development) to develop and run pipelines iteratively.
    

### Observable

You can monitor the status of your Dataflow jobs through the [Dataflow monitoring interface](https://cloud.google.com/dataflow/docs/guides/monitoring-overview) in the Google Cloud console. The monitoring interface includes a graphical representation of your pipeline, showing the progress and [execution details](https://cloud.google.com/dataflow/docs/concepts/execution-details) of each pipeline stage. The monitoring interface makes it easier to spot problems such as bottlenecks or high latency. You can also [profile](https://cloud.google.com/dataflow/docs/guides/profiling-a-pipeline) your Dataflow jobs to monitor CPU usage and memory allocation.

## How it works

Dataflow uses a data pipeline model, where data moves through a series of stages. Stages can include reading data from a source, transforming and aggregating the data, and writing the results to a destination.

Pipelines can range from very simple to more complex processing. For example, a pipeline might do the following:

- Move data as-is to a destination.
- Transform data to be more useable by the target system.
- Aggregate, process, and enrich data for analysis.
- Join data with other data.

A pipeline that is defined in Apache Beam does not specify _how_ the pipeline is executed. Running the pipeline is the job of a [_runner_](https://beam.apache.org/documentation/basics/#runner). The purpose of a runner is to run an Apache Beam pipeline on a specific platform. Apache Beam supports multiple runners, including a [Dataflow runner](https://beam.apache.org/documentation/runners/dataflow/).

To use Dataflow with your Apache Beam pipelines, specify the Dataflow runner. The runner uploads your executable code and dependencies to a Cloud Storage bucket and creates a Dataflow _job_. Dataflow then allocates a pool of VMs to execute the pipeline.

The following diagram shows a typical ETL and BI solution using Dataflow and other Google Cloud services


Cloud Pub/Sub to Cloud Dataflow: Cloud Dataflow is a managed data processing service that can be used to process and transform streaming data. By using Cloud Dataflow with Cloud Pub/Sub, you can implement custom processing logic to ensure data is delivered in strict chronological order with no repeats. This combination allows you to achieve guaranteed-once FIFO delivery