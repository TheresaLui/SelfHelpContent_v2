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

# Unable to connect to Cosmos DB Table API collection

To resolve common issues, try one or more of the following methods.

1. Review your account firewall configuration for Cosmos DB Account and confirm that the client public IP is added to the approved list of IPs.

2. Test the gateway mode connection if the connection fails for the direct mode or test direct mode if the connection fails with gateway mode.

3. Test the connection by accessing it from a location external to your network, this check eliminates any network restrictions causing the failure. You can test the application by  deploying an Azure virtual machine and running the application from the Azure VM which would help you to eliminate any network restriction.  

4. Renable the firewall rule if you have recently enabled the Cosmos DB Virtual Network service endpoint.


## **Recommended documents**

* [Connection mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* [SDK performance tips](https://docs.microsoft.com/azure/cosmos-db/performance-tips#sdk-usage)
