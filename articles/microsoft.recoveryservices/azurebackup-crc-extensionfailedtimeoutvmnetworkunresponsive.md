<properties
	pageTitle="extensionfailedtimeoutdelayinnetwork"
	description="extensionfailedtimeoutdelayinnetwork"
	infoBubbleText="Snapshot operation failed due to delay in network calls made to take disk blob-snapshots."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	articleId="azurebackup-crc-extensionfailedtimeoutvmnetworkunresponsive"
	diagnosticScenario="azurebackup-crc-extensionfailedtimeoutvmnetworkunresponsive"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ExtensionFailedTimeoutVMNetworkUnresponsive

<!--issueDescription-->
Backup operation failed due to a delay in network calls while performing the snapshot operation.
<!--/issueDescription-->

## **Recommended Steps**

We have detected that your backup operation failed due to a delay in network calls while performing the snapshot operation.

To resolve this issue, perform Step 1. If the issue persists, try steps 2 and 3.

1. Create snapshot through Host. From an elevated (admin) command-prompt, run the below command:

```
REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgentPersistentKeys" /v SnapshotMethod /t REG_SZ /d firstHostThenGuest /f
REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgentPersistentKeys" /v CalculateSnapshotTimeFromHost /t REG_SZ /d True /f
```

This will ensure the snapshots are taken through host instead of Guest. Retry the backup operation.

2. Try changing the backup schedule to a time when VM is under less load (less CPU/IOps etc.)
3. Try [increasing the size of VM](https://azure.microsoft.com/blog/resize-virtual-machines/) and retry the operation
