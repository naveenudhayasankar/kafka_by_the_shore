Start the docker container using the command: 
docker-compose up -d

Check the status of the images either using Docker Desktop or by using the command, 
docker-compose ps 
docker-compose ps --format "{{.ID}} : {{.Command}}"

Enter into Kafka container using Docker Desktop. 
1. Create a topic. 
	kafka-topics --create --topic test_topic --partitions 3 --replication-factor 1 --bootstrap-server localhost:9092

2. Create a producer. 
	kafka-console-producer --topic test_topic --bootstrap-server localhost:9092

3. Create a consumer in a different terminal. 
	kafka-console-consumer --topic test_topic --bootstrap-server localhost:9092

Now the messages sent in the Producer's terminal are read by the Consumer and displayed in its terminal.


