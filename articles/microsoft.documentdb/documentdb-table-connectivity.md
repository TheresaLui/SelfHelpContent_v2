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
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Unable to connect to Cosmos DB Table API Collection

To resolve common isuses, try one or more of the following methods.

1. Review your Account Firewall configuration for Cosmos DB Account and confirm that the client public IP is added to the approved list of IPs.

2. Test the Gateway mode connection if the connection fails for the direct mode or Test Direct mode if the connection fails with Gateway mode.

3. Test the connection by accessing it from a location external to your network, this check eliminates any network restrictions causing the failure. You can test the application by  deploying an Azure virtual machine and running the application from the Azure VM which would help you to eliminate any network restriction.  

4. Renable the Firewall rule exception if you have recently enabled the Cosmos DB Virtual Network Service Endpoint.


## **Recommended documents**

* [Connection mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* [SDK usage](https://docs.microsoft.com/azure/cosmos-db/performance-tips#sdk-usage)
