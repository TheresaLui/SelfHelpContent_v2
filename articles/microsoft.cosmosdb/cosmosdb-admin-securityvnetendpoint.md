<properties
	pageTitle="Cosmos security and VNet service endpoint"
	description="Troubleshoot CosmosDB security and VNet service endpoint related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636764"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-admin-securityvnetendpoint"
	displayOrder="24"
	category="Administration"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Connection failure after VNet service endpoint configuration
Most users are able to resolve their security and VNet case using the steps below.


## **Recommended Steps**

Please wait for 15-20 minutes before testing the connection through the VNet. You must re-enable the IP Firewall rule after you enable the Azure Virtual Network service endpoint.  

### **Unable to update Consistency as well as enable or disable multi-region writes**
With VNET enabled accounts, the selected user making changes to the account must have permissions on the VNET.
* Add the necessary permissions to the desired user to make changes or assign another user with the expected permissions to update the consistency 


## **Recommended Documents**
* [Secure access to an Azure Cosmos DB account by using Azure Virtual Network service endpoint](https://docs.microsoft.com/azure/cosmos-db/vnet-service-endpoint)
* [Frequently asked questions](https://docs.microsoft.com/azure/cosmos-db/vnet-service-endpoint#frequently-asked-questions)
