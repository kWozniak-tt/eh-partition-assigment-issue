# KafkaTrigger - TypeScript

The `KafkaTrigger` makes it incredibly easy to react to new events from a Kafka Broker. This sample demonstrates a simple use case of processing data from a given Kafka Broker using TypeScript.

## How it works

For a `KafkaTrigger` to work, you must provide a topic name which dictates where the messages should be read from with authentication.

## Configuration

### EventHubs for Kafka

Add `EVENT_HUBS_BOOTSTRAP_URL` and `EVENT_HUBS_CONNECTION_STRING` and `EVENT_HUBS_TOPIC` and `EVENT_HUBS_CONSUMER_GROUP` to your `local.settings.json`

_local.settings.json_

```json
{
  "IsEncrypted": false,
  "Values": {
    "AzureWebJobsStorage": "UseDevelopmentStorage=true",
    "FUNCTIONS_WORKER_RUNTIME": "node",
    "EVENT_HUBS_BOOTSTRAP_URL": "{YOUR_EVENT_HUBS_NAMESPACE}.servicebus.windows.net:9093",
    "EVENT_HUBS_TOPIC": "{your eventhub topic}",
    "EVENT_HUBS_CONSUMER_GROUP": "{your eventhub consumer group (not $Default)}",
    "EVENT_HUBS_CONNECTION_STRING":"{your eventhub connection string}"
  }
}
```

### Others

Modify `function.json` or `KafkaTrigger` attribute according to your broker.