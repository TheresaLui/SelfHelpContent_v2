<properties
	pageTitle="Time Based Retention Policy"
	description="Time Based Retention Policy"
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
	articleId="9b728421-bdfc-470d-91fd-4147fdacfaa2"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Time Based Retention Policy
<!--issueDescription-->
We've researched your case and believe the issue is due to a time based retention policy set on the resource. This time based retention policy is set by you or someone in your organization due to legal hold or regulatory compliance reasons. We cannot remove the policy from the backend due to Regulatory compliance.

* **Regulatory compliance**: Immutable storage for Azure Blob storage helps organizations address SEC 17a-4(f), CFTC 1.31(d), FINRA, and other regulations
* **Time-based retention policy support**: Users set policies to store data for a specified interval
* **Legal hold policy support**: When the retention interval is not known, users can set legal holds to store data immutably until the legal hold is cleared. When a legal hold is set, blobs can be created and read, but not modified or deleted. Each legal hold is associated with a user-defined alphanumeric tag that is used as an identifier string (such as a case ID).
* **Support for all blob tiers**: WORM policies are independent of the Azure Blob storage tier and apply to all the tiers: hot, cool, and archive. Users can transition data to the most cost-optimized tier for their workloads while maintaining data immutability.<br>
<br>
Further information at [Blob Immutable Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-immutable-storage)<br>
<br>
<br>
If further assistance is required, please engage Azure Dev Storage team.

<!--/issueDescription-->

## **Recommended Documents**

1. [Store business-critical blob data with immutable storage](https://docs.microsoft.com/azure/storage/blobs/storage-blob-immutable-storage#time-based-retention-policies)
2. [Blob Immutable Storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-immutable-storage)