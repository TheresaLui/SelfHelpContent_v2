<properties
	  pageTitle="Customer is facing an AAD Auth issue."
	  description="Customer is facing an AAD Auth issue."
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
	  articleId="327e1d97-3cce-41ae-8a81-a478b0fdd8bc"
	  ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Customer is facing an AAD Auth issue.

"Now that we have verified this to be an AAD Auth issue, lets get to the troubleshooting. AAD Auth issues on the storage account can be of two types. **Control Plane** issues or **Data Plane** issues. Please confirm if the customer is facing a control plane issue or a data plane issue.

**Control plane** issues are failures customer run into while trying to manage/configure their storage account. These failures will occur if the user does not have appropriate Azure Resource Manager role(Owner, Contributor, Reader, etc) assigned to their storage account. One of the common scenario is when the user is not able to see their storage account in portal. Assigning Data Roles to a user will not grant them permissions to manage the resource on portal. [Read this for more details.](https://docs.microsoft.com/azure/storage/common/storage-auth-aad#data-access-from-the-azure-portal)

**Data plane** issues are failures customer run into while trying to access data in their storage account. These failures will occur if the user does not have appropriate Data Plane roles assigned to their storage account. Assigning Azure Resource Manager roles does not grant access to Data in the storage account. [Read this for more details.](https://docs.microsoft.com/en-us/azure/storage/common/storage-auth-aad#azure-built-in-roles-for-blobs-and-queues)"

