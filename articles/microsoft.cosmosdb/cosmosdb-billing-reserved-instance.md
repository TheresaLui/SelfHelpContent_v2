<properties
	pageTitle="Reserved Instance in Azure Cosmos DB"
	description="Learn more about Azure Cosmos DB Reserved Capacity"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="tisande"
	ms.author="tisande"
	selfHelpType="generic"
	supportTopicIds="32692544"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-billing-reserved-instance"
	displayOrder="101"
	category="Billing and Pricing"
	ownershipId="AzureData_AzureCosmosDB"
/>


# Reserved Instance in Azure Cosmos DB 

Most users are able to resolve their Reserved Instance issue using the steps below.   


## **Recommended Steps**   

Reserved Instance (RI), also referred to as Reserved Capacity, can be a great way to reduce your Azure Cosmos DB bill. Savings for Azure Cosmos DB Reserved Capacity are outlined in the [Azure Cosmos DB pricing page](https://azure.microsoft.com/pricing/details/cosmos-db/) and [these steps](https://docs.microsoft.com/azure/cosmos-db/cosmos-db-reserved-capacity#buy-azure-cosmos-db-reserved-capacity) to purchase an Azure Cosmos DB Reserved Capacity reservation. You will also see Azure Cosmos DB Reserved Capacity size recommendations on this page as well as estimated discount amounts.  

To purchase a reservation, you must for the Cloud Solution Provider (CSP) program, be an admin or sales agent: 
* Be in the Owner role for at least one Enterprise or individual subscription with pay-as-you-go rates
* For Enterprise subscriptions, add Reserved Instance must be enabled in the [EA portal](https://ea.azure.com/) or if that setting is disabled, you must be an EA Admin on the subscription
* For the Cloud Solution Provider (CSP) program, only admin agents or sales agents can buy Azure Cosmos DB reserved capacity  

Azure Cosmos DB Reserved Capacity can be scoped to a single subscription, a single resource group, or shared across an entire Azure enrollment. You can change the reservation scope at any time. You can pay upfront or monthly for Azure Cosmos DB Reserved Capacity.  

## **Recommended Documents**   

[Optimize cost with reserved capacity in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cosmos-db-reserved-capacity)
<br>Azure Cosmos DB reserved capacity helps you save money by committing to a reservation for Azure Cosmos DB resources for either one year or three years. With Azure Cosmos DB reserved capacity, you can get a discount on the throughput provisioned for Cosmos DB resources. Examples of resources are databases and containers (tables, collections, and graphs).  

[What are Azure reservations?](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)
<br>Azure Reservations help you save money by committing to one-year or three-years plans for virtual machines, Azure Blob storage or Azure Data Lake Storage Gen2, SQL Database compute capacity, Azure Cosmos DB throughput, or other Azure resources. Committing allows you to get a discount on the resources you use. Reservations can significantly reduce your resource costs up to 72% on pay-as-you-go prices. Reservations provide a billing discount and don't affect the runtime state of your resources.  


[Understand reservation usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)
<br>Reservation costs and usage data are available for Enterprise Agreement customers in the Azure portal and REST APIs.
<br>This article helps you:
* Get reservation purchase data
* Know which subscription, resource group or resource used the reservation
* Chargeback for reservation utilization
* Calculate reservation savings
* Get reservation under-utilization data
* Amortize reservation costs  


[Understand reservation usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)
<br>This article helps you understand the reservation usage for a Pay-As-You-Go subscription.