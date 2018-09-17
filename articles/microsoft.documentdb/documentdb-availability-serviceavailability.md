<properties
	pageTitle="Cosmos DB is responding Service Unavailable"
  description="Cosmos DB Service Unavailable"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32597558"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# Cosmos DB is responding Service Unavailable

The Service Unavailable error is thrown by the client SDK and it could be that the Cosmos Service is functioning fine.  
Please review the Metric Tab for the Availability SLA for the given Cosmos Account. Please reach out to Support if the metric tab does 
reflect the availability the availability issue. 

Otherwise, ensure the application has implemented the Peformance Tips with respect to Networking and SDKs from https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking. Also, review the client resource such as CPU memory pressure on the client machine.



