<properties
	pageTitle="ExtensionOperationFailed"
	description="ExtensionOperationFailed"
	infoBubbleText="VMSnapshot extension operation failed"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-extensionoperationfailed"
	diagnosticScenario="azurebackup-crc-extensionoperationfailed"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ExtensionOperationFailed

<!--issueDescription-->
We have identified that the backup operation failed because of the missing **Microsoft.Azure.RecoveryServices.VMSnapshot** extension manifest file.
<!--/issueDescription-->

## **Recommended Steps**

* To resolve this issue, reinstall the extension manifest file. Extract this file from `C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot\1.0.57.0\Microsoft.Azure.RecoveryServices.VMSnapshot_1.0.57.0.zip`, and copy it to `C:\Packages\Plugins\Microsoft.Azure.RecoveryServices.VMSnapshot\<version>\`.

**NOTE**: To prevent this from re-occurring, the customer needs to find out which program (anti-virus/malicious-software) is deleting these files and take appropriate action (i.e. remove/disable that program).
