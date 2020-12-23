<properties
	pageTitle="NoExtensionStatusButStatusBlobAvailable"
	description="NoExtensionStatusButStatusBlobAvailable"
	infoBubbleText="backup operation failed because IaaS VM (with Linux OS) backup extension execution was stuck or crashed or the system calls might have timed out"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-noextensionstatusbutstatusblobavailable"
	diagnosticScenario="azurebackup-crc-noextensionstatusbutstatusblobavailable"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error NoExtensionStatusButStatusBlobAvailable

<!--issueDescription-->
We have identified that your backup operation failed because IaaS VM (with Linux OS) backup extension execution was stuck or crashed or the system calls might have timed out.
<!--/issueDescription-->

## **Recommended Steps**

1. Check if the VM is Linux and has more number of disks (disks count greater than 4). If yes, turn on sequential snapshot by following the below steps:

    -	Go to file */etc/azure/vmbackup.conf* and under [SnapshotThread]<br>
    -	Set the config value: *seqsnapshot = 2*
  
2. If the OS Version is Oracle Linux 7.6 and VM gets stuck during backup then please follow the below steps to mitigate the issue.

    -	Exclude temp disk from snapshots:<br>
    -	Check for mount path for Azure temporary disk. Generally it is */mnt/resources*
    -	Go to file */etc/azure/vmbackup.conf* and under [SnapshotThread]<br>
    -	Set the config value: *MountsToSkip = /mnt/resources*
