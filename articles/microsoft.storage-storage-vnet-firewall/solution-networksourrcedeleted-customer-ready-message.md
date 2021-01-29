<properties
	pageTitle="NetworkSourrceDeleted Customer Ready Message"
	description="NetworkSourrceDeleted Customer Ready Message"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="afc6d2a3-b5a1-4790-90ef-0a008e3dc4ff"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# NetworkSourrceDeleted Customer Ready Message

<!--issueDescription-->

### Customer Message

The NetworkSourceDelete error usually happens when a Firewall ACL had been created with a Subnet that was deleted afterwards. You may experience this error when a Subnet with the same name as the previosuly deleted one is recreated and you attempt to add it as a new Firewall ACL in other Storage Account.

You can resolve this issue by removing the ACLs with NetworkSourceDelete from the Storage Accounts that the error message displays.

For the below example, to resolve the issue the ACL for "default" Subnet needs to be removed from the Storage Account Firewall of "mystorageaccount" Storage Account.

{"responseBody":"{\"error\":{\"code\":\"NetworkAclsNetworkSourceDeleted\",\"message\":\"NetworkAcls VirtualNetworkRule /subscriptions/<SubscriptionId>/resourceGroups/myresourcegroup/providers/microsoft.network/virtualNetworks/myvnet/default with state NetworkSourceDeleted in accounts mystorageaccount is required to be removed before it can be added again.\"}}"}

<!--/issueDescription-->

