<properties
	pageTitle="On-premises agent is offline"
	description="On-premises agent is offline"
	infoBubbleText="Found on-premises agent offline. See details on the right."
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_datasync_onpremagentoffline"
	diagnosticScenario="SqlDataSync"
	selfHelpType="diagnostics"
	supportTopicIds="32630455"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_DataSync"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->  
We were able to detect the following on-premises agent(s) offline:<br>
**<!--$OnPremAgentOfflineList--> OnPremAgentOfflineList <!--/$OnPremAgentOfflineList-->**
<!--/issueDescription-->

Any of the following conditions might be present:

- **Cause**: The client agent is offline
- **Resolution**: Be sure that the client agent is online and then try again

- **Cause**: The client agent is uninstalled or missing
- **Resolution**: If the client agent is uninstalled or otherwise missing:

    1. Remove the agent XML file from the SQL Data Sync installation folder, if the file exists
    2. Install the agent on an on-premises computer (it can be the same or a different computer). Then, submit the agent key that's generated in the portal for the agent that's showing as offline.

- **Cause**: The SQL Data Sync service is stopped
- **Resolution**: Restart the SQL Data Sync service:

    1. In the **Start** menu, search for **Services**
    2. In the search results, select **Services**
    3. Find the **SQL Data Sync** service
    4. If the service status is **Stopped**, right-click the service name, and then select **Start**
