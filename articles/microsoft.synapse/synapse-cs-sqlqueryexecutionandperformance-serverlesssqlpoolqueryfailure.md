<properties
  pagetitle="SQL Query Execution and Performance/Serverless SQL pool - Query failure"
  description="SQL Query Execution and Performance/Serverless SQL pool - Query failure"
  service="microsoft.synapse"
  resource="workspaces"
  ms.author="fipopovi,saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32783909"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-cs-sqlqueryexecutionandperformance-serverlesssqlpoolqueryfailure.md"
  ownershipid="AzureData_SynapseAnalytics" />
# SQL Query Execution and Performance/Serverless SQL pool - Query failure

## **Recommended Steps**

* If your query fails with the error message **'File cannot be opened because it does not exist or it is used by another process'** and you're sure both file exist and it's not used by another process, it means Serverless SQL pool can't access the file 

	* If you are using AAD login, check whether UserIdentity credential exists. If it exists, check if you have proper rights to access the file. Easiest way is to grant yourself 'Storage Blob Data Contributor' role on the storage account you're trying to query. [Visit full guide on Azure Active Directory access control for storage for more information](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal). 

	* For credentials defined on storage path level, make sure credential is not created on storage level, but at least on container level 
	
    * For configuring storage access instructions, visit [control storage access for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control) 

    * If the storage is protected with the firewall, review the steps described in [querying firewall protected storage](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#querying-firewall-protected-storage).<br>
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

* If your query fails with the error message **'Failed to execute the query. Error: External table <_tablename_> is not accessible because content of directory cannot be listed.'**<br>
   If the storage is protected with the firewall, review the steps described in [querying firewall protected storage](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-storage-files-storage-access-control?tabs=user-identity#querying-firewall-protected-storage).<br>
   Use the Powershell script above to validate if the storage account network rules are correctly configured.

* If your query fails with the error message **'The query references an object that is not supported in distributed processing mode.'**, it means that query targets data from both storage account and temporary table, which is not supported at this moment 

* If your query fails with the error message **'Operation is not allowed for a replicated database.'**, it means that query was executed in replicated database context. Replicated databases are automatically created as result of metadata synchronization with other Spark capabilities and are read-only. Learn more about [shared metadata](https://docs.microsoft.com/azure/synapse-analytics/metadata/overview), [shared databases](https://docs.microsoft.com/azure/synapse-analytics/metadata/database) and [shared tables](https://docs.microsoft.com/azure/synapse-analytics/metadata/table).

* If your query fails with the error message **'Distributed query timeout expired. The timeout period elapsed prior to completion of the distributed operation.'**, it means that query lasted longer that allowed. Visit [performance best practices for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/best-practices-sql-on-demand) to optimize your query to execute faster. 

* If your query fails with the error message **'This query cannot be executed due to current resource constraints.'**, it means that Serverless SQL is not able to execute it at this moment due to resource constraints: 

   * Please make sure data types of reasonable sizes are used. Also, specify schema for Parquet files for string columns as they will be VARCHAR(8000) by default. 

   * If your query targets CSV files, consider [creating statistics](https://docs.microsoft.com/azure/synapse-analytics/sql/develop-tables-statistics#statistics-in-sql-on-demand-preview) 

   * Visit [performance best practices for Serverless SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql/best-practices-sql-on-demand) to optimize query