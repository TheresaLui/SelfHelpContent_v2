<properties
	pageTitle="CBPOperationAborted"
	description="CBPOperationAborted"
	infoBubbleText="The current operation was canceled by the administrator."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbpoperationaborted"
	diagnosticScenario="azurebackup-crc-cbpoperationaborted"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBP Operation Aborted

<!--issueDescription-->
We have identified that you recent backup operation has failed as it was cancelled or aborted by the user. To resolve this issue, ensure you are using the latest version of the Azure Backup Agent. To see the version currently in use, on the Actions pane of the MARS console, select **About Microsoft Azure Recovery Services Agent**.
<!--/issueDescription-->

## **Recommended Steps**

- Ensure if you are on the latest version of the Azure Backup Agent. To find out the version, on the Actions pane of the MARS console, select **About Microsoft Azure Recovery Services Agent**. You can download the latest version from [here](https://aka.ms/azurebackup_agent).
- Ensure CBEngine process is running and in services.msc the Microsoft Azure Recovery Services agent service is up and running
- If the server was restarted or the job was cancelled, then retry the operation
