<properties
	pageTitle="Check for Sync Agent Certificate Errors"
	description="Check for Sync Agent Certificate Errors"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32675708"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b9bb1805-92d0-4bf7-ac67-4d09b7d265c1"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# How to check for Sync Agent Certificate Errors

1. At this point go to event viewer log located under Applications and Services\Microsoft\FileSync\Agent in Event Viewer, check Operational
2. Look for an Error with Event ID 4030.  
3. It will have description text that begins with
  
~~~powershell

GetAllChanges failed. Local share name: myfilesyncsvc_mysyncgrp_<server_id>. PartnershipId: 1

~~~

4. If you see an Error Event ID 4030 with a description similar to the above it indicates that the issue is with the certificate and troubleshooting is covered in our troubleshooting guide at the link below

## **Recommended Documents**

1. [Troubleshooting Guide](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#-2134375680)