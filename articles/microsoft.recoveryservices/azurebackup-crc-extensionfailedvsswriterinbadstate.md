<properties
	pageTitle="ExtensionFailedVssWriterInBadState"
	description="ExtensionFailedVssWriterInBadState"
	infoBubbleText="Snapshot operation failed due to VSS Writers in bad state"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-extensionfailedvsswriterinbadstate"
	diagnosticScenario="azurebackup-crc-extensionfailedvsswriterinbadstate"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ExtensionFailedVssWriterInBadState

<!--issueDescription-->
We have identified that your snapshot operation failed due to the VSS (Volume Shadow copy Service) writer in a bad state.
<!--/issueDescription-->

## **Recommended Documents**

Step 1: Restart VSS writers that are in a bad state.

* From an elevated command prompt, run <br>
```vssadmin list writers```.
* The output contains all VSS writers and their state. For every VSS writer with a state that's not **[1] Stable**, restart the respective VSS writer's service.
* To restart the service, run the following commands from an elevated command prompt:

 ```net stop serviceName``` <br>
 ```net start serviceName```

> [!NOTE]
> Restarting some services can have an impact on your production environment. Ensure the approval process is followed and the service is restarted at the scheduled downtime.

Step 2: If restarting the VSS writers did not resolve the issue, then run the following command from an elevated command-prompt (as an administrator) to prevent the threads from being created for blob-snapshots.

```
console
REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgentPersistentKeys" /v SnapshotWithoutThreads /t REG_SZ /d True /f
```

If step 1 and 2 did not resolve the issue, follow the instructions in *Step 3* in this [article](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#extensionfailedvsswriterinbadstate---snapshot-operation-failed-because-vss-writers-were-in-a-bad-state)
