## KAFKA COMMANDS

## run ZooKeeper
	bin/zookeeper-server-start.sh kafka/config/zookeeper.properties


## run kafka
	bin/kafka-server-start.sh kafka/config/server.properties

## stop kafka
	bin/kafka-server-stop.sh

## TOPICS

## create kafka topic
	bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 16 --topic transactions

## delete topic
	bin/kafka-topics.sh --zookeeper localhost:2181 --delete --topic test

## list topics
	bin/kafka-topics.sh --list --zookeeper localhost:2181

	docker run --rm confluentinc/cp-kafka kafka-topics.sh --list --zookeeper 10.2.36.136:2181

## describe topics
	bin/kafka-topics.sh --describe --zookeeper localhost:2181 --topic transactions

## alter retention
	bin/kafka-topics.sh --alter --zookeeper localhost:2181 --topic transactions --config retention.ms=10000

## get configs for a topic
	bin/kafka-configs.sh --zookeeper localhost:2181 --describe --entity-name transactions --entity-type topics

## run kafka producer console - The Kafka distribution provides a command utility to send messages from the command line. It start up a terminal window where everything you type is sent to the Kafka topic.
	bin/kafka-console-producer.sh --broker-list localhost:9092 --topic transactions

## run kafka consumer console
	bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic transactions --from-beginning

## consumer-GROUPS - gives offset values with lag
	bin/kafka-consumer-groups.sh --list --bootstrap-server localhost:9092

	bin/kafka-consumer-groups.sh --describe --group transactions-cg --bootstrap-server localhost:9092

	bin/kafka-consumer-groups.sh --describe --group transactions-cg --bootstrap-server localhost:9092 --members

	bin/kafka-consumer-groups.sh --describe --group transactions-cg --bootstrap-server localhost:9092 --state

## OFFSETS

## current offset
	bin/kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic transactions

## count messages in a topic
	bin/kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic transactions --time -1 --offsets 1 | awk -F ':' '{sum += $3} END {print sum}'

## offset reset for all topics
	bin/kafka-consumer-groups.sh --bootstrap-server localhost:9092 --group transactions-cg --reset-offsets --to-earliest --all-topics --execute

	bin/kafka-consumer-groups.sh --bootstrap-server localhost:9092 --group transactions-cg --reset-offsets --to-offset 1 --all-topics --execute



















## Kafka Topics
### List existing topics
 `bin/kafka-topics.sh --zookeeper localhost:2181 --list`

### Describe a topic
  `bin/kafka-topics.sh --zookeeper localhost:2181 --describe --topic mytopic `
### Purge a topic
 `bin/kafka-topics.sh --zookeeper localhost:2181 --alter --topic mytopic --config retention.ms=1000`
 
... wait a minute ...

 `bin/kafka-topics.sh --zookeeper localhost:2181 --alter --topic mytopic --delete-config retention.ms`
 
### Delete a topic
 `bin/kafka-topics.sh --zookeeper localhost:2181 --delete --topic mytopic`
 
### Get number of messages in a topic ???
 `bin/kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic mytopic --time -1 --offsets 1 | awk -F  ":" '{sum += $3} END {print sum}'`
 
### Get the earliest offset still in a topic
`bin/kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic mytopic --time -2`

### Get the latest offset still in a topic
`bin/kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list localhost:9092 --topic mytopic --time -1`

### Consume messages with the console consumer
`bin/kafka-console-consumer.sh --new-consumer --bootstrap-server localhost:9092 --topic mytopic --from-beginning`

## Get the consumer offsets for a topic
`bin/kafka-consumer-offset-checker.sh --zookeeper=localhost:2181 --topic=mytopic --group=my_consumer_group`

### Read from __consumer_offsets

Add the following property to `config/consumer.properties`:
`exclude.internal.topics=false`

`bin/kafka-console-consumer.sh --consumer.config config/consumer.properties --from-beginning --topic __consumer_offsets --zookeeper localhost:2181 --formatter "kafka.coordinator.GroupMetadataManager\$OffsetsMessageFormatter"`

## Kafka Consumer Groups

### List the consumer groups known to Kafka
`bin/kafka-consumer-groups.sh --zookeeper localhost:2181 --list`  (old api)

`bin/kafka-consumer-groups.sh --new-consumer --bootstrap-server localhost:9092 --list` (new api)

### View the details of a consumer group 
`bin/kafka-consumer-groups.sh --zookeeper localhost:2181 --describe --group <group name>`

## kafkacat

### Getting the last five message of a topic
`kafkacat -C -b localhost:9092 -t mytopic -p 0 -o -5 -e`

## Zookeeper

### Starting the Zookeeper Shell

`bin/zookeeper-shell.sh localhost:2181`