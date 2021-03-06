********************** 42. Kafka SDK List ***********************
Enlaces:
https://www.conduktor.io/kafka/kafka-sdk-list

********************** 43. Creating Kafka Project ***********************
Enlaces:
https://docs.aws.amazon.com/corretto/latest/corretto-11-ug/what-is-corretto-11.html
https://www.jetbrains.com/idea/download/#section=linux
https://www.conduktor.io/kafka/creating-a-kafka-java-project-using-gradle-build-gradle
https://www.conduktor.io/kafka/creating-a-kafka-java-project-using-maven-pom-xml

https://github.com/gtorres04/kafka-beginners-course/releases/tag/43_Creating_Kafka_Project

********************** 44. Java Producer ***********************

* Kafka Producer: Java API - Basics

- Aprender como escribir un productor básico para enviar datos a kafka.
- Ver los parámetros de configuración básicos
- Confirmaremos como recibimos los datos en un consumidor kafka (Console)

https://github.com/gtorres04/kafka-beginners-course/releases/tag/44_Java_Producer

********************** 45. Java Producer Callbacks ***********************

* Kafka Producer: Java API - Callbacks

Veremos las devoluciones de llamada de la api de java, entonces:
- Entendamos desde el propio productor a que particion y offset se envio el mensaje, utilizando callback.
- Hechemos un vistaso a algo llamado StickyPartitioner, que es un comportamiento muy interesante del productor.

https://github.com/gtorres04/kafka-beginners-course/releases/tag/45_Java_Producer_Callbacks

Resultado al ejecutar el codigo enviando un solo mensaje

[main] INFO ProducerDemoWithCallback - I am a Kafka Producer
[main] INFO org.apache.kafka.clients.producer.ProducerConfig - ProducerConfig values: 
	acks = -1
	batch.size = 16384
	bootstrap.servers = [127.0.0.1:9092]
	buffer.memory = 33554432
	client.dns.lookup = use_all_dns_ips
	client.id = producer-1
	compression.type = none
	connections.max.idle.ms = 540000
	delivery.timeout.ms = 120000
	enable.idempotence = true
	interceptor.classes = []
	key.serializer = class org.apache.kafka.common.serialization.StringSerializer
	linger.ms = 0
	max.block.ms = 60000
	max.in.flight.requests.per.connection = 5
	max.request.size = 1048576
	metadata.max.age.ms = 300000
	metadata.max.idle.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partitioner.class = class org.apache.kafka.clients.producer.internals.DefaultPartitioner
	receive.buffer.bytes = 32768
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retries = 2147483647
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	transaction.timeout.ms = 60000
	transactional.id = null
	value.serializer = class org.apache.kafka.common.serialization.StringSerializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1651594079641
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 2
Offset: 0
Timestamp: 1651594080216
[main] INFO org.apache.kafka.clients.producer.KafkaProducer - [Producer clientId=producer-1] Closing the Kafka producer with timeoutMillis = 9223372036854775807 ms.
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics scheduler closed
[main] INFO org.apache.kafka.common.metrics.Metrics - Closing reporter org.apache.kafka.common.metrics.JmxReporter
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics reporters closed
[main] INFO org.apache.kafka.common.utils.AppInfoParser - App info kafka.producer for producer-1 unregistered

Resultado al ejecutar 10 mensaje consecutivos:
Esto sucede porque existe un comportamiento en el cliente de kafka llamado StickyPartitioner, que lo que hace es inteligentemente utiliza una misma particion para encolar los mensajes con el fin de mejorar el rendimiento. Realmente lo que hace es agrupar los mensajes en un mismo lote y lo envia a Kafka.

[main] INFO ProducerDemoWithCallback - I am a Kafka Producer
[main] INFO org.apache.kafka.clients.producer.ProducerConfig - ProducerConfig values: 
	acks = -1
	batch.size = 16384
	bootstrap.servers = [127.0.0.1:9092]
	buffer.memory = 33554432
	client.dns.lookup = use_all_dns_ips
	client.id = producer-1
	compression.type = none
	connections.max.idle.ms = 540000
	delivery.timeout.ms = 120000
	enable.idempotence = true
	interceptor.classes = []
	key.serializer = class org.apache.kafka.common.serialization.StringSerializer
	linger.ms = 0
	max.block.ms = 60000
	max.in.flight.requests.per.connection = 5
	max.request.size = 1048576
	metadata.max.age.ms = 300000
	metadata.max.idle.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partitioner.class = class org.apache.kafka.clients.producer.internals.DefaultPartitioner
	receive.buffer.bytes = 32768
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retries = 2147483647
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	transaction.timeout.ms = 60000
	transactional.id = null
	value.serializer = class org.apache.kafka.common.serialization.StringSerializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1651594628861
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 1
Timestamp: 1651594629348
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 2
Timestamp: 1651594629362
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 3
Timestamp: 1651594629364
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 4
Timestamp: 1651594629364
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 5
Timestamp: 1651594629365
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 6
Timestamp: 1651594629365
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 7
Timestamp: 1651594629365
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 8
Timestamp: 1651594629365
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 9
Timestamp: 1651594629365
[kafka-producer-network-thread | producer-1] INFO ProducerDemoWithCallback - Recibida nueva metadata/ 
Topic: demo_java
Partition: 1
Offset: 10
Timestamp: 1651594629365
[main] INFO org.apache.kafka.clients.producer.KafkaProducer - [Producer clientId=producer-1] Closing the Kafka producer with timeoutMillis = 9223372036854775807 ms.
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics scheduler closed
[main] INFO org.apache.kafka.common.metrics.Metrics - Closing reporter org.apache.kafka.common.metrics.JmxReporter
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics reporters closed
[main] INFO org.apache.kafka.common.utils.AppInfoParser - App info kafka.producer for producer-1 unregistered

Process finished with exit code 0

********************** 46. Java Producer with Keys ***********************

- Enviar claves no nula a el topico de kafka
- Observaremos que la clave hace que vaya a la misma partición

https://github.com/gtorres04/kafka-beginners-course/releases/tag/46_Java_Producer_with_Keys

Resultado de enviar 10 mensajes con claves diferentes cada uno:

[main] INFO ProducerDemoKeys - I am a Kafka Producer
[main] INFO org.apache.kafka.clients.producer.ProducerConfig - ProducerConfig values: 
	acks = -1
	batch.size = 16384
	bootstrap.servers = [127.0.0.1:9092]
	buffer.memory = 33554432
	client.dns.lookup = use_all_dns_ips
	client.id = producer-1
	compression.type = none
	connections.max.idle.ms = 540000
	delivery.timeout.ms = 120000
	enable.idempotence = true
	interceptor.classes = []
	key.serializer = class org.apache.kafka.common.serialization.StringSerializer
	linger.ms = 0
	max.block.ms = 60000
	max.in.flight.requests.per.connection = 5
	max.request.size = 1048576
	metadata.max.age.ms = 300000
	metadata.max.idle.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partitioner.class = class org.apache.kafka.clients.producer.internals.DefaultPartitioner
	receive.buffer.bytes = 32768
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retries = 2147483647
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	transaction.timeout.ms = 60000
	transactional.id = null
	value.serializer = class org.apache.kafka.common.serialization.StringSerializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1651597036544
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_0
Partition: 0
Offset: 11
Timestamp: 1651597036886
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_3
Partition: 0
Offset: 12
Timestamp: 1651597036899
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_4
Partition: 0
Offset: 13
Timestamp: 1651597036899
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_1
Partition: 1
Offset: 11
Timestamp: 1651597036898
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_6
Partition: 1
Offset: 12
Timestamp: 1651597036900
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_8
Partition: 1
Offset: 13
Timestamp: 1651597036900
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_2
Partition: 2
Offset: 1
Timestamp: 1651597036899
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_5
Partition: 2
Offset: 2
Timestamp: 1651597036900
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_7
Partition: 2
Offset: 3
Timestamp: 1651597036900
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_9
Partition: 2
Offset: 4
Timestamp: 1651597036901
[main] INFO org.apache.kafka.clients.producer.KafkaProducer - [Producer clientId=producer-1] Closing the Kafka producer with timeoutMillis = 9223372036854775807 ms.
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics scheduler closed
[main] INFO org.apache.kafka.common.metrics.Metrics - Closing reporter org.apache.kafka.common.metrics.JmxReporter
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics reporters closed
[main] INFO org.apache.kafka.common.utils.AppInfoParser - App info kafka.producer for producer-1 unregistered

