# SiteWhere InfluxDB Recipe
The recipe includes all of the core SiteWhere microservices as well as MongoDB, 
InfluxDB and Mosquitto. Device management data is stored in MongoDB while device
event data is stored in InfluxDB. Before running this recipe, make sure that the 
**infrastructure** recipe has been started so services such as ZooKeeper and Kafka 
are running.