<properties
    pageTitle="Dropped server in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: deleted server"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="Bashar-MSFT"
    ms.author="bahusse"
    displayOrder="170"
    selfHelpType="generic"
    supportTopicIds="32640015, 32780985"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d5bcb730-39d9-4889-9dce-0777c7f3c778"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Restoring a deleted server

**Follow the steps below to attempt restoring a deleted server**

Azure Database for PostgreSQL generally does not support restoring a deleted server. When a server is deleted, the operation later cascades to the backups. You can try restoring the server to a point in time just before it was dropped using [restore a dropped Azure Database for PostgreSQL server](https://docs.microsoft.com/azure/postgresql/howto-restore-dropped-server).

## **Recommended Steps**

1. Go to the **Activity Log** in the Azure portal

2. Select **Add filter**:

	* Add a filter for **Resource Type** = Azure Database for PostgreSQL servers (Microsoft.DBforPostgreSQL/servers)
	* Add a filter for **Operation** = Delete PostgreSQL Server (Microsoft.DBforPostgreSQL/servers/delete)

3. Double click on the relevant **Delete PostgreSQL Server** event
4. Select the **JSON** tab. Note down the `resourceId` and `submissionTimestamp` properties in the JSON output. The `resourceId` is in the following format: `/subscriptions/ffffffff-ffff-ffff-ffff-ffffffffffff/resourceGroups/***********/providers/Microsoft.DBforPostgreSQL/servers/********`.

    Next, you will recreate the server using the [Create Server REST API](https://docs.microsoft.com/rest/api/postgresql/servers/create). The following steps use the Azure Docs embedded REST API interface. You can choose to use your preferred REST API interface.

5. Open the [Create Server REST API page](https://docs.microsoft.com/rest/api/postgresql/servers/create). Select the green **"Try It"** tab. Sign in with your Azure account.
6. Use the `resourceId` you noted down in a previous step to fill out the `resourceGroupName`, `serverName` (deleted server name), and `subscriptionId`
7. Scroll down to the request **Body** section. Paste in the following code. **Remember to fill in the `location`, `restorePointInTime` and `sourceServerId` fields.**
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
     -  `location` - The original location of the dropped server, please note you are only allowed to choose the source server location here.
     -  `restorePointInTime` - 15 minutes prior to the delete
     -   `submissionTimestamp` you noted in a previous step
     -  `sourceServerId` - Use the `resourceId` of the dropped server


    If you see Response Code 202, the restore request is successfully submitted. The server creation status can be monitored from Activity log by filtering for Resource Type = Azure Database for MySQL servers (Microsoft.DBforMySQL/servers) and Operation = Update MySQL Server Create.

In the future, consider using [resource locks](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/prevent-the-disaster-of-accidental-deletion-for-your-postgres/ba-p/825196).

## **Recommended Documents**

* See [restore a dropped Azure Database for PostgreSQL server](https://docs.microsoft.com/azure/postgresql/howto-restore-dropped-server) to recover a dropped PostgreSQL server resource within 5 days from the time of server deletion. The recommended steps will work only if the backup for the server is still available and not deleted from the system.
* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)
* [Activity Log](https://docs.microsoft.com/azure/azure-monitor/platform/activity-log)
