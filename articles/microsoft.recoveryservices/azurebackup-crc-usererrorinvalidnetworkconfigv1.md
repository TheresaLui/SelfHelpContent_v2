<properties
	pageTitle="UserErrorInvalidNetworkConfigV1"
	description="UserErrorInvalidNetworkConfigV1"
	infoBubbleText="Invalid VM network Configuration"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorinvalidnetworkconfigv1"
	diagnosticScenario="azurebackup-crc-usererrorinvalidnetworkconfigv1"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorInvalidNetworkConfigV1

<!--issueDescription-->
We have identified that your backup operation are failed because you are using a Classic VMs, where the RDFE service does not support UpdateExtension operation.
<!--/issueDescription-->

## **Recommended Step**
As a workaround to resolve this issue, you can backup by shutting down the virtual machine and starting it back when the snapshot operation is over.