Process finished with exit code 0

Al volver a ejecutar deberia tener el mismo resultado:

[main] INFO ProducerDemoKeys - I am a Kafka Producer
[main] INFO org.apache.kafka.clients.producer.ProducerConfig - ProducerConfig values: 
	acks = -1
	batch.size = 16384
	bootstrap.servers = [127.0.0.1:9092]
	buffer.memory = 33554432
	client.dns.lookup = use_all_dns_ips
	client.id = producer-1
	compression.type = none
	connections.max.idle.ms = 540000
	delivery.timeout.ms = 120000
	enable.idempotence = true
	interceptor.classes = []
	key.serializer = class org.apache.kafka.common.serialization.StringSerializer
	linger.ms = 0
	max.block.ms = 60000
	max.in.flight.requests.per.connection = 5
	max.request.size = 1048576
	metadata.max.age.ms = 300000
	metadata.max.idle.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partitioner.class = class org.apache.kafka.clients.producer.internals.DefaultPartitioner
	receive.buffer.bytes = 32768
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retries = 2147483647
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	transaction.timeout.ms = 60000
	transactional.id = null
	value.serializer = class org.apache.kafka.common.serialization.StringSerializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1651597299273
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_0
Partition: 0
Offset: 14
Timestamp: 1651597299638
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_3
Partition: 0
Offset: 15
Timestamp: 1651597299651
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_4
Partition: 0
Offset: 16
Timestamp: 1651597299651
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_1
Partition: 1
Offset: 14
Timestamp: 1651597299650
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_6
Partition: 1
Offset: 15
Timestamp: 1651597299652
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_8
Partition: 1
Offset: 16
Timestamp: 1651597299652
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_2
Partition: 2
Offset: 5
Timestamp: 1651597299651
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_5
Partition: 2
Offset: 6
Timestamp: 1651597299652
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_7
Partition: 2
Offset: 7
Timestamp: 1651597299652
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_9
Partition: 2
Offset: 8
Timestamp: 1651597299652
[main] INFO org.apache.kafka.clients.producer.KafkaProducer - [Producer clientId=producer-1] Closing the Kafka producer with timeoutMillis = 9223372036854775807 ms.
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics scheduler closed
[main] INFO org.apache.kafka.common.metrics.Metrics - Closing reporter org.apache.kafka.common.metrics.JmxReporter
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics reporters closed
[main] INFO org.apache.kafka.common.utils.AppInfoParser - App info kafka.producer for producer-1 unregistered

Process finished with exit code 0


********************** 47. Java Consumer ***********************

* Java API Basics

- Aprender como escribir un consumidor basico para recibir datos desde kafka
- Ver parametros de configuacion basicos
- Confirmar recibimos los datos desde un producto kafka escrito en Java.

https://github.com/gtorres04/kafka-beginners-course/releases/tag/47_Java_Consumer

Se ejecuta un consumidor:

[main] INFO ConsumerDemo - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-second-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-second-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1651600873583
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Subscribed to topic(s): demo_java
[main] INFO ConsumerDemo - Polling
[main] INFO ConsumerDemo - Polling
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Discovered group coordinator 127.0.0.1:9092 (id: 2147483647 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] (Re-)joining group
[main] INFO ConsumerDemo - Polling
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Successfully joined group with generation Generation{generationId=1, memberId='consumer-my-second-application-1-652cc133-3a76-4e98-895b-0c28cf2e6225', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Finished assignment for group at generation 1: {consumer-my-second-application-1-652cc133-3a76-4e98-895b-0c28cf2e6225=Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Successfully synced group in generation Generation{generationId=1, memberId='consumer-my-second-application-1-652cc133-3a76-4e98-895b-0c28cf2e6225', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Adding newly assigned partitions: demo_java-0, demo_java-1, demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Found no committed offset for partition demo_java-0
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Found no committed offset for partition demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Found no committed offset for partition demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.SubscriptionState - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting offset for partition demo_java-0 to position FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}.
[main] INFO org.apache.kafka.clients.consumer.internals.SubscriptionState - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting offset for partition demo_java-1 to position FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}.
[main] INFO org.apache.kafka.clients.consumer.internals.SubscriptionState - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting offset for partition demo_java-2 to position FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}.
[main] INFO ConsumerDemo - Key: null
Value: hello world
Partition: 0
Offset: 0
[main] INFO ConsumerDemo - Key: null
Value: hello world 0
Partition: 0
Offset: 1
[main] INFO ConsumerDemo - Key: null
Value: hello world 1
Partition: 0
Offset: 2
[main] INFO ConsumerDemo - Key: null
Value: hello world 2
Partition: 0
Offset: 3
[main] INFO ConsumerDemo - Key: null
Value: hello world 3
Partition: 0
Offset: 4
[main] INFO ConsumerDemo - Key: null
Value: hello world 4
Partition: 0
Offset: 5
[main] INFO ConsumerDemo - Key: null
Value: hello world 5
Partition: 0
Offset: 6
[main] INFO ConsumerDemo - Key: null
Value: hello world 6
Partition: 0
Offset: 7
[main] INFO ConsumerDemo - Key: null
Value: hello world 7
Partition: 0
Offset: 8
[main] INFO ConsumerDemo - Key: null
Value: hello world 8
Partition: 0
Offset: 9
[main] INFO ConsumerDemo - Key: null
Value: hello world 9
Partition: 0
Offset: 10
[main] INFO ConsumerDemo - Key: ID_0
Value: hello world 0
Partition: 0
Offset: 11
[main] INFO ConsumerDemo - Key: ID_3
Value: hello world 3
Partition: 0
Offset: 12
[main] INFO ConsumerDemo - Key: ID_4
Value: hello world 4
Partition: 0
Offset: 13
[main] INFO ConsumerDemo - Key: ID_0
Value: hello world 0
Partition: 0
Offset: 14
[main] INFO ConsumerDemo - Key: ID_3
Value: hello world 3
Partition: 0
Offset: 15
[main] INFO ConsumerDemo - Key: ID_4
Value: hello world 4
Partition: 0
Offset: 16
[main] INFO ConsumerDemo - Key: null
Value: hello world
Partition: 1
Offset: 0
[main] INFO ConsumerDemo - Key: null
Value: hello world 0
Partition: 1
Offset: 1
[main] INFO ConsumerDemo - Key: null
Value: hello world 1
Partition: 1
Offset: 2
[main] INFO ConsumerDemo - Key: null
Value: hello world 2
Partition: 1
Offset: 3
[main] INFO ConsumerDemo - Key: null
Value: hello world 3
Partition: 1
Offset: 4
[main] INFO ConsumerDemo - Key: null
Value: hello world 4
Partition: 1
Offset: 5
[main] INFO ConsumerDemo - Key: null
Value: hello world 5
Partition: 1
Offset: 6
[main] INFO ConsumerDemo - Key: null
Value: hello world 6
Partition: 1
Offset: 7
[main] INFO ConsumerDemo - Key: null
Value: hello world 7
Partition: 1
Offset: 8
[main] INFO ConsumerDemo - Key: null
Value: hello world 8
Partition: 1
Offset: 9
[main] INFO ConsumerDemo - Key: null
Value: hello world 9
Partition: 1
Offset: 10
[main] INFO ConsumerDemo - Key: ID_1
Value: hello world 1
Partition: 1
Offset: 11
[main] INFO ConsumerDemo - Key: ID_6
Value: hello world 6
Partition: 1
Offset: 12
[main] INFO ConsumerDemo - Key: ID_8
Value: hello world 8
Partition: 1
Offset: 13
[main] INFO ConsumerDemo - Key: ID_1
Value: hello world 1
Partition: 1
Offset: 14
[main] INFO ConsumerDemo - Key: ID_6
Value: hello world 6
Partition: 1
Offset: 15
[main] INFO ConsumerDemo - Key: ID_8
Value: hello world 8
Partition: 1
Offset: 16
[main] INFO ConsumerDemo - Key: null
Value: hello world
Partition: 2
Offset: 0
[main] INFO ConsumerDemo - Key: ID_2
Value: hello world 2
Partition: 2
Offset: 1
[main] INFO ConsumerDemo - Key: ID_5
Value: hello world 5
Partition: 2
Offset: 2
[main] INFO ConsumerDemo - Key: ID_7
Value: hello world 7
Partition: 2
Offset: 3
[main] INFO ConsumerDemo - Key: ID_9
Value: hello world 9
Partition: 2
Offset: 4
[main] INFO ConsumerDemo - Key: ID_2
Value: hello world 2
Partition: 2
Offset: 5
[main] INFO ConsumerDemo - Key: ID_5
Value: hello world 5
Partition: 2
Offset: 6
[main] INFO ConsumerDemo - Key: ID_7
Value: hello world 7
Partition: 2
Offset: 7
[main] INFO ConsumerDemo - Key: ID_9
Value: hello world 9
Partition: 2
Offset: 8
[main] INFO ConsumerDemo - Polling
[main] INFO ConsumerDemo - Polling
[main] INFO ConsumerDemo - Polling
[main] INFO ConsumerDemo - Polling

