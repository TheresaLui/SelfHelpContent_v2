<properties
    pageTitle="Authorization"
    description="Troubleshoot Azure Cosmos DB Authorization and RBAC related issues"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32681006"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-admin-rbac"
    displayOrder="26"
    category="Administration"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Authorization and Role-based access control (RBAC) Topics

Azure Cosmos DB provides built-in role-based access control (RBAC) for common *control-plane* management scenarios in Azure Cosmos DB such as creating or deleting databases or containers, changing throughput, changing default consistency levels, adding or removing regions, or regenerating access keys. These and other operations can assign any of the [built-in Azure Cosmos DB RBAC roles](https://docs.microsoft.com/azure/cosmos-db/role-based-access-control) to users, groups, service principals, or managed identities to grant or deny access to resources and operations on Azure Cosmos DB resources. Subscription administrators can also create [custom RBAC roles](https://docs.microsoft.com/azure/role-based-access-control/custom-roles) to suit their needs.

**Note**: If you are receiving an error message for insufficient permissions or authorization error, follow up with the administrator for the Cosmos account or subscription so that the required permissions can be granted.

## **Recommended Steps**

### **Role Based Access Control**

* For a listing of the built-in RBAC roles for Azure Cosmos DB see [Role-based access control in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/role-based-access-control)
* For a listing of all operations that can be configured for a custom RBAC role, see [Azure Cosmos DB Resource Provider Operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftdocumentdb)
* Please note, role assignments are scoped to **control-plane access only**, as defined above. Data plane operations, including queries and all CRUD operations on data stored within Azure Cosmos DB are secured using master keys, resource tokens, Azure Key Vault or using a certificate-based approach as shown below. To learn more, see [Secure access to data in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data).
* Users can use managed identities to secure access to the master keys for Azure Cosmos DB and allow for safe key rotation. To learn more see, [How to use a system-assigned managed identity to access Azure Cosmos DB data](https://docs.microsoft.com/azure/cosmos-db/managed-identity-based-authentication)
* Finally, users can choose to implement a certificate-based authentication for an Azure AD identity to allow users to access data within Azure Cosmos DB without having to distribute the master keys. For more information on how to implement this see, [Certificate-based authentication with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/certificate-based-authentication).

### **Cannot load a document in Data explorer: Error 401**

Error Message: *The input authorization token can't serve the request. Please check that the expected payload is built as per the protocol, and check the key being used.*

* First verify the expected payload is as per the protocol you are using
* If you are experiencing this error in Data Explorer when using special character encodings in the id, this is a current known issue. Please use the [Sunset Link](https://cosmos.azure.com/sunset) as a workaround.

## **Recommended Documents**

[How to create a custom RBAC role](https://docs.microsoft.com/azure/role-based-access-control/custom-roles)
<br>If the built-in roles for Azure resources don't meet the specific needs of your organization, you can create your own custom roles. This article covers how you can create and assign custom roles to users, groups, and service principals at subscription, resource group, and resource scopes.  

[Azure Cosmos DB Security Overview](https://docs.microsoft.com/azure/cosmos-db/database-security)
<br>This article discusses database security best practices and key features offered by Azure Cosmos DB to help you prevent, detect, and respond to database breaches.  

[Azure Cosmos DB Resource Provider Operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftdocumentdb)
<br>This article lists the operations available for each Azure Resource Manager resource provider. These operations can be used in custom roles to provide granular role-based access control (RBAC) to resources in Azure.  

[How to use a system-assigned managed identity to access Azure Cosmos DB data](https://docs.microsoft.com/azure/cosmos-db/managed-identity-based-authentication)
<br>Gone are the days of copying and pasting keys. Use managed identities to unlock a **robust, key rotation agnostic** solution to get your Azure Cosmos DB keys on demand. From there you can use the keys to access your Azure Cosmos DB's databases, containers, and items.  
[Certificate-based authentication with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/certificate-based-authentication)
<br>Certificate-based authentication enables your client application to be authenticated by using Azure Active Directory (Azure AD) with a client certificate. You can perform certificate-based authentication on a machine where you need an identity, such as an on-premises machine or virtual machine in Azure.  

[Secure Azure Cosmos keys using Azure Key Vault](https://docs.microsoft.com/azure/cosmos-db/access-secrets-from-keyvault)
<br>When using Azure Cosmos DB for your applications, you can access the database, collections, documents by using the endpoint and the key within the app configuration file. However, it is not safe to put keys and URL directly in the application code because they are available in clear text format to all the users. You want to make sure that the endpoint and keys are available but through a secured mechanism. This is where Azure Key Vault can help you to securely store and manage application secrets.  
