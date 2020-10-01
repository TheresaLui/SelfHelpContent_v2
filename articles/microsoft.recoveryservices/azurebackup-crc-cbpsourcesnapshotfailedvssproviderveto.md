<properties
	pageTitle="CBPSourceSnapshotFailedVSSProviderVETO"
	description="CBPSourceSnapshotFailedVSSProviderVETO"
	infoBubbleText="Backup failed because the VSS service encountered an error. This could be a transient problem"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbpsourcesnapshotfailedvssproviderveto"
	diagnosticScenario="azurebackup-crc-cbpsourcesnapshotfailedvssproviderveto"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# CBPSourceSnapshotFailedVSSProviderVETO 

<!--issueDescription-->
Your backup operation failed because there might be a disk management policy that is preventing the discs from being displayed ONLINE.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, ensure that the Disk Management Policy is set to display all the discs ONLINE<br>
1. To check the current SAN policy, open an elevated command prompt by typing `cmd` in the Run window and run `diskpart` command. This will prompt the diskpart window<br>
2. In the diskpart prompt execute the command `SAN`<br>
3. If the output displayed **SAN Policy: Online All**, then the disk management policy is set correctly<br>
4. If the policy is not set correctly then it needs to be updated. Update the policy by executing the command `SAN POLICY=OnlineAll`
