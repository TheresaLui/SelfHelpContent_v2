<properties
	pageTitle="Permission denied accessing job input or output data"
	description="When you attempt to write the input data for a job or read the output data for a job you receive a permission denied (403 Forbidden) error"
	infoBubbleText="Permission issues when reading input or output data"
	service="microsoft.quantum"
	resource="workspaces"
	ms.author="mblouin"
	displayOrder=""
	articleId="quantum-permissions-storageaccount"
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds=""
	resourceTags=""
	productPesIds="17040"
	cloudEnvironments="public"
	ownershipId=""
/>

# Permission denied accessing job input or output data

Job input and output data is stored in an Azure Storage account deployed in the same subscription as your workspace. This storage account is associated with the Quantum Workspace at creation time. 

As the storage account remains a separate resource you may experience various types of permission issues tyring to access it. 


## **Recommended Steps**

1. Review the input and output data links on the job that you are trying to access. They contain the storage account name as part of the URL.
2. Review the permission settings on the storage account.
3. To reconfigure permissions, please follow the documentation around [storage account permissions] (https://docs.microsoft.com/azure/storage/common/storage-access-blobs-queues-portal)

## **Recommended Documents**

TODO: Add Documentation Links
* [This is the display text of an external document](https://)
* [Storage account permissions] (https://docs.microsoft.com/azure/storage/common/storage-access-blobs-queues-portal)

### Notes

* The **Recommended Steps** and **Recommended Documents** headings must be entered as shown above (bolded H2)
* Formatting is not identical to Microsoft Docs - tables do not work, nor [!NOTE] tags
* Your Recommended Steps should be actual steps, not just links to other articles
* Ensure all links to Microsoft docs are non-region-specific, i.e. does not include /en-us/. This does not apply to articles for Mooncake.
* Don't link to internal review documentation - these URLs always start with "review.microsoft.docs", and users are unable to access them
* Do not use aka.ms links
* Copy the raw form of this article to use as a template for your own Common Solution article. Be sure to fill in the metadata!
