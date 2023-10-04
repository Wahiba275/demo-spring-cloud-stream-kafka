# Event Driven Architecture - JMS et KAFKA
# Table of Contents
<ul>
  <li>Introduction</li>
  <li>Starting Kafka server</li>
        <ul>
          <li> Start Zookeeper</li>
          <li>Start Kafka Server</li>
        </ul>
  <li>Testing with Kafka Tools</li>
  <ul>
    <li>KAFKA Console</li>
     <li>Rest Controller with Stream Bridge</li>
     <li>Cunsomer KAFKA</li>
     <li>Supplier KAFKA</li>
    <li>Function</li>
    <li>Kafka Stream</li>
  </ul>
  <li>Conclusion</li>
</ul>

# Introduction 

Event-Driven Architecture (EDA) is a way of building software where components communicate through events or messages. Two popular tools for EDA are JMS and Kafka.
JMS (Java Message Service) helps applications send and receive messages in a reliable way. It's great for making sure important information gets to where it needs to be.
Kafka is a powerful tool for handling lots of real-time data. It's like a super-fast conveyor belt for events, making it perfect for scenarios where you need to process data as it comes in, like tracking website clicks or managing system logs.<br>
In EDA, these tools help different parts of your software talk to each other efficiently and handle events as they happen.

# Starting KAFKA Server
## Start Zookeeper
`start bin\windows\zookeeper-server-start.bat config/zookeeper.properties`
![Zookeeper](example.jpg)
## Start Kafka Server 
`start bin\windows\kafka-server-start.bat config/server.properties`
![Kafka](example.jpg)
# Testing with Kafka Tools
## KAFKA Console 
1. Consuming messages by subscribing to a topic
`start bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic R1`
2. Publishing messages to topics
`start bin\windows\kafka-console-producer.bat --bootstrap-server localhost:9092 --topic R2`
![producer](example.jpg)
## Rest Controller with Stream Bridge
![producer](example.jpg)
![producer](example.jpg)
![producer](example.jpg)


