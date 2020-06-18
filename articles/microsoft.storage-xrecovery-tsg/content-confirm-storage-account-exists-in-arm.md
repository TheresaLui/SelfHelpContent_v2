<properties
	pageTitle="Confirm that the storage account appears in ARM"
	description="Confirm that the storage account appears in ARM"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="a68f00f6-8f2f-4e6a-97b8-c605b662ab94"
/>

# Confirm that the storage account appears in ARM

1. Navigate to Geneva Actions (Jarvis Actions) : [Azure Resource Manager > Resource Group Management > Synchronize Subscription resources from specific resource provider](https://jarvis-west.dc.ad.msft.net/B7BF0B48?genevatraceguid=b7ab48f0-5c87-405b-af1a-a01ad587b009)
2. Fill in the requested information and provide Resource Provider Namespace as "Microsoft.Storage"
3. Hit "Run".
4. The response may be paged.
	1. If the resource is not found, find "nextLink" at the end of the response body.
	2. paste that in the 'Query String (Optional)' field, and hit "Run" again.
	3. Repeat until the resource is found or the end of the list is reached.
5. Note that there may be some delay between when Synchronization is run and when the resource appears. If the resource does not appear even after 60 minutes, engage WASU with an IcM.

## Recommended Documents

1. [WASU Storage Recovery IcM Template](https://icm.ad.msft.net/imp/v3/incidents/create?tmpl=V3F2C9)
