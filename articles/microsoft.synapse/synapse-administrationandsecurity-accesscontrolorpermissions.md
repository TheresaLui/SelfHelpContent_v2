<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738757"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Administration and Security/Access control or permissions"
	description = "Administration and Security/Access control or permissions"
	articleId = "synapse-administrationandsecurity-accesscontrolorpermissions"
	authors = "saltug"
	ms.author = "saltug"
/>

# Administration and Security/Access control or permissions

## **Recommended Steps**

A [system-assigned managed identity](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-identity) is created for your Azure Synapse workspace when you create the workspace. You can [retrieve your workspace's managed identity](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-identity#retrieve-managed-identity-in-azure-portal) from Azure Portal.

When a table (a table in a Spark database or external table created in SQL On-Demand) is queried by Spark or SQL on-demand engines that the query submitter has the right to use, the query **submitter's security principal is being passed through** to the underlying files. Permissions are checked at the file system level. Learn how to [assign ```Storage Blob Data Reader``` or ```Storage Blob Data Contributor``` RBAC permissions on Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#assign-a-built-in-rbac-role).

### Spark and SQL Pool Security Model on Metadata
* The Spark databases and tables, along with their synchronized representations in the SQL engines will be secured at the underlying storage level.
* The security principal who creates a database is considered the owner of that database, and has all the rights to the database and its objects.
* The security principal who creates a managed table is considered the owner of that table and has all the rights to the table as well as the underlying folders and files. In addition, the owner of the database will automatically become co-owner of the table.
* If you create a Spark or SQL external table with authentication pass-through, the data is only secured at the folder and file levels. If someone queries this type of external table, the security identity of the query submitter is passed down to the file system, which will check for access rights.

## **Recommended Documents**

* [Secure your Synapse workspace](https://docs.microsoft.com/azure/synapse-analytics/security/how-to-set-up-access-control#overview)
* [Azure Synapse workspace managed identity](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-identity)
* [Create and manage IP firewall rules](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall#create-and-manage-ip-firewall-rules)
* [Managed workspace VNet](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-vnet)
* [Managed private endpoint](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-private-endpoints)
* [Azure Active Directory Authentication](https://docs.microsoft.com/azure/synapse-analytics/sql/active-directory-authentication)
* [AAD pass-through in Azure Synapse Analytics](https://docs.microsoft.com/azure/synapse-analytics/sql/active-directory-authentication#aad-pass-through-in-azure-synapse-analytics)

