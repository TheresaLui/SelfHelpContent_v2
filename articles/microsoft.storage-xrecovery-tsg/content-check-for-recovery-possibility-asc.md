<properties
	pageTitle="Check for recovery possibility from ASC"
	description="Check for recovery possibility from ASC"
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
	articleId="6f987b08-daee-4d7a-8727-0f630dbf10c9"
/>

# Check for recovery possibility from ASC

1. Navigate to Resource Explorer in Azure Support Center and select the resource at the Subscription level(top resource).Choose the operations tab, set the timeframe when the account might have been deleted. If not sure, choose last 14 days. Older deletes are unlikely to be recoverable. Run the report.
2. Navigate to Resource Explorer and select the resource at the Subscription level(top resource).
3. Select Storage tab/section.
4. Fill the details of the Storage Account we are attempting to recover under the subsection Account Deletion History & Recovery and Run the query.
5. Review and follow the Recommended Actions and leverage the Customer Ready Message.
6. Possible ASC responses are:
    1. Unable to recover Storage Account
    2. Recovery of deleted Storage Account may be possible
