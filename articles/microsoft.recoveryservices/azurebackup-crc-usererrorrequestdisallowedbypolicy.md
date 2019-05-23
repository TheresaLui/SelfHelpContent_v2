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
	cloudEnvironments="public"
/>

# Error UserErrorRequestDisallowedByPolicy

<!--issueDescription-->
## We have identified an Azure Resource Manager policy configured on the resource group is preventing backup service to initiate the backup/restore operation.
<!--/issueDescription-->

## **Recommended Steps**
To resolve UserErrorRequestDisallowedByPolicy ensure configured ARM policy is not blocking the backup/restore operation. Your subscription administrators might assign policies that limit how resources are deployed. This error can happen if an ARM policy is configured on the resource group preventing the backup service to initiate the backup/restore operation.
To resolve the issue follow these steps:<br/>
* From the Azure portal navigate to the resource group in which the recovery service vault exist.  
*	From Settings, click Policies and check if any policy is created which could leads to backup/restoration failure.  
*	If any ARM Policy is exist, then ensure policy doesn’t block the backup/restore and retry the operation.
