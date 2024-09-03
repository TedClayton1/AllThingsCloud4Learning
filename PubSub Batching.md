


A [batch](https://cloud.google.com/pubsub/docs/publisher#batching), within the context of Cloud Pub/Sub, refers to a group of one or more messages published to a topic by a [publisher](https://cloud.google.com/pubsub/docs/overview#publisher-subscriber-relationships) in a single publish request. Batching is done by default in the [client library](https://cloud.google.com/pubsub/docs/reference/libraries) or explicitly by the user. The purpose for this feature is to allow for a higher throughput of messages while also providing a more efficient way for messages to travel through the various layers of the service(s). Adjusting the batch size (i.e. how many messages or bytes are sent in a publish request) can be used to achieve the desired level of throughput.

Ideally, if cost is not a consideration and the use case requirement is met, instances of the publisher can be created on an as-needed basis with batching disabled. This minimizes latency and maximizes throughput by scaling horizontally on the number of publishers.

_Note: 1000 bytes is the minimum request size, so if a request is smaller than that, it will be rounded up to 1000 bytes for cost purposes._

However, in most cases, cost is a consideration and therefore sending multiple messages in a single publish request is one way to reach equivalent throughput with fewer publishers. Since messages will be held in order to fill batches, it can result in an increase in latency.