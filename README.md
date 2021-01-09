# Kafka-producer-consumer
Kafka-producer-consumer code


step1 :  Download Kafka src file from website and place to C drive with file name changed to kafka.

step2 : inside of server.properties file edit log.dirs like below. Path to server.properties is C:\kafka\config
        log.dirs=C:/kafka/kafka-logs

step3 : inside of zookeeper.properties file edit dataDir like below. Path to zookeper.properties is C:\kafka\config
        dataDir=C:/kafka/zookeeper-data



C:\kafka\bin\windows

Starting the Zookeeper Server:     1>    zookeeper-server-start.bat ..\..\config\zookeeper.properties
Starting the Kafka Server:     2>    kafka-server-start.bat ..\..\config\server.properties


Checking available toipcs:   kafka-topics.bat --zookeeper localhost:2181 --list

Option –describe returns description of all existing topics :   C:\kafka\bin\windows>kafka-topics.bat --zookeeper localhost:2181 --describe

Topic creation:   kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 -topic <testingTopice name>

Push message from command line:   kafka-console-producer.bat --topic javatechie --bootstrap-server localhost:9092

consume messages checking command level:     kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic <testingTopice name>



CMD for Know the messages from beginning onwards topic based:

C:\kafka\bin\windows>kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic javatechie --from-beginning