Al volver a ejecutar el mismo consumidor nos damos cuenta que no inicia desde el offset 0, sino que lo retoma por donde lo dejo en su ultima ejecucion:

[main] INFO ConsumerDemo - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-second-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-second-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1651601534730
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Subscribed to topic(s): demo_java
[main] INFO ConsumerDemo - Polling
[main] INFO ConsumerDemo - Polling
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Discovered group coordinator 127.0.0.1:9092 (id: 2147483647 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] (Re-)joining group
[main] INFO ConsumerDemo - Polling
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Successfully joined group with generation Generation{generationId=3, memberId='consumer-my-second-application-1-0a9a8a7d-eb65-4755-b271-7513bd05300d', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Finished assignment for group at generation 3: {consumer-my-second-application-1-0a9a8a7d-eb65-4755-b271-7513bd05300d=Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Successfully synced group in generation Generation{generationId=3, memberId='consumer-my-second-application-1-0a9a8a7d-eb65-4755-b271-7513bd05300d', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Adding newly assigned partitions: demo_java-0, demo_java-1, demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Setting offset for partition demo_java-0 to the committed offset FetchPosition{offset=17, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=17, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-second-application-1, groupId=my-second-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=9, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}
[main] INFO ConsumerDemo - Polling
[main] INFO ConsumerDemo - Polling
[main] INFO ConsumerDemo - Polling

********************** 48. Java Consumer - Graceful Shutdown ***********************

- Asegurarnos que nuestro codigo responda a la señal de terminacion.
- Mejorar nuestro codigo Java para cerrar correctamente un consumidor

[main] INFO ConsumerDemoWithShutdown - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1652193960469
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Node -1 disconnected.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Connection to node -1 (/127.0.0.1:9092) could not be established. Broker may not be available.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Bootstrap broker 127.0.0.1:9092 (id: -1 rack: null) disconnected
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Node -1 disconnected.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Connection to node -1 (/127.0.0.1:9092) could not be established. Broker may not be available.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Bootstrap broker 127.0.0.1:9092 (id: -1 rack: null) disconnected
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Node -1 disconnected.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Connection to node -1 (/127.0.0.1:9092) could not be established. Broker may not be available.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Bootstrap broker 127.0.0.1:9092 (id: -1 rack: null) disconnected
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Node -1 disconnected.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Connection to node -1 (/127.0.0.1:9092) could not be established. Broker may not be available.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Bootstrap broker 127.0.0.1:9092 (id: -1 rack: null) disconnected
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Node -1 disconnected.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Connection to node -1 (/127.0.0.1:9092) could not be established. Broker may not be available.
[main] WARN org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Bootstrap broker 127.0.0.1:9092 (id: -1 rack: null) disconnected
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[main] INFO ConsumerDemoWithShutdown - Polling
[Thread-0] INFO ConsumerDemoWithShutdown - Detectado un apagado, salgamos mediante el llamado a concumer.wakerup()...
[main] INFO ConsumerDemoWithShutdown - Wake up exception!
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting generation due to: consumer pro-actively leaving the group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: consumer pro-actively leaving the group
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics scheduler closed
[main] INFO org.apache.kafka.common.metrics.Metrics - Closing reporter org.apache.kafka.common.metrics.JmxReporter
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics reporters closed
[main] INFO org.apache.kafka.common.utils.AppInfoParser - App info kafka.consumer for consumer-my-third-application-1 unregistered
[main] INFO ConsumerDemoWithShutdown - El consumidor esta ahora elegantemente cerrado

Process finished with exit code 1

************************** 49. Java Consumer inside Consumer Group **************************

KAFKA CONSUMER: JAVA API - CONSUMER GROUPS

- Hacer que nuestro consumidor en Java, consuma datos como parte de un grupo de consumidores.
- Observar el mecanismo de rebalanceo

+ Se ejecuta un primer consumidor

[main] INFO ConsumerDemoWithShutdown - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1652270951313
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9092 (id: 2147483647 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=7, memberId='consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 7: {consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca=Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=7, memberId='consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0, demo_java-1, demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-0 to the committed offset FetchPosition{offset=17, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=17, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=9, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}

Al unirse al grupo un segundo consumidor, los logs de consumidor se actualizan a:

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-0, demo_java-1, demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=8, memberId='consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 8: {consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195=Assignment(partitions=[demo_java-0, demo_java-1]), consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca=Assignment(partitions=[demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=8, memberId='consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=9, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}

Al agregarse al grupo un tercer consumidor se pintan los siguientes logs:

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=9, memberId='consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 9: {consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195=Assignment(partitions=[demo_java-0]), consumer-my-third-application-1-5c5cd250-f3cf-48ba-846f-fb230d1cd0d3=Assignment(partitions=[demo_java-2]), consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca=Assignment(partitions=[demo_java-1])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=9, memberId='consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=17, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}

+ Se ejecuta un segundo consumidor

/usr/lib/jvm/java-1.11.0-openjdk-amd64/bin/java -javaagent:/opt/intellij-idea-community/lib/idea_rt.jar=36055:/opt/intellij-idea-community/bin -Dfile.encoding=UTF-8 -classpath /home/gotorres/Escritorio/CAPACITACION/Kafka/ Apache Kafka Series - Learn Apache Kafka for Beginners v3/resources/seccion9/kafka-beginners-course/kafka-basics/out/production/classes:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.apache.kafka/kafka-clients/3.1.0/af924560e38c0a6dbf270bc2d361b2dfab0e03ec/kafka-clients-3.1.0.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.slf4j/slf4j-simple/1.7.36/a41f9cfe6faafb2eb83a1c7dd2d0dfd844e2a936/slf4j-simple-1.7.36.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.slf4j/slf4j-api/1.7.36/6c62681a2f655b49963a5983b8b0950a6120ae14/slf4j-api-1.7.36.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/com.github.luben/zstd-jni/1.5.0-4/338d83645fb93afc9e8b38a12d9d16d41d0819b3/zstd-jni-1.5.0-4.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.lz4/lz4-java/1.8.0/4b986a99445e49ea5fbf5d149c4b63f6ed6c6780/lz4-java-1.8.0.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.xerial.snappy/snappy-java/1.1.8.4/66f0d56454509f6e36175f2331572e250e04a6cc/snappy-java-1.1.8.4.jar io.conduktor.demos.kafka.ConsumerDemoWithShutdown
[main] INFO ConsumerDemoWithShutdown - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1652271016385
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9092 (id: 2147483647 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=8, memberId='consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=8, memberId='consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0, demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-0 to the committed offset FetchPosition{offset=17, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=17, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}

Al agregarse al grupo un tercer consumidor se pintan los siguientes logs:

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-0, demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=9, memberId='consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=9, memberId='consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-0 to the committed offset FetchPosition{offset=17, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}


+ Se ejecuta un tercer consumidor

/usr/lib/jvm/java-1.11.0-openjdk-amd64/bin/java -javaagent:/opt/intellij-idea-community/lib/idea_rt.jar=33737:/opt/intellij-idea-community/bin -Dfile.encoding=UTF-8 -classpath /home/gotorres/Escritorio/CAPACITACION/Kafka/ Apache Kafka Series - Learn Apache Kafka for Beginners v3/resources/seccion9/kafka-beginners-course/kafka-basics/out/production/classes:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.apache.kafka/kafka-clients/3.1.0/af924560e38c0a6dbf270bc2d361b2dfab0e03ec/kafka-clients-3.1.0.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.slf4j/slf4j-simple/1.7.36/a41f9cfe6faafb2eb83a1c7dd2d0dfd844e2a936/slf4j-simple-1.7.36.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.slf4j/slf4j-api/1.7.36/6c62681a2f655b49963a5983b8b0950a6120ae14/slf4j-api-1.7.36.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/com.github.luben/zstd-jni/1.5.0-4/338d83645fb93afc9e8b38a12d9d16d41d0819b3/zstd-jni-1.5.0-4.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.lz4/lz4-java/1.8.0/4b986a99445e49ea5fbf5d149c4b63f6ed6c6780/lz4-java-1.8.0.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.xerial.snappy/snappy-java/1.1.8.4/66f0d56454509f6e36175f2331572e250e04a6cc/snappy-java-1.1.8.4.jar io.conduktor.demos.kafka.ConsumerDemoWithShutdown
[main] INFO ConsumerDemoWithShutdown - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1652272130805
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9092 (id: 2147483647 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=9, memberId='consumer-my-third-application-1-5c5cd250-f3cf-48ba-846f-fb230d1cd0d3', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=9, memberId='consumer-my-third-application-1-5c5cd250-f3cf-48ba-846f-fb230d1cd0d3', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=9, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}

Como se puede apreciar se rebalancean las particiones asignadas a cada consumidor
- Al agregar al grupo el primer consumidor las tres particiones del topico fueron asignadas a unico consumidor
- Al agregar al grupo el segundo consumidor, las 3 particiones del topico fueron asignadas asi:
	- Consumidor 1: partitions=[demo_java-2]
	- Consumidor 2: partitions=[demo_java-0, demo_java-1]
- Al agregar al grupo el tercer consumidor, las 3 particiones del topico fueron asignadas asi:
	- Consumidor 1: partitions=[demo_java-1]
	- Consumidor 1: partitions=[demo_java-0]
	- Consumidor 1: partitions=[demo_java-2]

Al ejecutar un productor con Claves ProductorDemoKeys.java, revisemos los mensajes consumidos por los consumidores:

Productor:

/usr/lib/jvm/java-1.11.0-openjdk-amd64/bin/java -javaagent:/opt/intellij-idea-community/lib/idea_rt.jar=36163:/opt/intellij-idea-community/bin -Dfile.encoding=UTF-8 -classpath /home/gotorres/Escritorio/CAPACITACION/Kafka/ Apache Kafka Series - Learn Apache Kafka for Beginners v3/resources/seccion9/kafka-beginners-course/kafka-basics/out/production/classes:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.apache.kafka/kafka-clients/3.1.0/af924560e38c0a6dbf270bc2d361b2dfab0e03ec/kafka-clients-3.1.0.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.slf4j/slf4j-simple/1.7.36/a41f9cfe6faafb2eb83a1c7dd2d0dfd844e2a936/slf4j-simple-1.7.36.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.slf4j/slf4j-api/1.7.36/6c62681a2f655b49963a5983b8b0950a6120ae14/slf4j-api-1.7.36.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/com.github.luben/zstd-jni/1.5.0-4/338d83645fb93afc9e8b38a12d9d16d41d0819b3/zstd-jni-1.5.0-4.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.lz4/lz4-java/1.8.0/4b986a99445e49ea5fbf5d149c4b63f6ed6c6780/lz4-java-1.8.0.jar:/home/gotorres/.gradle/caches/modules-2/files-2.1/org.xerial.snappy/snappy-java/1.1.8.4/66f0d56454509f6e36175f2331572e250e04a6cc/snappy-java-1.1.8.4.jar io.conduktor.demos.kafka.ProducerDemoKeys
[main] INFO ProducerDemoKeys - I am a Kafka Producer
[main] INFO org.apache.kafka.clients.producer.ProducerConfig - ProducerConfig values: 
	acks = -1
	batch.size = 16384
	bootstrap.servers = [127.0.0.1:9092]
	buffer.memory = 33554432
	client.dns.lookup = use_all_dns_ips
	client.id = producer-1
	compression.type = none
	connections.max.idle.ms = 540000
	delivery.timeout.ms = 120000
	enable.idempotence = true
	interceptor.classes = []
	key.serializer = class org.apache.kafka.common.serialization.StringSerializer
	linger.ms = 0
	max.block.ms = 60000
	max.in.flight.requests.per.connection = 5
	max.request.size = 1048576
	metadata.max.age.ms = 300000
	metadata.max.idle.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partitioner.class = class org.apache.kafka.clients.producer.internals.DefaultPartitioner
	receive.buffer.bytes = 32768
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retries = 2147483647
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	transaction.timeout.ms = 60000
	transactional.id = null
	value.serializer = class org.apache.kafka.common.serialization.StringSerializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1652272621941
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to FhDdAAqYRe-suzogvcmOmw
[kafka-producer-network-thread | producer-1] INFO org.apache.kafka.clients.Metadata - [Producer clientId=producer-1] Cluster ID: qacydFJ1Q1iwULM3BwB4Ew
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_0
Partition: 0
Offset: 17
Timestamp: 1652272622255
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_3
Partition: 0
Offset: 18
Timestamp: 1652272622267
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_4
Partition: 0
Offset: 19
Timestamp: 1652272622267
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_1
Partition: 1
Offset: 17
Timestamp: 1652272622266
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_6
Partition: 1
Offset: 18
Timestamp: 1652272622267
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_8
Partition: 1
Offset: 19
Timestamp: 1652272622268
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_2
Partition: 2
Offset: 9
Timestamp: 1652272622267
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_5
Partition: 2
Offset: 10
Timestamp: 1652272622267
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_7
Partition: 2
Offset: 11
Timestamp: 1652272622268
[kafka-producer-network-thread | producer-1] INFO ProducerDemoKeys - Recibida nueva metadata/ 
Topic: demo_java
Key: ID_9
Partition: 2
Offset: 12
Timestamp: 1652272622268
[main] INFO org.apache.kafka.clients.producer.KafkaProducer - [Producer clientId=producer-1] Closing the Kafka producer with timeoutMillis = 9223372036854775807 ms.
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics scheduler closed
[main] INFO org.apache.kafka.common.metrics.Metrics - Closing reporter org.apache.kafka.common.metrics.JmxReporter
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics reporters closed
[main] INFO org.apache.kafka.common.utils.AppInfoParser - App info kafka.producer for producer-1 unregistered

Process finished with exit code 0


Consumidor 1:

[main] INFO ConsumerDemoWithShutdown - Key: ID_1
Value: hello world 1
Partition: 1
Offset: 17
[main] INFO ConsumerDemoWithShutdown - Key: ID_6
Value: hello world 6
Partition: 1
Offset: 18
[main] INFO ConsumerDemoWithShutdown - Key: ID_8
Value: hello world 8
Partition: 1
Offset: 19

Consumidor 2:

[main] INFO ConsumerDemoWithShutdown - Key: ID_0
Value: hello world 0
Partition: 0
Offset: 17
[main] INFO ConsumerDemoWithShutdown - Key: ID_3
Value: hello world 3
Partition: 0
Offset: 18
[main] INFO ConsumerDemoWithShutdown - Key: ID_4
Value: hello world 4
Partition: 0
Offset: 19

Consumidor 3:

[main] INFO ConsumerDemoWithShutdown - Key: ID_2
Value: hello world 2
Partition: 2
Offset: 9
[main] INFO ConsumerDemoWithShutdown - Key: ID_5
Value: hello world 5
Partition: 2
Offset: 10
[main] INFO ConsumerDemoWithShutdown - Key: ID_7
Value: hello world 7
Partition: 2
Offset: 11
[main] INFO ConsumerDemoWithShutdown - Key: ID_9
Value: hello world 9
Partition: 2
Offset: 12
[main] INFO org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Node -1 disconnected.

Ahora si un consumidor se sale del grupo, por ejemplo el consumidor 3:

Consumidor 3:

[Thread-0] INFO ConsumerDemoWithShutdown - Detectado un apagado, salgamos mediante el llamado a concumer.wakerup()...
[main] INFO ConsumerDemoWithShutdown - Wake up exception!
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Member consumer-my-third-application-1-5c5cd250-f3cf-48ba-846f-fb230d1cd0d3 sending LeaveGroup request to coordinator 127.0.0.1:9092 (id: 2147483647 rack: null) due to the consumer is being closed
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting generation due to: consumer pro-actively leaving the group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: consumer pro-actively leaving the group
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics scheduler closed
[main] INFO org.apache.kafka.common.metrics.Metrics - Closing reporter org.apache.kafka.common.metrics.JmxReporter
[main] INFO org.apache.kafka.common.metrics.Metrics - Metrics reporters closed
[main] INFO org.apache.kafka.common.utils.AppInfoParser - App info kafka.consumer for consumer-my-third-application-1 unregistered
[main] INFO ConsumerDemoWithShutdown - El consumidor esta ahora elegantemente cerrado

Process finished with exit code 1

Consumidor 1:

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=10, memberId='consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 10: {consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195=Assignment(partitions=[demo_java-0, demo_java-1]), consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca=Assignment(partitions=[demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=10, memberId='consumer-my-third-application-1-4f0f491b-e4db-4320-94a8-363e620bc2ca', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=13, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}

Consumidor 2: 

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-0
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=10, memberId='consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=10, memberId='consumer-my-third-application-1-3cc6c547-dc4f-46e3-bbd3-846832910195', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0, demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-0 to the committed offset FetchPosition{offset=20, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=20, offsetEpoch=Optional[0], currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 0 rack: null)], epoch=0}}

Como se aprecia se vuelve a rebalancear las particiones del topico en los consumidores activos del grupo.


************************** 50. Java Consumer Incremental Cooperative Rebalance & Static Group Membership **************************

CONSUMER GROUPS AND PARTITION REBALANCE

- Mover particiones entre consumidores es conocido como REBALANCEO
- La reasignacion de particiones pasa cuando un consumidor sale o entra a un grupo.
- La reasignacion de particiones pasa cuando un administrador agrego una particion a un topico.

REBALANCEO ENTUSIASTA (Eager Rebalance)

- Es el comportamiento por defecto
- Todos los consumidores paran de consumir mensajes y renuncian a su membresia de particiones, esto quiere decir que ningun consumidor esta leyendo desde ninguna partición. 
- Luego todos los consumidores volveran a unirse al grupo en el que estaban y obtendran nuevas asignaciones de partición. Esto quiere decir que a todos estos consumidores ahora se les asignaran nuevas particiones
- Durante un corto periodo de tiempo, todo el grupo de consumidores dejo de procesar mensajes. Esto se llama el evento de detener el mundo.
- No hay garantia que sus consumidores vayan a recuperar las particiones que solian tener.

Entonces existen dos problemas:
1. Tal vez desee que sus consumidores vuelvan a recuperar las particiones que solian tener.
2. Tal vez no desee que algunos consumidores dejen de consumir si estaban leyendo desde la misma partición. No quieres que esto detenga la lectura de mensajes.

COOPERATIVE REBALANCE (Incremental Rebalance)

- En lugar de reasignar todas las particiones a todos los consumidores, la estrategia es reasignar pequeños subconjuntos de las particiones de un consumidor a otro.
- Los consumidores que tienen particiones asignadas aun pueden procesar los datos sin interrupciones. Hasta encontrar una asignacion estable sin desasignar el resto de comsumidores pueden pasar por muchas iteraciones.

COOPERATIVE REBALANCE ¿COMO SE UTILIZA?

- En kafka consumer existe una configuracion llamada estrategia de asignacion de particion (partition.assignment.strategy)
	- Las primeras 3 estrategias configurables (partition.assignment.strategy) son de caracter ansiosa, eso quiere decir que  cada vez que las use, habra un evento de parada mundial y solo rompera su grupo de consumidores por pocos segundos, y si el grupo de consumidores es grande, puede llevar un tiempo reasignar todas las particiones:
		- RangeAssinor: Su valor predeterminado, que asigna la particion por tema y puede provocar un desequilibrio.
		- RoundRobin: Tambien es un tipo ansioso de asignacion y todas las particiones de todos los temas se asignan de forma rotativa, lo que es realmente para el equilibrio ya que todos los consumidores tendran mas o menos el mismo numero de particiones.
		- StickyAssignor: Rebalancea como RoundRobin al principio, y luego minimizara los movimientos de particion cuando un consumidor se una o banadone el grupo para minimizar los movimientos.
		- CooperativeStickyAssignor: La estrategia de rebalance es identica a StickyAssignor pero suporta el rebalanceo cooperativo, por lo tanto los consumidores pueden mantener leyendo desde el topico siempre.
		- The default assignor is [RangeAssignor, CooperativeStickyAssignor]: El cual usa el RangeAssignor por defecto, pero permite actualizar a el CooperativeStickyAssignor con solo rebote rodante (Rolling Bounce) que remueba el RangeAssignor desde la lista.
- En kafka Connect: kafka connect es el equilibrio cooperativo (Cooperative Rebalance).
- Kafka Streams: Se activa de manera preterminada usando StreamsPartitionAssignor.

STATIC GROUP MEMBERSHIP (Ser miembro de un grupo estatico)

Hemos visto que cada vez que los consumidores se unen o abandonan el grupo, se activa un rebalanceo, ya que kafka dice, que necesitamos que todos los consumidores lean absolutamente todas las particiones, pero primero es todo para que usted diga, cuando un consumidor
se va entonces no cambie las asignaciones. Entonces, la razon por la que primero, cuando se va y regresa hay una reasignacion y es que obtiene una nueva identificacion de miembro, porque se va y cuando luego se registra kafka le da una nueva identificacion de miembro.

Pero si especifica un ID de instancia de grupo como parte de la configuracion del consumidor, entonces convierte al consumidor en un miembro estatico y debe averiguar que desea poner en esta configuracion. Pero lo que pasa es que si, por ejemplo, tienes 3 consumidores con ID diferentes, si un consumidor sale del grupo la particion no se reasignara a otro consumidor y esta particion esperara al consumidor que se reconecte, el tiempo de espera de la particion la determinara el parametro session.timeout.ms.

## 51. Java Consumer Incremental Cooperative Rebalance - Practice 

* Se crea un topico llamado demo_java

```
gerlinorlandotorres@MacBook-Pro-de-Gerlin kafka-stack-docker-compose % kafka-topics --bootstrap-server localhost:9092 --topic demo_java --create --partitions 3 --replication-factor 2
WARNING: Due to limitations in metric names, topics with a period ('.') or underscore ('_') could collide. To avoid issues it is best to use either, but not both.
Created topic demo_java.
gerlinorlandotorres@MacBook-Pro-de-Gerlin kafka-stack-docker-compose % kafka-topics --bootstrap-server localhost:9092 --topic demo_java --describe                                    
Topic: demo_java        TopicId: EV3ubJdsSyiw2e0S1ClvBQ PartitionCount: 3       ReplicationFactor: 2    Configs: 
        Topic: demo_java        Partition: 0    Leader: 2       Replicas: 2,1   Isr: 2,1
        Topic: demo_java        Partition: 1    Leader: 3       Replicas: 3,2   Isr: 3,2
        Topic: demo_java        Partition: 2    Leader: 1       Replicas: 1,3   Isr: 1,3
```
* Se ejecuta un consumidor con las siguientes caracteristicas (ConsumerDemoCooperative.java)
```
package io.conduktor.demos.kafka;

import org.apache.kafka.clients.consumer.ConsumerRecords;
import org.apache.kafka.clients.consumer.KafkaConsumer;
import org.apache.kafka.clients.consumer.OffsetResetStrategy;
import org.apache.kafka.common.errors.WakeupException;
import org.apache.kafka.common.serialization.StringDeserializer;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;

import java.time.Duration;
import java.util.Collections;
import java.util.Properties;

import static org.apache.kafka.clients.consumer.ConsumerConfig.*;

public class ConsumerDemoCooperative {

    private static final Logger log = LoggerFactory.getLogger(ConsumerDemoCooperative.class.getSimpleName());

    public static void main(String[] args) {
        log.info("I am a Kafka Consumer");

        // Crear las propiedades del consumidor
        Properties properties = new Properties();
        properties.setProperty(BOOTSTRAP_SERVERS_CONFIG, "127.0.0.1:9092"); // IP y PUERTO del servidor de Kafka
        properties.setProperty(KEY_DESERIALIZER_CLASS_CONFIG, StringDeserializer.class.getName()); // Deserializador de la clave del mensaje a recibir
        properties.setProperty(VALUE_DESERIALIZER_CLASS_CONFIG, StringDeserializer.class.getName()); // Deserializador del valor del mensaje a recibir
        properties.setProperty(GROUP_ID_CONFIG, "my-third-application"); // ID del grupo al que pertenecera el consumidor
        properties.setProperty(AUTO_OFFSET_RESET_CONFIG, OffsetResetStrategy.EARLIEST.name().toLowerCase()); // Desde donde iniciara la lectura de los mensajes en base al offset

        // Crear el consumidor
        KafkaConsumer<String, String> consumer = new KafkaConsumer<>(properties);

        // obtengo una referencia al hilo de ejecucion actual
        final Thread mainThread = Thread.currentThread();

        // Adicionando el hook de apagado
        Runtime.getRuntime().addShutdownHook(new Thread(() -> {
            log.info("Detectado un apagado, salgamos mediante el llamado a concumer.wakerup()...");
            consumer.wakeup();

            // Unir el hilo principal para permitir la ejecucion de el codigo en el hilo principal
            try {
                mainThread.join();
            } catch (InterruptedException e) {
                throw new RuntimeException(e);
            }
        }));

        try {
            // Subscribir el consumidor a nuestro topico
            consumer.subscribe(Collections.singleton("demo_java"));

            // Sondear para obtener nuevos datos
            while (true) {
                ConsumerRecords<String, String> consumerRecords = consumer.poll(Duration.ofMillis(100));
                consumerRecords.forEach(consumerRecord -> log.info("Key: {}\n" +
                        "Value: {}\n" +
                        "Partition: {}\n" +
                        "Offset: {}", consumerRecord.key(), consumerRecord.value(), consumerRecord.partition(), consumerRecord.offset()));
            }
        } catch (WakeupException wakeupException) {
            log.info("Wake up exception!");
            // Ignoramos esto por lo que es una exception esperada cuando se cierra un consumidor
        } catch (Exception exception) {
            log.error("Error inesperado: {}", exception.toString());
        } finally {
            consumer.close(); // Esto ademas confirmara los offsets si es necesario
            log.info("El consumidor esta ahora elegantemente cerrado");
        }
    }
}

```
Resultado de la ejecucion
```
12:11:21: Executing ':kafka-basics:ConsumerDemoCooperative.main()'...

> Task :kafka-basics:compileJava UP-TO-DATE
> Task :kafka-basics:processResources NO-SOURCE
> Task :kafka-basics:classes UP-TO-DATE

> Task :kafka-basics:ConsumerDemoCooperative.main()
[main] INFO ConsumerDemoCooperative - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1655979082452
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: haCR281HQJa46xeRJyL1cg
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9094 (id: 2147483644 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=1, memberId='consumer-my-third-application-1-c54e0465-d146-4c18-80d5-b9a67c787c24', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 1: {consumer-my-third-application-1-c54e0465-d146-4c18-80d5-b9a67c787c24=Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=1, memberId='consumer-my-third-application-1-c54e0465-d146-4c18-80d5-b9a67c787c24', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0, demo_java-1, demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Found no committed offset for partition demo_java-0
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Found no committed offset for partition demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Found no committed offset for partition demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.SubscriptionState - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting offset for partition demo_java-0 to position FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9093 (id: 2 rack: null)], epoch=0}}.
[main] INFO org.apache.kafka.clients.consumer.internals.SubscriptionState - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting offset for partition demo_java-1 to position FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9094 (id: 3 rack: null)], epoch=0}}.
[main] INFO org.apache.kafka.clients.consumer.internals.SubscriptionState - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting offset for partition demo_java-2 to position FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 1 rack: null)], epoch=0}}.
```
Se asignan las tres particiones del topico a este consumidor
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0, demo_java-1, demo_java-2
```
* Se ejecuta un segundo consumidor con las caracteristicas del anterior (ConsumerDemoCooperative.java), teniendo como resultado al ejeuctarlo
```
12:21:57: Executing ':kafka-basics:ConsumerDemoCooperative.main()'...

Starting Gradle Daemon...
Gradle Daemon started in 927 ms
> Task :kafka-basics:compileJava UP-TO-DATE
> Task :kafka-basics:processResources NO-SOURCE
> Task :kafka-basics:classes UP-TO-DATE

> Task :kafka-basics:ConsumerDemoCooperative.main()
[main] INFO ConsumerDemoCooperative - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1655979723132
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 0 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 0 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 0 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: haCR281HQJa46xeRJyL1cg
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9094 (id: 2147483644 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=2, memberId='consumer-my-third-application-1-67e1e1b3-d1aa-4833-9a0f-8a9f917f38a0', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=2, memberId='consumer-my-third-application-1-67e1e1b3-d1aa-4833-9a0f-8a9f917f38a0', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0, demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-0 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9093 (id: 2 rack: null)], epoch=0}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9094 (id: 3 rack: null)], epoch=0}}
```
A este segundo consumidor se le asignan 2 particiones de las 3 que tenia anteriormente:
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0, demo_java-1
```
Revisemos que paso con el primer consumidor
```
[main] INFO org.apache.kafka.clients.NetworkClient - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Node -1 disconnected.
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-0, demo_java-1, demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=2, memberId='consumer-my-third-application-1-c54e0465-d146-4c18-80d5-b9a67c787c24', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 2: {consumer-my-third-application-1-67e1e1b3-d1aa-4833-9a0f-8a9f917f38a0=Assignment(partitions=[demo_java-0, demo_java-1]), consumer-my-third-application-1-c54e0465-d146-4c18-80d5-b9a67c787c24=Assignment(partitions=[demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=2, memberId='consumer-my-third-application-1-c54e0465-d146-4c18-80d5-b9a67c787c24', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 1 rack: null)], epoch=0}}
```
El primer consumidor quedo con una sola particion tal y como lo muestran las lineas
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 2: {consumer-my-third-application-1-67e1e1b3-d1aa-4833-9a0f-8a9f917f38a0=Assignment(partitions=[demo_java-0, demo_java-1]), consumer-my-third-application-1-c54e0465-d146-4c18-80d5-b9a67c787c24=Assignment(partitions=[demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=2, memberId='consumer-my-third-application-1-c54e0465-d146-4c18-80d5-b9a67c787c24', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-2
```
* Ejecutemos un tercer consumidor

```
12:37:38: Executing ':kafka-basics:ConsumerDemoCooperative.main()'...

Starting Gradle Daemon...
Gradle Daemon started in 924 ms
> Task :kafka-basics:compileJava UP-TO-DATE
> Task :kafka-basics:processResources NO-SOURCE
> Task :kafka-basics:classes UP-TO-DATE

> Task :kafka-basics:ConsumerDemoCooperative.main()
[main] INFO ConsumerDemoCooperative - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1655980663690
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 1 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 4 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 3 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: haCR281HQJa46xeRJyL1cg
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9094 (id: 2147483644 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=4, memberId='consumer-my-third-application-1-bd86764e-2b76-4dd0-b809-383e84154c52', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=4, memberId='consumer-my-third-application-1-bd86764e-2b76-4dd0-b809-383e84154c52', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 1 rack: null)], epoch=4}}
```
Revisemos que paso con el consumidor 2
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-0, demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=4, memberId='consumer-my-third-application-1-43a8acc5-2315-4400-871b-1a045e7b9829', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=4, memberId='consumer-my-third-application-1-43a8acc5-2315-4400-871b-1a045e7b9829', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-0 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9093 (id: 2 rack: null)], epoch=1}}
```
El consumidor 2 quedo con una sola particion
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0
```

Revisemos el consumidor 1
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=4, memberId='consumer-my-third-application-1-523ab3cc-a184-451e-bfa2-595e1f70a2dc', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 4: {consumer-my-third-application-1-bd86764e-2b76-4dd0-b809-383e84154c52=Assignment(partitions=[demo_java-2]), consumer-my-third-application-1-523ab3cc-a184-451e-bfa2-595e1f70a2dc=Assignment(partitions=[demo_java-1]), consumer-my-third-application-1-43a8acc5-2315-4400-871b-1a045e7b9829=Assignment(partitions=[demo_java-0])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=4, memberId='consumer-my-third-application-1-523ab3cc-a184-451e-bfa2-595e1f70a2dc', protocol='range'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9094 (id: 3 rack: null)], epoch=3}}
```
El consumidor 1 cambio de tener la particion 2 a tener la 1 en este rebalanceo
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-1
```
CONLUSION DEL REBALANCEO: Efectivamente los consumidores en cada rebalanceo de particiones son afectados, ya que en cada rebalanceo kafka puede que les asigne particiones diferentes a las que tenia anteriormente, y por tanto sucede lo que se conoce DETENER EL MUNDO.

## Solucion al problema (DETENER EL MUNDO)

Anteriormente al ejecutar los consumidores podiamos ver la estrategia de asgnacion (Rebalanceo) a la que obedecian
Consumidor 1,2 y 3 obedecian a 2 estrategias, dandole prioridad al parecer a la primera (org.apache.kafka.clients.consumer.RangeAssignor)
```
...
partition.assignment.strategy = [class org.apache.kafka.clients.consumer.RangeAssignor, class org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
...
```
Lo que vamos hacer es solo dejar esta `org.apache.kafka.clients.consumer.CooperativeStickyAssignor` y revisemos que sucede al ejecutar nuevamente 3 consumidores. Antes que nada debemos agregar una propiedad al consumidor que lo configure obedeciendo a solo dicha estrategia
```
properties.setProperty(PARTITION_ASSIGNMENT_STRATEGY_CONFIG, CooperativeStickyAssignor.class.getName()); // Especifica solo una estrategia de asignacion o rebalanceo
```
Ejecutemos el consumidor 1
```
13:00:34: Executing ':kafka-basics:ConsumerDemoCooperative.main()'...

> Task :kafka-basics:compileJava
> Task :kafka-basics:processResources NO-SOURCE
> Task :kafka-basics:classes

> Task :kafka-basics:ConsumerDemoCooperative.main()
[main] INFO ConsumerDemoCooperative - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1655982035937
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 1 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 4 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 3 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: haCR281HQJa46xeRJyL1cg
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9094 (id: 2147483644 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=8, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.AbstractStickyAssignor - Final assignment of partitions to consumers: 
{consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=[demo_java-0, demo_java-1, demo_java-2]}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 8: {consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=8, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-0, demo_java-1, demo_java-2]
	Current owned partitions:                  []
	Added partitions (assigned - owned):       [demo_java-0, demo_java-1, demo_java-2]
	Revoked partitions (owned - assigned):     []

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1, demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-0, demo_java-1, demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-0 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9093 (id: 2 rack: null)], epoch=1}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9094 (id: 3 rack: null)], epoch=3}}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 1 rack: null)], epoch=4}}
```
Ejecutemos el consumidor 2:
```
13:01:45: Executing ':kafka-basics:ConsumerDemoCooperative.main()'...

