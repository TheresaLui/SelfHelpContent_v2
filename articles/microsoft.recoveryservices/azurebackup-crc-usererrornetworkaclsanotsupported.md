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
	cloudEnvironments="public"
/>

# Error UserErrorNetworkAclSANotSupported

<!--issueDescription-->
We have identified that restore operation are failing due to the managed disk VMs where a user has selected a network restricted storage account for the restore operation which is not a supported scenario. Restore for Network restricted storage account is only supported for un-managed VMs.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the below:
* Go to Azure portal -> Storage Account -> Firewall and Virtual Networks and check if access is allowed for selected network or/and any IP address is added in firewall to restrict the access to the storage account.
* If storage account is restricted with firewall and Virtual Networks, then remove the restrictions from the storage account or choose a different storage account without any restriction for restoration.
