<properties
	pageTitle="Connectivity Azure Cosmos DB Cassandra API"
  	description="Conectivity TabAzure Cosmos DB Cassandra API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="403"
	selfHelpType="resource"
	supportTopicIds="32615107"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Unable to connect to Azure Cosmos DB Cassandra API 

To resolve this issue, try one or more of the following methods.

1. Review the firewall configuration for your Cosmos DB account and confirm that the list of approved IP addresses includes that of the client attempting to connect to your Cosmos DB Table account.

2. Test the connection by accessing it from a location external to your network. This will allow you to rule out any network restrictions that may be causing the failure. One way to do this is by deploying an Azure virtual machine and running your application from the Azure VM to eliminate any network restrictions.  

3. Re-enable the firewall rule if you have recently enabled the Cosmos DB Virtual Network service endpoint.

4. Ensure the SSL is enabled in the connection options.


## **Recommended documents**

* [Connect to Azure Cosmos DB Cassandra API using .Net][Azure Cosmos DB Cassandra API FAQ](https://docs.microsoft.com/azure/cosmos-db/create-cassandra-dotnet#review-the-code)
* [Connect to Azure Cosmos DB Cassandra API using Java](https://docs.microsoft.com/azure/cosmos-db/create-cassandra-java#review-the-code)
* [Connect to Azure Cosmos DB Cassandra API using Node.js](https://docs.microsoft.com/azure/cosmos-db/create-cassandra-nodejs#review-the-code)
* [Connect to Azure Cosmos DB Cassandra API using Python](https://docs.microsoft.com/azure/cosmos-db/create-cassandra-python#review-the-code)
