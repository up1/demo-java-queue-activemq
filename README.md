# Spring Boot with ActiveMQ Artemis
* [ActiveMQ](https://activemq.apache.org/components/artemis/)
* [Spring Boot + ActiveMQ](https://docs.spring.io/spring-boot/docs/2.4.3/reference/html/spring-boot-features.html#boot-features-artemis)

## Steps

### 1. Download [ActiveMQ Artemis](https://activemq.apache.org/components/artemis/download/)
```
$cd ./bin
$./artemis create mybroker
$./mybroker/bin/artemis run

     _        _               _
    / \  ____| |_  ___ __  __(_) _____
   / _ \|  _ \ __|/ _ \  \/  | |/  __/
  / ___ \ | \/ |_/  __/ |\/| | |\___ \
 /_/   \_\|   \__\____|_|  |_|_|/___ /
 Apache ActiveMQ Artemis 2.17.0
```
 Access to console admin page `http://localhost:8161/console`
 * username=`demo`
 * password=`demo`

### 2. Start producer
```
$cd demo_activemq
$mvnw spring-boot:run
```

### 3. Start consumer
```
$cd demo_activemq-consumer
$mvnw spring-boot:run
```

### 4. Testing
Call api with url= http://localhost:8080/hello/<name>
 
