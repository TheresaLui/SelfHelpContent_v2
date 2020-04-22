<properties
	pageTitle="UserErrorInsufficientSpaceForRestoreOnDisk"
	description="UserErrorInsufficientSpaceForRestoreOnDisk"
	infoBubbleText="There is insufficient free space on disk volume to create the datasource"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorinsufficientspaceforrestoreondisk"
	diagnosticScenario="azurebackup-crc-usererrorinsufficientspaceforrestoreondisk"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorInsufficientSpaceForRestoreOnDisk

<!--issueDescription-->
We have identified that your restore failed due to insufficient free space on disk volume to create the datasource.
<!--/issueDescription-->

## **Recommended Steps**

* To resolve this issue, free up the space in the target disk to create the database successfully
* Alternatively, you can choose a disk with sufficient space during the restore operation in the **Advanced Configuration** blade
