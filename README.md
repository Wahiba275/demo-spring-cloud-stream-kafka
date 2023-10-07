# Event Driven Architecture - JMS et KAFKA
# Table of Contents
<ul>
  <li><a href="#introduction">Introduction</a></li>
  <li>
    <a href="#start-kafka-server">Starting Kafka Server</a>
    <ul>
      <li><a href="#start-zookeeper">Start Zookeeper</a></li>
      <li><a href="#start-kafka-server">Start Kafka Server</a></li>
    </ul>
  </li>
  <li><a href="#testing-with-kafka-tools">Testing with Kafka Tools</a></li>
  <ul>
    <li><a href="#kafka-console">KAFKA Console</a></li>
    <li><a href="#rest-controller-with-stream-bridge">Rest Controller with Stream Bridge</a></li>
    <li><a href="#consumer-kafka">Consumer KAFKA</a></li>
    <li><a href="#supplier-kafka">Supplier KAFKA</a></li>
    <li><a href="#function-kafka">Function</a></li>
    <li><a href="#kafka-stream">Kafka Stream</a></li>
  </ul>
</ul>

<h1 id="introduction">Introduction</h1>

Event-Driven Architecture (EDA) is a way of building software where components communicate through events or messages. Two popular tools for EDA are JMS and Kafka.
JMS (Java Message Service) helps applications send and receive messages in a reliable way. It's great for making sure important information gets to where it needs to be.
Kafka is a powerful tool for handling lots of real-time data. It's like a super-fast conveyor belt for events, making it perfect for scenarios where you need to process data as it comes in, like tracking website clicks or managing system logs.<br>
In EDA, these tools help different parts of your software talk to each other efficiently and handle events as they happen.

<h1 id="starting-kafka-server">Starting Kafka Server</h1>
<h2 id="start-zookeeper">Start Zookeeper</h2>

`start bin\windows\zookeeper-server-start.bat config/zookeeper.properties`

![Image Alt Text](/Kafka/Zookeeper.PNG)
<h2 id="start-kafka-server">Start Kafka Server</h2>
`start bin\windows\kafka-server-start.bat config/server.properties`

![Image Alt Text](/Kafka/kafka.PNG)

<h1 id="testing-with-kafka-tools">Testing with Kafka Tools</h1>
<h2 id="kafka-console">KAFKA Console</h2>
1. Consuming messages by subscribing to a topic<br>

`start bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic R1`

2. Publishing messages to topics<br>

`start bin\windows\kafka-console-producer.bat --bootstrap-server localhost:9092 --topic R2`

![Image Alt Text](/Kafka/consoleKafka.PNG)

3. Docker Compose
   
   `docker-compose up`

   `docker exec --interactive --tty broker kafka-console-consumer --bootstrap-server broker:9092 --topic R2`

   `docker exec --interactive --tty broker kafka-console-producer --bootstrap-server broker:9092 --topic R2`

   ![Image Alt Text](/Kafka/docker-compose.PNG)
   
<h2 id="rest-controller-with-stream-bridge">Rest Controller with Stream Bridge</h2>

![Image Alt Text](/Kafka/publishRestController.PNG)

![Image Alt Text](/Kafka/Cons.PNG)

![Image Alt Text](/Kafka/cons3.PNG)

<h2 id="consumer-kafka">Consumer KAFKA</h2>

![Image Alt Text](/Kafka/PageEventConsumer.PNG)

![Image Alt Text](/Kafka/pageCons.PNG)


<h2 id="supplier-kafka">Supplier KAFKA</h2>

![Image Alt Text](/Kafka/supplier1.PNG)

![Image Alt Text](/Kafka/supp.PNG)
<h2 id="function-kafka">Function</h2>

![Image Alt Text](/Kafka/f.PNG)

![Image Alt Text](/Kafka/f2.PNG)

<h2 id="kafka-stream">Kafka Stream</h2>

![Image Alt Text](/Kafka/KafkaStream.PNG)

![Image Alt Text](/Kafka/hhhhh.png)






