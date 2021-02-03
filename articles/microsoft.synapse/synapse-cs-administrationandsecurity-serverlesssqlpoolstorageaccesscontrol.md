<properties
  pagetitle="Administration and Security/Serverless SQL pool - Storage access control&#xD;"
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

* **"File cannot be opened because it does not exist or is used by another process"**<br>
   If your query fails with this error and you've verified that the file exists and is not used by another process, then the Serverless SQL pool can't access the file.<br>
   If the storage is protected with the firewall, review the steps described in [querying firewall protected storage](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#querying-firewall-protected-storage).<br>
   Use the following Powershell script to validate if the storage account network rules are correctly configured:<br>
   
   ```
      $resourceGroupName = "<resource group name>"
      $accountName = "<storage account name>"
      $rule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName $resourceGroupName -Name $accountName
      
      $rule.ResourceAccessRules | ForEach-Object {
         Write-Host "Rule: " $_.ResourceId
         if ($_.ResourceId -cmatch "\/subscriptions\/(\w\-*)+\/+resourcegroups\/+(.)")
            { Write-Host "Storage account network rule is successfully configured." -ForegroundColor Green }
         else
            { Write-Host "Storage account network rule is not configured correctly. The identifier ""resourcegroups"" must be in lower case." -ForegroundColor Yellow }
         Write-Host
      }
   ```

* **"Failed to execute the query. Error: External table <_tablename_> is not accessible because content of directory cannot be listed."**<br>
   If the storage is protected with the firewall, review the steps described in [querying firewall protected storage](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#querying-firewall-protected-storage).<br>
   Use the Powershell script above to validate if the storage account network rules are correctly configured.

* **If you use AAD login, check if the UserIdentity credential exists**<br>
   If this credential exists, you can give yourself permission to access the file by granting yourself the **Storage Blob Data Contributor** role on the storage account you're trying to query. [Visit full guide on Azure Active Directory access control for storage for more information](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal). 

* **Create storage path credentials at the container level or higher (not at the storage level).**<br>
   For more information see [control storage access for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control). 

* **Create appropriate credentials as described in [control storage access for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control).**

* **Check the [supported storage authorization types](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#supported-storage-authorization-types).**

* **If using ADF to access the Serverless SQL pool, determine if the MSI account for your workspace has been given access to storage.**
      MSI account has the same name as your workspace name. [Visit full guide on Azure Active Directory access control for storage for more information](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal).

## **Recommended Documents**

* [Control storage account access for serverless SQL](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity)

* [Querying firewall protected storage](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#querying-firewall-protected-storage)

* [Credentials - Server and Database-scoped](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#credentials)

* [Configure Azure Storage firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)
