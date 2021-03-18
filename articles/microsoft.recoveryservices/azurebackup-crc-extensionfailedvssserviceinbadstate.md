<properties
	pageTitle="ExtensionFailedVssServiceInBadState"
	description="ExtensionFailedVssServiceInBadState"
	infoBubbleText="Snapshot operation failed due to VSS Writers in bad state"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-extensionfailedvssserviceinbadstate"
	diagnosticScenario="azurebackup-crc-extensionfailedvssserviceinbadstate"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ExtensionFailedVssServiceInBadState

<!--issueDescription-->
We have detected that your VSS (Volume Shadow copy Service) service is in an inconsistent state.
<!--/issueDescription-->

## **Recommended Steps**

Restart VSS (Volume Shadow Copy) service.

- Navigate to Services.msc and restart 'Volume Shadow Copy service'.<br>
(or)<br>
- Run the following commands from an elevated command prompt:

 ```net stop VSS``` <br>
 ```net start VSS```

If the issue still persists, restart the VM at the scheduled downtime.
