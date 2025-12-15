# Eventbridge Mesh - Single Consumer Example

Slightly modified from a sample found in [aws-cdk-examples](https://github.com/aws-samples/aws-cdk-examples/tree/main/python/eventbridge-mesh/single-consumer) to all consumers in an AWS org to put messages on the producer event bus, which then get forwarded to the consumer.

Also fixed what looks like a small bug where the example was creating a consumer event bus using `events.EventBus.from_event_bus_arn` but specifying the default event bus, not the one specified in `ConsumerStack`

Put events using `aws events put-events --entries file://entries.json`

Also realised there [this sample](https://github.com/aws-samples/aws-cdk-examples/tree/main/python/cross-account-eventbridge-in-organization), which does the same thing as my changes!