<properties
	pageTitle="Connectivity Table API"
  	description="Conectivity Table API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="68"
	selfHelpType="resource"
	supportTopicIds="32597500"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Unable to connect to Cosmos DB Table API Collection

To resolve common isuses, try one or more of the following methods.

1. Review your Account Firewall configuration for Cosmos DB Account and confirm the client public ip is added to the exception list.

2. Test the Gateway mode connection if the connection is failing for the direct mode or Test Direct mode if its failing with Gateway mode.

3. Test the connection from outside of your network to eliminate any network restrictions causing the failure.  You can test the application by
   deploying a Azure Virtual machine and running the application from the Azure VM which would help you to eliminate any network restriction.  

4. Renabled the Firewall rule exception if you have recently enabled the Cosmos DB Virtual Network Service Endpoint.


## **Recommended documents**

* [Connection mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* [SDK usage](https://docs.microsoft.com/azure/cosmos-db/performance-tips#sdk-usage)
