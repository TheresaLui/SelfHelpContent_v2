<properties
	pageTitle="UserErrorNetworkAclSANotSupported"
	description="UserErrorNetworkAclSANotSupported"
	infoBubbleText="Network Acl Storage Account Not Supported"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrornetworkaclsanotsupported"
	diagnosticScenario="azurebackup-crc-usererrornetworkaclsanotsupported"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorNetworkAclSANotSupported

<!--issueDescription-->
We have identified that the restore operation has failed. The managed disk VM has selected a network-restricted storage account for the restore operation, which is not a supported scenario. This feature is only supported for un-managed VMs.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the below:

* Go to Azure portal -> Storage Account -> Firewall and Virtual Networks and check if access is allowed for the selected network
* Ensure the IP address is added as an exception to the firewall settings that restrict the access to the storage account
* If storage account is restricted with firewall and Virtual Networks, then remove restrictions from the storage account or choose a different storage account without any restriction for restoration
