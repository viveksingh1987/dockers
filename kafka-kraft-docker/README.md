# Access kafka container
docker exec -it kafka bash

# Create a new Topic

/usr/bin/kafka-topics --create --topic test-topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1


# Send message 

/usr/bin/kafka-console-producer --broker-list localhost:9092 --topic test-topic

# Read Message

/usr/bin/kafka-console-consumer --bootstrap-server localhost:9092 --topic test-topic --from-beginning


# Check all topics

/usr/bin/kafka-topics --list --bootstrap-server localhost:9092


# Check all logs

docker logs kafka