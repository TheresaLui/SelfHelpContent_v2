<properties
	pageTitle="Role Based Access Control (RBAC) in Azure Cosmos DB"
	description="Role Based Access Control (RBAC) in Azure Cosmos DB"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32788621,32788622"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	articleId="cosmosdb-security-rbac"
	displayOrder="166"
	category="Security"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Role Based Access Control (RBAC) in Azure Cosmos DB

Most users can resolve role-based access control (RBAC) issues in Cosmos DB by using the steps below.

## **Recommended Steps**  

### **Frequently asked questions**  

### **Which Azure Cosmos DB APIs are supported by RBAC?**
<br>Only the SQL API is currently supported.   

### **Is it possible to manage role definitions and role assignments from the Azure portal?**
<br>Azure portal support for role management is not available yet.   

### **When using the Azure Cosmos DB data plane RBAC, is it possible to perform management operations (like creating a container or updating the throughput)?**
<br>No. To perform management operations with an Azure Active Directory (AD) identity, use Cosmos DB's management plane with Azure RBAC.   

### **I got an error saying that my request got blocked because I don't have the required RBAC permission. How can I solve this?**
<br>This error message explicitly mentions which action Azure Cosmos DB tried to perform. Make sure that the Azure AD identity you use is associated with a role definition that includes this action.   

### **Is the Azure AD token automatically refreshed by the Azure Cosmos DB SDKs when it expires?**
<br>Yes.   

### **Is it possible to disable the usage of the account primary key when using RBAC?**
<br>Disabling the account primary key is not currently possible.   

## **Recommended Documents**
[Configure role-based access control with Azure Active Directory for your Azure Cosmos DB account](https://docs.microsoft.com/azure/cosmos-db/how-to-setup-rbac)   
 
