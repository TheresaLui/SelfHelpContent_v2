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
	cloudEnvironments="Public"
/>

# Enable replication failed as machine's disk size is not meet the requirement
<!--issueDescription-->
Failed to enable replication for the machine <!--$vmname-->[vmname]<!--/$vmname--> with error 28109. This issue can occur if the disk size of the machine is smaller than the minimum size required, or the disk type is unsupported such as BitLocker encrypted disk.
<!--/issueDescription-->

## **Recommended Steps**

- Make sure that the disk size of the machine is larger than 1 GB. To resize the disk size for an Azure virtual machine, see [How to expand the disk of a virtual machine
](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resize-a-managed-disk).
- Remove the BitLocker encrypted disk or turn off the encryption.