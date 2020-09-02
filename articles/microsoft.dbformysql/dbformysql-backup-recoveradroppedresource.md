<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="savjani"
    ms.author="pariks"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32640087"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="baebc228-20af-4d96-9dcf-9f5663257124"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Recover a dropped MySQL server resource

When a server is dropped, the operation cascades to the backups shortly after the server drop operation was initiated. The following recommended steps can be followed to recover a dropped MySQL server resource within 5 days from the time of server deletion. The recommended steps will work only if the backup for the server is still available and not deleted from the system. 

## **Recommended Steps**

- Go to the [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log) from Azure portal.
- Click on Add filter at the top and add a filter for Resource Type = Azure Database for MySQL servers (Microsoft.DBforMySQL/servers).
- Click on Add filter to add another filter for Operation = Delete MySQL Server (Microsoft.DBforMySQL/servers/delete).
- Double Click on the Delete MySQL Server and click on the JSON tab and note down the "resourceId" and "submissionTimestamp" attributes in JSON output. The resourceId is in the following format /subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/TargetResourceGroup/providers/Microsoft.DBforMySQL/servers/deletedserver
- Next go to [MySQL Server Create Page](https://docs.microsoft.com/en-us/rest/api/mysql/servers/create) and click on Try It tab highlighted in green and login in with your Azure account.
- Provide the resourceGroupName, serverName (deleted server name), subscriptionId, derived from resourceId attribute while api-version is pre-populated. Next scroll below on Request Body section and paste the following

{
"location": "<Dropped Server Location>",  
"properties": 
	{
    		"restorePointInTime": <submissionTimestamp>,
    		"createMode": "PointInTimeRestore",
    		"sourceServerId": "/subscriptions/5c5037e5-d3f1-4e7b-b3a9-f6bf94902b30/resourcegroups/pariks-pass-demo/providers/Microsoft.DBforMySQL/servers/parikmysql"
  	}
}

- If you see Response Code 202, the restore request is successfully submitted. The server creation status can be monitored from Activity log by filtering for for Resource Type = Azure Database for MySQL servers (Microsoft.DBforMySQL/servers)

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity)
* [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log)
