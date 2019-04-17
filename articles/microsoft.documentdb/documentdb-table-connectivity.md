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
	articleId="a4d7272c-1eaf-4d31-ad59-4d99f61366bd"
/>

# Unable to connect to Azure Cosmos DB Table API collection

To resolve this issue, try one or more of the following methods.

1. Review the firewall configuration for your Cosmos DB account and confirm that the list of approved IP addresses includes that of the client attempting to connect to your Cosmos DB Table account.

2. Test the connection policy. If the connection is failing under direct mode , try it using gateway mode. Or, if it's failing under gateway mode, test it under direct mode.

3. Test the connection by accessing it from a location external to your network. This will allow you to rule out any network restrictions that may be causing the failure. One way to do this is by deploying an Azure virtual machine and running your application from the Azure VM to eliminate any network restrictions.  

4. Re-enable the firewall rule if you have recently enabled the Cosmos DB Virtual Network service endpoint.


## **Recommended documents**

* [Connection mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* [SDK performance tips](https://docs.microsoft.com/azure/cosmos-db/performance-tips#sdk-usage)
