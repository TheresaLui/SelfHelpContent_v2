<properties
	pageTitle="UserErrorCannotOpenFailoverClusteringRegKey"
	description="UserErrorCannotOpenFailoverClusteringRegKey"
	infoBubbleText="Failed to open the Windows Server Failover Clustering Registry SubKey. This caused the operation to fail."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorcannotopenfailoverclusteringregkey"
	diagnosticScenario="azurebackup-crc-usererrorcannotopenfailoverclusteringregkey"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorCannotOpenFailoverClusteringRegKey

<!--issueDescription-->
We have identified that your backup operation failed due an issue opening the Windows Server Failover Clustering Registry Subkey.
<!--/issueDescription-->

## **Recommended Steps**

 To resolve this issue, perform the below:

 - Ensure WSFC service is installed, running and accessible in the current state
 - Ensure the availability group has is not dropped
 - Retry the operation to test if the issue was transient
