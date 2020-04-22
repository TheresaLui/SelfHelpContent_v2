<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738833"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Authentication failure/Storage Accounts"
	description = "Authentication failure/Storage Accounts"
	articleId = "synapse-authenticationfailure-storageaccounts"
	authors = "saltug"
	ms.author = "saltug"
/>

# Authentication failure/Storage Accounts

## **Recommended Steps**

You need to be a member of the ```Storage Blob Reader``` role on the underlying storage in order to be able to query the files. Learn how to [assign ```Storage Blob Data Reader``` or ```Storage Blob Data Contributor``` RBAC permissions on Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#assign-a-built-in-rbac-role).

Check how you can [Secure your Synapse workspace](https://docs.microsoft.com/azure/synapse-analytics/security/how-to-set-up-access-control) to make sure all necessary settings are in place.

If you are using private links to your workspace, please review [Securing a linked service with Private Links](https://docs.microsoft.com/azure/synapse-analytics/data-integration/linked-service)

Make sure you [Grant permissions to workspace managed identity](https://docs.microsoft.com/azure/synapse-analytics/security/how-to-grant-workspace-managed-identity-permissions) for allowing your Synapse Workspace identity to access your storage accounts

## **Recommended Documents**

* [Create a Managed private endpoint to your data source](https://docs.microsoft.com/azure/synapse-analytics/security/how-to-create-managed-private-endpoints)
* [Securing a linked service with Private Links](https://docs.microsoft.com/azure/synapse-analytics/data-integration/linked-service)
