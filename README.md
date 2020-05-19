# kafka_commands 

# Start the zookeeper service
To start the zookeeper service, Open a new PowerShell As Administrator window in the C:\kafka_2.12-2.2.0 folder and run the following. Keep the window open.

```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties```

# Start the Kafka service
To start the kafka service. Open a new PowerShell As Administrator window in the C:\kafka_2.12-2.2.0 folder and run the following. Keep the window open.

```.\bin\windows\kafka-server-start.bat .\config\server.properties```

# Working with Kafka
To run these, open PowerShell as Admininstrator in C:\kafka_2.12-2.2.0 folder and topic_name must be replaced by our topic.

## To create a topic:
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --create  --replication-factor 1 --partitions 1 --topic topic_name```

## To delete a topic:
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --delete --topic topic_name```

## To list topics:
```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list```

## To write messages to the topic:
```.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic topic_name```

Then, A prompt expects for inserting the messages

## To view the messages on a topic:
```.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic topic_name --from-beginning```

</br>

# Unique commands from my work:

I have run the commands from C:\kafka_2.12-2.2.0 folder in Powershell

### Started the zookeeper service by running:

```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties```

### Started the kafka service by running:

```.\bin\windows\kafka-server-start.bat .\config\server.properties```

### Created a unique topic by running:

```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --create  --replication-factor 1 --partitions 1 --topic Interpol_Info```

### Listed all created topics by running:

```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list```

### Started a Kafka producer for writing messages to your unique topic by running:

```.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic Interpol_Info```

### Started a Kafka consumer for retrieving messages from your unique topic by running:

```.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic Interpol_Info --from-beginning```
