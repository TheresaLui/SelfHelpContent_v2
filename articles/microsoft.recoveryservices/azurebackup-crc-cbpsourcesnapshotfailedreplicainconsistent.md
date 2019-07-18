<properties
	pageTitle="CBPSourceSnapshotFailedReplicaInconsistent "
	description="CBPSourceSnapshotFailedReplicaInconsistent "
	infoBubbleText="Backup failed because the disk-backup replica is either invalid or missing."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbpsourcesnapshotfailedreplicainconsistent"
	diagnosticScenario="azurebackup-crc-cbpsourcesnapshotfailedreplicainconsistent"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error CBPSourceSnapshotFailedReplicaInconsistent

<!--issueDescription-->
We have identified that your backup operation failed because the Source volume snapshot failed due to inconsistent datasource replica.
<!--/issueDescription-->

## **Recommended Steps**

To resolve the issue, try the following:

* [Manually perform a consistency check on data source and retry backup operation](https://docs.microsoft.com/previous-versions/system-center/data-protection-manager-2006/cc161279%28v%3dtechnet.10%29)
* Create a disk recovery point and retry backup operation
