```shell
curl -s -u T2PMKC4GRUAGEVK4:6xblGQW1cEb+HA4aP4TNyMdDZWpDXs63aFP2/TUo8nhRGH+MUTtKzukkbfLUd424 \
      https://psrc-12d08v.eu-north-1.aws.confluent.cloud/subjects/products-value/versions \
      --header "Content-Type: application/vnd.schemaregistry.v1+json" \
      --data "@products-ruleset.json" | jq
```


```shell
curl -i -X PUT -H "Accept:application/json" -H  "Content-Type:application/json" http://localhost:8086/connectors/my-datagen-source1/config -d '{
    "name" : "my-datagen-source1",
    "connector.class": "io.confluent.kafka.connect.datagen.DatagenConnector",
    "kafka.topic" : "products",
    "value.converter.use.latest.version": "true",
    "value.converter.auto.register.schemas": "false",
    "value.converter.schema.registry.url": "https://psrc-12d08v.eu-north-1.aws.confluent.cloud",
    "producer.override.use.latest.version": "true",
    "producer.override.auto.register.schemas":"false",
    "confluent.topic.bootstrap.servers": "pkc-7xoy1.eu-central-1.aws.confluent.cloud:9092",
    "confluent.topic.replication.factor": "1",
    "output.data.format" : "AVRO",
    "quickstart" : "SHOES",
    "tasks.max" : "1"
}'
```


```shell

curl -s -u T2PMKC4GRUAGEVK4:6xblGQW1cEb+HA4aP4TNyMdDZWpDXs63aFP2/TUo8nhRGH+MUTtKzukkbfLUd424 \
      https://psrc-12d08v.eu-north-1.aws.confluent.cloud/subjects/products-value/versions \
      --header "Content-Type: application/vnd.schemaregistry.v1+json" \
      --data "@products-ruleset.json" | jq

```