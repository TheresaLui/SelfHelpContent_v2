<properties
    pageTitle="Authorization"
    description="Troubleshoot Azure Cosmos DB Authorization and RBAC related issues"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="markjbrown"
    ms.author="mjbrown"
    selfHelpType="resource"
    supportTopicIds="32681006"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
    articleId="cosmosdb-admin-rbac"
    displayOrder="26"
    category="Administration"
/>

# Azure Cosmos DB Authorization and Role-based access control (RBAC) Topics

Azure Cosmos DB provides built-in role-based access control (RBAC) for common *control-plane* management scenarios in Azure Cosmos DB such as creating or deleting databases or containers, changing throughput, changing default consistency levels, adding or removing regions, or regenerating access keys. These and other operations can assign any of the [built-in Azure Cosmos DB RBAC roles](https://docs.microsoft.com/azure/cosmos-db/role-based-access-control) to users, groups, service principals, or managed identities to grant or deny access to resources and operations on Azure Cosmos DB resources. Subscription administrators can also create [custom RBAC roles](https://docs.microsoft.com/azure/role-based-access-control/custom-roles) to suit their needs.

**Note**: If you are receiving an error message for insufficient permissions or authorization error, follow up with the administrator for the Cosmos account or subscription so that the required permissions can be granted.

## **Recommended Steps**

* For a listing of the built-in RBAC roles for Azure Cosmos DB see [Role-based access control in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/role-based-access-control)
* For a listing of all operations that can be configured for a custom RBAC role, see [Azure Cosmos DB Resource Provider Operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftdocumentdb)
* Please note, role assignments are scoped to **control-plane access only**, as defined above. Data plane operations, including queries and all CRUD operations on data stored within Azure Cosmos DB are secured using master keys, resource tokens, Azure Key Vault or using a certificate-based approach as shown below. To learn more, see [Secure access to data in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data).
* Users can use Azure Key Vault to secure access to the master keys for Azure Cosmos DB. To learn more see, [Secure Azure Cosmos keys using Azure Key Vault](https://docs.microsoft.com/azure/cosmos-db/access-secrets-from-keyvault).
* Finally, users can choose to implement a certificate-based authentication for an Azure AD identity to allow users to access access data within Azure Cosmos DB without having to distribute the master keys. For more information on how to implement this see, [Certificate-based authentication with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/certificate-based-authentication).

## **Recommended Documents**

* [How to create a custom RBAC role](https://docs.microsoft.com/azure/role-based-access-control/custom-roles)
* [Azure Cosmos DB Security Overview](https://docs.microsoft.com/azure/cosmos-db/database-security)
* [Azure Cosmos DB Resource Provider Operations](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftdocumentdb)
* [Certificate-based authentication with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/certificate-based-authentication)
* [Secure Azure Cosmos keys using Azure Key Vault](https://docs.microsoft.com/azure/cosmos-db/access-secrets-from-keyvault)
