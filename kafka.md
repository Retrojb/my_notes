# KAFKA notes

Patrick Druley

Series of events

Producers: forms that generate events (writing) to kafka
writess to a kafka brokers(house data) (AWS infrastructure) associated with disks 

once in broker is polled to the consumer does things with the data 

kafka decouples procucers and consumer reduces app to app integration
topics: metadata for describing structure, logical representation, categorizes events into groups
	producer: Do these procucers produce the same event?
	retention policies: how long will data be stored in a topic (default 1 week)
	segements --> paritions --> topics --> broker
	stream unbound series of events (not set by time, batched work, bounded) 
	
	events 
		Header info: Topic, parition, timestamp, etc (holds message, record, event as metadata)
		Body info: { k, v }
		
producers send events tp brokers
broker receive and store events
	cluster can have many brokers
	each broker manages multiple paritions
	brokers talk to each other for replication purpose  
	
Kafka Connect API
framework and server service import and export data from kafka 
	can manage hundereds of data sources
	source connector (producer) and sink (consumer)
	
Kafka Streams API
	transform data in real time
	
