<properties
	pageTitle="CBPSourceSnapshotFailedReplicaMissingOrInvalid "
	description="CBPSourceSnapshotFailedReplicaMissingOrInvalid "
	infoBubbleText="Backup failed because the disk-backup replica is either invalid or missing."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbpsourcesnapshotfailedreplicamissingorinvalid "
	diagnosticScenario="azurebackup-crc-cbpsourcesnapshotfailedreplicamissingorinvalid"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error CBPSourceSnapshotFailedReplicaMissingOrInvalid

<!--issueDescription-->
We have identified that your backup operation failed because the disk-backup replica is either invalid or missing
<!--/issueDescription-->

## **Recommended Steps**
To resolve CBPSourceSnapshotFailedReplicaMissingOrInvalid issue, try the following:

* Manually perform a consistency check on data source and retry backup operation. For more information, see this [article](https://docs.microsoft.com/previous-versions/system-center/data-protection-manager-2006/cc161279%28v%3dtechnet.10%29).
* Create a disk recovery point and retry backup operation.
