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

1. Go to the [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log) from Monitor blade in Azure portal for the subscription which hosted the dropped MySQL server
2. Click on Add filter at the top and add a filter for **Resource Type** = Azure Database for MySQL servers (Microsoft.DBforMySQL/servers) and **Operation** = Delete MySQL Server (Microsoft.DBforMySQL/servers/delete)
3. Double Click on the **Delete MySQL Server** event and click on the JSON tab and note down the "resourceId" and "submissionTimestamp" attributes in JSON output. The resourceId is in the following format: `/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/TargetResourceGroup/providers/Microsoft.DBforMySQL/servers/deletedserver`
4. Next, go to [Create Server REST API Page](https://docs.microsoft.com/rest/api/mysql/servers/create) and click on **"Try It"** tab highlighted in green and login in with your Azure account
5. Provide the resourceGroupName, serverName (deleted server name), subscriptionId, derived from resourceId attribute captured in Step 3, while api-version is pre-populated
6. Next, scroll below on Request Body section and paste the following substituting the **Dropped Server Location**, **submissionTimestamp**, and **resourceId**. For restorePointInTime, specify a value of submissionTimestamp minus **15 minutes** to ensure the command doesnt error out:

```
{
"location": "Dropped Server Location",  
"properties": 
	{
    		"restorePointInTime": "submissionTimestamp - 15 minutes",
    		"createMode": "PointInTimeRestore",
    		"sourceServerId": "resourceId"
  	}
}
```

7. If you see Response Code 202, the restore request is successfully submitted. The server creation status can be monitored from Activity log by filtering for Resource Type = Azure Database for MySQL servers (Microsoft.DBforMySQL/servers) and Operation = Update MySQL Server Create. 

You can also refer to [restore a dropped Azure Database for MySQL server](https://docs.microsoft.com/azure/mysql/howto-restore-dropped-server) for detailed steps.

## **Recommended Documents**

* You can refer to [restore a dropped Azure Database for MySQL server](https://docs.microsoft.com/azure/mysql/howto-restore-dropped-server) to recover a dropped MySQL server resource within 5 days from the time of server deletion. The recommended steps will work only if the backup for the server is still available and not deleted from the system.
* Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
* [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log)
