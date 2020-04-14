<properties
	pageTitle="UserErrorOperationFailedTargetSQLServerInSingleUserMode"
	description="UserErrorOperationFailedTargetSQLServerInSingleUserMode"
	infoBubbleText="Operation failed as the Server is in single-user mode."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererroroperationfailedtargetsqlserverinsingleusermode"
	diagnosticScenario="azurebackup-crc-usererroroperationfailedtargetsqlserverinsingleusermode"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorOperationFailedTargetSQLServerInSingleUserMode

<!--issueDescription-->
We have identified that your restore operation failed because the SQL Server was not in multi user mode.
<!--/issueDescription-->

## **Recommended Steps**

Your restore operation failed because the SQL Server is set to single user mode. To mitigate this issue, start the server in multi-user mode:

* Go to **SQL Server Configuration Manager** and choose **SQL Server Services**. Right-click on the database engine service and select **Properties**.
* Select **Startup Parameters** and remove the **-m** parameter (without quotes) from the list and click **OK**. Skip this step-in case the **-m** parameter is not present in the **Startup Parameters** list.
* Restart the SQL Server service and retry the restore operation
