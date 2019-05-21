<properties
	pageTitle="Microsoft Azure has information regarding your issue"
	description="Microsoft Azure has information regarding your issue"
	infoBubbleText="Microsoft Azure has information regarding your issue. Please see details to the right."
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="genlin"
	ms.author="asgang"
	displayOrder=""
	articleId="BootAndSystemPartitionNotOnSameDisk"
	diagnosticScenario="BootAndSystemPartitionNotOnSameDisk"
	selfHelpType="Diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="Public"
/>

# Fail to enable Site Recovery Mobility service on the virtual machine
<!--issueDescription-->
Failed to enable Site Recovery Mobility service on the virtual machine. The issue occurs because the virtual machine's Boot partition and system partition are not on the same disk.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, move the boot partition into the disk that hosts the system partition, and then enable the protection.

