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
	cloudEnvironments="public"
	articleId="9b728421-bdfc-470d-91fd-4147fdacfaa2"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Time Based Retention Policy
<!--issueDescription-->
We've researched your case and believe the issue is due to a time based retention policy set on the resource. This time based retention policy is set by you or someone in your organization due to legal hold or regulatory compliance reasons. We cannot remove the policy from the backend due to Regulatory compliance.

Some more information is provided below. 

Regulatory compliance: Immutable storage for Azure Blob storage helps organizations address SEC 17a-4(f), CFTC 1.31(d), FINRA, and other regulations.
Time-based retention policy support: Users set policies to store data for a specified interval.
Legal hold policy support: When the retention interval is not known, users can set legal holds to store data immutably until the legal hold is cleared. When a legal hold is set, blobs can be created and read, but not modified or deleted. Each legal hold is associated with a user-defined alphanumeric tag that is used as an identifier string (such as a case ID).
<!--/issueDescription-->

## Recommended Documents

* [Store business-critical blob data with immutable storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-immutable-storage#time-based-retention-policies)