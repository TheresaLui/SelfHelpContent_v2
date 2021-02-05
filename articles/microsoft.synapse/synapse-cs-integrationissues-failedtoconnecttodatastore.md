<properties
  pagetitle="Integration Issues/Failed to connect to data store"
  description="Integration Issues/Failed to connect to data store"
  service="microsoft.synapse"
  resource="workspaces"
  ms.author="saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32783882"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-cs-integrationissues-failedtoconnecttodatastore.md"
  ownershipid="AzureData_SynapseAnalytics" />
# Integration Issues/Failed to connect to data store

## **Recommended Steps**

* Make sure that [Synapse Workspace's managed identity](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-identity) has correct permissions on data store that you are trying access.

* If you receive the error message "File cannot be opened because it does not exist or is used by another process" or "Failed to execute the query. Error: External table <_tablename_> is not accessible because content of directory cannot be listed":
   * Verify that the file exists and is not used by another process.<br>
   
   * If the storage is protected with the firewall, review the steps described in [querying firewall protected storage](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#querying-firewall-protected-storage).<br>
   Use the following PowerShell script to validate if the storage account network rules are correctly configured:<br>
   
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

## **Recommended Documents**

* [Iterative development and debugging](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json)

* [Monitor your workspace pipeline runs](https://docs.microsoft.com/azure/synapse-analytics/monitoring/how-to-monitor-pipeline-runs)

* [Supported data stores](https://docs.microsoft.com/azure/data-factory/connector-overview?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#supported-data-stores)

* [Connector troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#azure-blob-storage)
