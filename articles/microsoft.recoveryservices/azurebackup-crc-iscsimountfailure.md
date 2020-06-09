<properties
	pageTitle="IscsiMountFailure"
	description="IscsiMountFailure"
	infoBubbleText="Mounting the disk failed."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-iscsimountfailure"
	diagnosticScenario="azurebackup-crc-iscsimountfailure"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error IscsiMountFailure

<!--issueDescription-->
We have identified that your files and folders restore operation failed because iSCSI failed to mount the volume. 
<!--/issueDescription-->

## **Recommended Steps**

- Open iSCSI initiator and check if Target > Status is shown as Connected (note: sometimes it might show connected but the status could be inactive)
- To resolve this issue, disconnect the target and retry the restore operation
