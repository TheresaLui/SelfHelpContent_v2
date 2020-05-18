<properties
	pageTitle="No Access (403) when trying to delete an Azure File Share"
	description="No Access (403) when trying to delete an Azure File Share"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1fcba446-43d0-4ea6-8f31-24417f9b5c40"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# No Access (403) when trying to delete an Azure File Share

<!--issueDescription-->
We've researched your case and believe that the unable to delete issue is due to [Azure Firewall](https://docs.microsoft.com/en-us/azure/storage/common/storage-network-security) being enabled on your storage account and the source IP/Public IP of the connection not being whitelisted. In order to resolve this issue you must [whitelist the Public IP within the Firewall of the Storage Account](https://docs.microsoft.com/en-us/azure/storage/common/storage-network-security#grant-access-from-an-internet-ip-range).
<!--/issueDescription-->

## Recommended Documents

1. [Grant access from an internet IP range](https://docs.microsoft.com/en-us/azure/storage/common/storage-network-security#grant-access-from-an-internet-ip-range)
2. [Azure Firewall](https://docs.microsoft.com/en-us/azure/storage/common/storage-network-security)
