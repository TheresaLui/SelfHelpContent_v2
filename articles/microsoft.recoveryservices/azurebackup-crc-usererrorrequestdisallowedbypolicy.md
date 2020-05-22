<properties
	pageTitle="UserErrorRequestDisallowedByPolicy"
	description="UserErrorRequestDisallowedByPolicy"
	infoBubbleText="An invalid policy is configured on the VM which is preventing Snapshot operation."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorrequestdisallowedbypolicy"
	diagnosticScenario="azurebackup-crc-usererrorrequestdisallowedbypolicy"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorRequestDisallowedByPolicy

<!--issueDescription-->
We have identified that an Azure Resource Manager policy configured on the resource group is preventing the backup service from initiating the backup/restore operation.
<!--/issueDescription-->

## **Recommended Steps**

* Ensure the configured ARM policy is not blocking the backup/restore operation. Your subscription administrators might assign policies that limit how resources are deployed. This error can happen if an ARM policy is configured on the resource group preventing the backup service to initiate the backup/restore operation. To resolve the issue follow these steps:

	* From the Azure portal, navigate to the resource group in which the recovery service vault exists
	* From **Settings**, click **Policies** and check if any policy is created which could leads to backup/restoration failure
	* If any **ARM Policy** exists, ensure the policy doesn’t block the backup/restore and retry the operation
