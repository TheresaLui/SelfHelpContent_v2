<properties
  pagetitle="Administration and Security/Serverless SQL pool - Storage access control"
  service="microsoft.synapse"
  resource="workspaces"
  ms.author="fipopovi,saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32783913"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-cs-administrationandsecurity-serverlesssqlpoolstorageaccesscontrol.md"
  ownershipid="AzureData_SynapseAnalytics" />
# Administration and Security/Serverless SQL pool - Storage access control

Most customers resolve their storage access issues in Serverless SQL pool using these steps.


## **Recommended Steps**

* **"File cannot be opened because it does not exist or is used by another process"**
   If your query fails with the above error message and you're sure both file exist and it's not used by another process, it means Serverless SQL pool can't access the file.

* **"Failed to execute the query. Error: External table <_tablename_> is not accessible because content of directory cannot be listed."**
   If the storage is protected with the firewall, review the steps described in [querying firewall protected storage](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#querying-firewall-protected-storage).

* **If you use AAD login, check if the UserIdentity credential exists**
   If this credential exists and you don't have permissions to access the file, grant yourself the **'Storage Blob Data Contributor'** role on the storage account you're trying to query. [Visit full guide on Azure Active Directory access control for storage for more information](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal). 

* **For credentials defined on the storage path level, create these credentials at the container level or higher (not at the storage level).**
   For more information see [control storage access for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control). 

* **Create appropriate credentials as described in [control storage access for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control).**

* **Check the [supported storage authorization types](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#supported-storage-authorization-types).**

* **If using ADF to access the Serverless SQL pool, determine if the MSI account for your workspace has been given access to storage.**
      MSI account has the same name as your workspace name. [Visit full guide on Azure Active Directory access control for storage for more information](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal).

## **Recommended Documents**

* [Control storage account access for serverless SQL](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity)

* [Supported storage authorization types](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#supported-storage-authorization-types)

* [Querying firewall protected storage](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#querying-firewall-protected-storage)

* [Credentials - Server and Database-scoped](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#credentials)

* [Use the Azure portal to assign an Azure role for access to blob and queue data](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal)

* [Configure Azure Storage firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)