Starting Gradle Daemon...
Gradle Daemon started in 933 ms
> Task :kafka-basics:compileJava UP-TO-DATE
> Task :kafka-basics:processResources NO-SOURCE
> Task :kafka-basics:classes UP-TO-DATE

> Task :kafka-basics:ConsumerDemoCooperative.main()
[main] INFO ConsumerDemoCooperative - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1655982111474
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 1 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 4 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 3 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: haCR281HQJa46xeRJyL1cg
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9094 (id: 2147483644 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=9, memberId='consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=9, memberId='consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       []
	Current owned partitions:                  []
	Added partitions (assigned - owned):       []
	Revoked partitions (owned - assigned):     []

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: 
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=10, memberId='consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=10, memberId='consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-2]
	Current owned partitions:                  []
	Added partitions (assigned - owned):       [demo_java-2]
	Revoked partitions (owned - assigned):     []

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-2 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9092 (id: 1 rack: null)], epoch=4}}
```

Revisemos el consumidor 1
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=9, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.AbstractStickyAssignor - Final assignment of partitions to consumers: 
{consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b=[demo_java-2], consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=[demo_java-0, demo_java-1]}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 9: {consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b=Assignment(partitions=[]), consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=Assignment(partitions=[demo_java-0, demo_java-1])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=9, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-0, demo_java-1]
	Current owned partitions:                  [demo_java-0, demo_java-1, demo_java-2]
	Added partitions (assigned - owned):       []
	Revoked partitions (owned - assigned):     [demo_java-2]

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-2
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to revoke partitions [demo_java-2] as indicated by the current assignment and re-join
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: 
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=10, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.AbstractStickyAssignor - Final assignment of partitions to consumers: 
{consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b=[demo_java-2], consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=[demo_java-0, demo_java-1]}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 10: {consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b=Assignment(partitions=[demo_java-2]), consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=Assignment(partitions=[demo_java-0, demo_java-1])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=10, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-0, demo_java-1]
	Current owned partitions:                  [demo_java-0, demo_java-1]
	Added partitions (assigned - owned):       []
	Revoked partitions (owned - assigned):     []

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: 
```
* Ejecutemos el consumidor 3
```
13:03:44: Executing ':kafka-basics:ConsumerDemoCooperative.main()'...

Starting Gradle Daemon...
Gradle Daemon started in 939 ms
> Task :kafka-basics:compileJava UP-TO-DATE
> Task :kafka-basics:processResources NO-SOURCE
> Task :kafka-basics:classes UP-TO-DATE

> Task :kafka-basics:ConsumerDemoCooperative.main()
[main] INFO ConsumerDemoCooperative - I am a Kafka Consumer
[main] INFO org.apache.kafka.clients.consumer.ConsumerConfig - ConsumerConfig values: 
	allow.auto.create.topics = true
	auto.commit.interval.ms = 5000
	auto.offset.reset = earliest
	bootstrap.servers = [127.0.0.1:9092]
	check.crcs = true
	client.dns.lookup = use_all_dns_ips
	client.id = consumer-my-third-application-1
	client.rack = 
	connections.max.idle.ms = 540000
	default.api.timeout.ms = 60000
	enable.auto.commit = true
	exclude.internal.topics = true
	fetch.max.bytes = 52428800
	fetch.max.wait.ms = 500
	fetch.min.bytes = 1
	group.id = my-third-application
	group.instance.id = null
	heartbeat.interval.ms = 3000
	interceptor.classes = []
	internal.leave.group.on.close = true
	internal.throw.on.fetch.stable.offset.unsupported = false
	isolation.level = read_uncommitted
	key.deserializer = class org.apache.kafka.common.serialization.StringDeserializer
	max.partition.fetch.bytes = 1048576
	max.poll.interval.ms = 300000
	max.poll.records = 500
	metadata.max.age.ms = 300000
	metric.reporters = []
	metrics.num.samples = 2
	metrics.recording.level = INFO
	metrics.sample.window.ms = 30000
	partition.assignment.strategy = [org.apache.kafka.clients.consumer.CooperativeStickyAssignor]
	receive.buffer.bytes = 65536
	reconnect.backoff.max.ms = 1000
	reconnect.backoff.ms = 50
	request.timeout.ms = 30000
	retry.backoff.ms = 100
	sasl.client.callback.handler.class = null
	sasl.jaas.config = null
	sasl.kerberos.kinit.cmd = /usr/bin/kinit
	sasl.kerberos.min.time.before.relogin = 60000
	sasl.kerberos.service.name = null
	sasl.kerberos.ticket.renew.jitter = 0.05
	sasl.kerberos.ticket.renew.window.factor = 0.8
	sasl.login.callback.handler.class = null
	sasl.login.class = null
	sasl.login.connect.timeout.ms = null
	sasl.login.read.timeout.ms = null
	sasl.login.refresh.buffer.seconds = 300
	sasl.login.refresh.min.period.seconds = 60
	sasl.login.refresh.window.factor = 0.8
	sasl.login.refresh.window.jitter = 0.05
	sasl.login.retry.backoff.max.ms = 10000
	sasl.login.retry.backoff.ms = 100
	sasl.mechanism = GSSAPI
	sasl.oauthbearer.clock.skew.seconds = 30
	sasl.oauthbearer.expected.audience = null
	sasl.oauthbearer.expected.issuer = null
	sasl.oauthbearer.jwks.endpoint.refresh.ms = 3600000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.max.ms = 10000
	sasl.oauthbearer.jwks.endpoint.retry.backoff.ms = 100
	sasl.oauthbearer.jwks.endpoint.url = null
	sasl.oauthbearer.scope.claim.name = scope
	sasl.oauthbearer.sub.claim.name = sub
	sasl.oauthbearer.token.endpoint.url = null
	security.protocol = PLAINTEXT
	security.providers = null
	send.buffer.bytes = 131072
	session.timeout.ms = 45000
	socket.connection.setup.timeout.max.ms = 30000
	socket.connection.setup.timeout.ms = 10000
	ssl.cipher.suites = null
	ssl.enabled.protocols = [TLSv1.2, TLSv1.3]
	ssl.endpoint.identification.algorithm = https
	ssl.engine.factory.class = null
	ssl.key.password = null
	ssl.keymanager.algorithm = SunX509
	ssl.keystore.certificate.chain = null
	ssl.keystore.key = null
	ssl.keystore.location = null
	ssl.keystore.password = null
	ssl.keystore.type = JKS
	ssl.protocol = TLSv1.3
	ssl.provider = null
	ssl.secure.random.implementation = null
	ssl.trustmanager.algorithm = PKIX
	ssl.truststore.certificates = null
	ssl.truststore.location = null
	ssl.truststore.password = null
	ssl.truststore.type = JKS
	value.deserializer = class org.apache.kafka.common.serialization.StringDeserializer

[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka version: 3.1.0
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka commitId: 37edeed0777bacb3
[main] INFO org.apache.kafka.common.utils.AppInfoParser - Kafka startTimeMs: 1655982230296
[main] INFO org.apache.kafka.clients.consumer.KafkaConsumer - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Subscribed to topic(s): demo_java
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-0 to 1 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-2 to 4 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Resetting the last seen epoch of partition demo_java-1 to 3 since the associated topicId changed from null to EV3ubJdsSyiw2e0S1ClvBQ
[main] INFO org.apache.kafka.clients.Metadata - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Cluster ID: haCR281HQJa46xeRJyL1cg
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Discovered group coordinator 127.0.0.1:9094 (id: 2147483644 rack: null)
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to re-join with the given member-id
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=11, memberId='consumer-my-third-application-1-d784761e-7670-4fcb-a546-e64976658bdd', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=11, memberId='consumer-my-third-application-1-d784761e-7670-4fcb-a546-e64976658bdd', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       []
	Current owned partitions:                  []
	Added partitions (assigned - owned):       []
	Revoked partitions (owned - assigned):     []

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: 
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=12, memberId='consumer-my-third-application-1-d784761e-7670-4fcb-a546-e64976658bdd', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=12, memberId='consumer-my-third-application-1-d784761e-7670-4fcb-a546-e64976658bdd', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-1]
	Current owned partitions:                  []
	Added partitions (assigned - owned):       [demo_java-1]
	Revoked partitions (owned - assigned):     []

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Setting offset for partition demo_java-1 to the committed offset FetchPosition{offset=0, offsetEpoch=Optional.empty, currentLeader=LeaderAndEpoch{leader=Optional[127.0.0.1:9094 (id: 3 rack: null)], epoch=3}}
```

