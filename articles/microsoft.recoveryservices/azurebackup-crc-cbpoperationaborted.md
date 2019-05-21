<properties
	pageTitle="CBPOperationAborted"
	description="CBPOperationAborted"
	infoBubbleText="The current operation was canceled by the administrator."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpoperationaborted"
	diagnosticScenario="azurebackup-crc-cbpoperationaborted"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# CBPOperationAborte

<!--issueDescription-->
## We have identified that you recent backup operation has failed since it was cancelled or aborted by the user
<!--/issueDescription-->

## **Recommended Steps**
- Ensure if you're on the latest version of the Azure Backup Agent.

	- To find out the version, on the Actions pane of the MARS console, select **About Microsoft Azure Recovery Services Agent**. You can download the latest version from [here](https://aka.ms/azurebackup_agent).
- Ensure CBEngine process is running and in Services.msc the Microsoft Azure Recovery Services agent service is up and running.
- If the server was restarted or the job was cancelled, then retry the operation.
