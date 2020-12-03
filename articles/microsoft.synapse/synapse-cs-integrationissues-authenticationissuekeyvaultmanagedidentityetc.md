<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783836"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Integration Issues/Authentication issue (Key Vault, Managed Identity, etc.)"
    description = "Integration Issues/Authentication issue (Key Vault, Managed Identity, etc.)"
    articleId = "synapse-cs-integrationissues-authenticationissuekeyvaultmanagedidentityetc.md"
    ms.author = "saltug"
/>

# Integration Issues/Authentication issue (Key Vault, Managed Identity, etc.)

## **Recommended Steps**

Make sure you provided right credentials while creating your linked service. You can review [Grant permissions to workspace managed identity](https://docs.microsoft.com/azure/synapse-analytics/security/how-to-grant-workspace-managed-identity-permissions) to allow your Synapse Workspace have access to the resources you want to link.

To reference a stored credential stored in Azure Key Vault, you need to:

1. Retrieve Synapse Workspace managed identity
2. Grant the managed identity access to your Azure Key Vault
3. Create a linked service pointing to your Azure Key Vault
4. Create data store linked service, inside which reference the corresponding secret stored in key vault

## **Recommended Documents**

* [Securing a linked service with Private Links](https://docs.microsoft.com/azure/synapse-analytics/data-integration/linked-service)

* [Grant permissions to workspace managed identity](https://docs.microsoft.com/azure/synapse-analytics/security/how-to-grant-workspace-managed-identity-permissions)

* [Access control to workspace pipeline runs](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control#access-control-to-workspace-pipeline-runs)

* [Linked services in Azure Synapse Analytics](https://docs.microsoft.com/azure/data-factory/concepts-linked-services?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json)

Store credentials in and retrieve from Azure Key Vault Document, including following sections:

* [Prerequisites](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#prerequisites)

* [Steps](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#steps)

* [Azure Key Vault linked service](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#azure-key-vault-linked-service)

* [Reference secret stored in key vault](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#reference-secret-stored-in-key-vault)
 