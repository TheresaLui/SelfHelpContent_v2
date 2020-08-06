<properties
	pageTitle="Enable replication failed due to unsupported disk size"
	description="Failed to enable replication because the disk size is not meet the requirement"
	infoBubbleText="Microsoft Azure has information regarding your issue. Please see details on the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="genlin"
	ms.author="asgang"
	displayOrder=""
	articleId="ASR_A2A_EnableReplicationFailure_DiskSizeLessThanMinimum"
	diagnosticScenario="ASRA2AMgmtFailures"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="Compute_SiteRecovery"
/>

# Enable replication failed as virtual machine's disk size is not meet the requirement
<!--issueDescription-->
Failed to enable replication for the virtual machine <!--$vmname-->[vmname]<!--/$vmname--> with error 28109. This problem can occur if the disk size is smaller than the minimum size required, or the disk type is unsupported such as BitLocker encrypted disk.
<!--/issueDescription-->

## **Recommended Steps**

To resolve the issue, follow these steps:

1. Make sure that the disk size of the virtual machine is larger than 1 GB. To resize the disk size, see [How to expand the disk of a virtual machine](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resize-a-managed-disk).
2. Remove the BitLocker encrypted disk or turn off the encryption
