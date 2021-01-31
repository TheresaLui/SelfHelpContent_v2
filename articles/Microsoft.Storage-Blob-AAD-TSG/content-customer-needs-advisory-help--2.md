<properties
	  pageTitle="Customer needs advisory help."
	  description="Customer needs advisory help."
      service="Microsoft.Storage"
      resource="Microsoft.Storage/storageAccounts,Microsoft.ClassicStorage/storageAccounts"
	  authors="yagohel23"
	  ms.author="yagohel"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds="32679285,32679299,32679292,32678715"
	  resourceTags=""
	  productPesIds="16459,16461,15629,16598"
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="9913d2e9-78a3-4e8a-9e15-316d0e8d25eb"
	  ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Customer needs advisory help.

Some common customer questions on this topic are listed below with their answers. If you do not find answers to the customer questions here, please escalate using the escalation process defined at the bottom of this card. 

1. **How can we setup Storage Explorer such that a user has access only to a particular container?** Storage Explorer now has a feature which lets users connect directly to a particular container using AAD Authentication. Make sure the customer is using the latest version of the tool. [Please visit.](https://docs.microsoft.com/azure/vs-azure-tools-storage-manage-with-storage-explorer?tabs=windows#add-a-resource-via-azure-ad)

2. **How can we verify which user/application is accessing my data?** Customers can setup Azure Monitor based Diagnostics logs on their Storage Account to log all the Blob/Queue Storage operations happening on their Storage Account. In these logs, if AAD Auth is used, customers can find the AAD Object ID of the user/application which accessed their data. More details on this can be [found here](https://docs.microsoft.com/azure/storage/blobs/monitor-blob-storage-reference#resource-logs-preview).

3. **How long would a new Role Assignments take to propagate?** Azure role assignments may take up to five minutes to propagate. If you notice a certain role assignment taking longer to propagate, we may need to engage the EEEs/PG to have a look at the same. 

4. **How to generate a SAS token using a user's Azure AD credentials?** Customers can create user delegation SAS tokens for this purpose. A user delegation SAS is supported for Azure Blob storage and Azure Data Lake Storage Gen2. [Visit this for more details](https://docs.microsoft.com/rest/api/storageservices/create-user-delegation-sas). 


Apart from this, the following resources can also be reviewed for other generic questions regarding Azure AD Authentication. 

1. [Information on built-in roles, permissions needed for various data operations & setting up RBAC permissions can be found here.](https://docs.microsoft.com/azure/storage/common/storage-auth-aad#access-data-with-an-azure-ad-account)

2. [Information on how to authorize using VM/VMSS managed identities can be found here.](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-msi)

3. [Information on how to authorize using a client application.](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-app?tabs=dotnet)

4. [RBAC permissions needed for calling Blob and Queue Data Operations](https://docs.microsoft.com/rest/api/storageservices/authorize-with-azure-active-directory#permissions-for-calling-blob-and-queue-data-operations)

## Escalation

If the information above is not enough to answer customer questions, please reach out to your TAs through the [Ava Teams channel.](https://teams.microsoft.com/l/channel/19%3a3e1c65a38017478b86ad318bf03a1f65%40thread.skype/Storage?groupId=8a6a0fe1-0d7d-41a0-93f0-0fd7af9ac2c8&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47)

