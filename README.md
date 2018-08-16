# Spring-Cloud-Config-server

EmployeeProducer produces the employee details through its service and EmployeeConsumer consume it

Instead of hardcoding the Service URL and port of EmployeeProducer in consumer module, Use EurekaServer that registers both the services.

Incase if the location of EmployeeProducer changes, consumer module can still consumes the service because producer registers itself with EurekaServer and it provides the service to consumer

Netflix Ribbon's RoundRobinRule algorithm is used to balance the load on EmployeeProducer module. Download and run producer module on different ports to create multiple instances and consume it

EmployeeProducer gets the EurekaServer URL through the CloudConfigServer which has a central externalized common configurations required by the services 