Revisemos el consumidor 2
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=11, memberId='consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=11, memberId='consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-2]
	Current owned partitions:                  [demo_java-2]
	Added partitions (assigned - owned):       []
	Revoked partitions (owned - assigned):     []

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: 
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=12, memberId='consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=12, memberId='consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-2]
	Current owned partitions:                  [demo_java-2]
	Added partitions (assigned - owned):       []
	Revoked partitions (owned - assigned):     []

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-2])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: 
```
Revisemos el consumidor 1:
```
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0, demo_java-1])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: 
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: group is already rebalancing
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=11, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.AbstractStickyAssignor - Final assignment of partitions to consumers: 
{consumer-my-third-application-1-d784761e-7670-4fcb-a546-e64976658bdd=[demo_java-1], consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b=[demo_java-2], consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=[demo_java-0]}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 11: {consumer-my-third-application-1-d784761e-7670-4fcb-a546-e64976658bdd=Assignment(partitions=[]), consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b=Assignment(partitions=[demo_java-2]), consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=Assignment(partitions=[demo_java-0])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=11, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-0]
	Current owned partitions:                  [demo_java-0, demo_java-1]
	Added partitions (assigned - owned):       []
	Revoked partitions (owned - assigned):     [demo_java-1]

[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Revoke previously assigned partitions demo_java-1
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Request joining group due to: need to revoke partitions [demo_java-1] as indicated by the current assignment and re-join
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Notifying assignor about the new Assignment(partitions=[demo_java-0])
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Adding newly assigned partitions: 
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] (Re-)joining group
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully joined group with generation Generation{generationId=12, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.AbstractStickyAssignor - Final assignment of partitions to consumers: 
{consumer-my-third-application-1-d784761e-7670-4fcb-a546-e64976658bdd=[demo_java-1], consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b=[demo_java-2], consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=[demo_java-0]}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Finished assignment for group at generation 12: {consumer-my-third-application-1-d784761e-7670-4fcb-a546-e64976658bdd=Assignment(partitions=[demo_java-1]), consumer-my-third-application-1-26483eb0-21ce-407f-b274-5e9bc0a3b98b=Assignment(partitions=[demo_java-2]), consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed=Assignment(partitions=[demo_java-0])}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Successfully synced group in generation Generation{generationId=12, memberId='consumer-my-third-application-1-3495632d-6a5a-4daf-ba8e-1dcc2e0568ed', protocol='cooperative-sticky'}
[main] INFO org.apache.kafka.clients.consumer.internals.ConsumerCoordinator - [Consumer clientId=consumer-my-third-application-1, groupId=my-third-application] Updating assignment with
	Assigned partitions:                       [demo_java-0]
	Current owned partitions:                  [demo_java-0]
	Added partitions (assigned - owned):       []
	Revoked partitions (owned - assigned):     []

```
# 53. Java Consumer Auto Offset Commit Behavior

Una cosa que hemos estado dando por sentado son los offsets de los consumidores.
* En La api del consumidor Java, los offsets son regularmente confirmados.
* Habilita por defecto al menos una vez los escenarios de lectura.

¿Cuando se confirman los offsets?

* Los offsets se confirman cuando se llama `.poll()` y cuando han transcurrido los milisegundos configurados en `auto.commit.interval.ms`. Por ejemplo: `auto.commit.interval.ms=5000` y `enable.auto.commit=true` entonces se confirmara cada 5 segundos.

# 55. Real World Project Overview

Recursos:
1. Wikimedia Recent Change Stream: https://stream.wikimedia.org/v2/stream/recentchange
2. Demo 1: https://codepen.io/Krinkle/pen/BwEKgW?editors=1010
3. Demo 2: https://esjewett.github.io/wm-eventsource-demo/

# 56. Real World Exercise - Solution
reference: https://www.conduktor.io/apache-kafka-for-beginners

Repositorio con la solucion hecha por conduktor: https://github.com/conduktor/kafka-beginners-course



