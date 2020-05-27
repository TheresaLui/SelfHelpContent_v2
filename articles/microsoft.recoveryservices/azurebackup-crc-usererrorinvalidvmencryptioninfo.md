<properties
	pageTitle="UserErrorInvalidVMEncryptionInfo"
	description="UserErrorInvalidVMEncryptionInfo"
	infoBubbleText="Invalid Encryption information supplied for VM"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorinvalidvmencryptioninfo"
	diagnosticScenario="azurebackup-crc-usererrorinvalidvmencryptioninfo"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorInvalidVMEncryptionInfo

<!--issueDescription-->
We identified that your backup operation failed because of the invalid encryption information supplied for VM.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, follow the below:

- If you have previously used [Azure Disk Encryption with Azure AD](https://docs.microsoft.com/azure/security/azure-security-disk-encryption-prerequisites-aad) app to encrypt this VM, you will have to continue use this option to encrypt your VM
- You can’t use [Azure Disk Encryption](https://docs.microsoft.com/azure/security/azure-security-disk-encryption-prerequisites) on this encrypted VM as it is not a supported scenario. Switching away from AAD application for this encrypted VM isn’t supported yet.
