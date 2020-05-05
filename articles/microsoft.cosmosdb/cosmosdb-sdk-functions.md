<properties 
	pageTitle="SDK issues on Azure Functions" 
	description="Issues while using the Cosmos DB SDK on Azure Functions" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="ealsur" 
	ms.author="maquaran" 
	selfHelpType="generic" 
	supportTopicIds="32688838,32688840"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sdk-functions" 
	displayOrder="298" 
	category="SDK (SQL API) Issues" 
	ownershipId="AzureData_AzureCosmosDB"
/>

# Using the Azure Cosmos DB SDK in Azure Functions
This section refers to using the Cosmos DB SDK to perform operations in the context of an Azure Function. 

## **Recommended Steps**  

### **Issues with the Azure Functions Trigger for Azure Cosmos DB**
Please see the `Tools and Connectors` problem type for specific troubleshooting with the Azure Functions Trigger for Cosmos DB.

### **Functions Host restart**  
[Azure Functions Host has limits](https://docs.microsoft.com/azure/azure-functions/functions-scale#service-limits) regarding the number of connections, memory utilization, and execution timeout.
<br>If the Host is restarting it could be related to a violation of one of these limits.
<br>In the case of the Cosmos DB SDK the most common cause is not using the client as a **singleton** instance. Valid options are:
1. Use a [static client](https://docs.microsoft.com/azure/azure-functions/manage-connections#static-clients) instance.
1. Leverage [Dependency Injection on Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-dotnet-dependency-injection) to initialize and reuse the same client instance.

### **401 - UnauthorizedException**
This error is often related to using an invalid authorization key or credential. 
1. Verify that the Key being used is valid. If you are reading the Key or Connection String from an external source, like Azure Key Vault, verify the information there is up to date.
1. If there was a recent key rotation on the account, ensure you went with the [recommended procedure](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#key-rotation). When using any old or new key there is a window of time where the key might not be valid.

### Other issues
For any other issues, see the **SDK - Error or unexpected result** problem type. Azure Functions is mainly the execution environment and there is a possibility of the issue being a generic SDK issue covered in the general troubleshooting.

## **Recommended Documents**  

[Troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api-faq)
<br>Frequently asked questions about Cosmos DB SQL API.  
