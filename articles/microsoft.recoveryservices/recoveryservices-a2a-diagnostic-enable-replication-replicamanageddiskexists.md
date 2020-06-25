<properties
	pageTitle="Enable replication failed as virtual machine's disk was previously protected"
	description="Failed to enable replication because the replica of disk is already exists"
	infoBubbleText="Microsoft Azure has information regarding your issue. Please see details on the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="genlin"
	ms.author="asgang"
	displayOrder=""
	articleId="ASR_A2A_EnableReplicationFailure_ReplicaManagedDiskExists"
	diagnosticScenario="ASRA2AMgmtFailures"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Enable replication failed as virtual machine's disk was previously protected
<!--issueDescription-->
Failed to enable replication for the virtual machine <!--$vmname-->[vmname]<!--/$vmname--> with error 150161. This problem can occur if the virtual machine was previously protected, and the replica disk was not cleaned when the replication was disabled.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, delete the replica disk that identified in the error message and then try to enable replication again.
