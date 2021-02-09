<properties
	pageTitle="Confirm that the storage account appears in ARM"
	description="Confirm that the storage account appears in ARM"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="symondsk"
	ms.author="ksymonds"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
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
5. Note that there may be some delay between when Synchronization is run and when the resource appears. You can run a nslookup on the account FQDN, if it resolves to a cluster then it has been restored. 

```
c:\users\>nslookup xyzstoreacct123.blob.core.windows.net
Server: cdns01.ispcom.net
Address: 10.11.12.13

Non-authoritative answer:
Name:    blob.blz22prdstr02a.store.core.windows.net
Address:  55.222.111.111
Aliases:  xyzstoreacct123.blob.core.windows.net

```


If the resource does not appear after 60 minutes, engage **XStore/Location Service** team. If you don't have access to route the ICM to **XStore/Location service** team, engage one of the storage TAs or email cssstorageta@microsoft.com. \[https:// ICM\]

## Recommended Documents

1. [WASU Storage Recovery IcM Template](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=V3F2C9)
