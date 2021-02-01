<properties
	  pageTitle="Customer is facing a control plane issue. "
	  description="Customer is facing a control plane issue. "
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
	  articleId="f953e78d-e97f-49db-baea-f5f60cfa8f1b"
	  ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Customer is facing a control plane issue. 

**Control plane** issues like customers not being able to see their account or not being able to update storage configs will happen if the user does not have appropriate Resource Manager Role assigned on the storage account. In such cases, the user will not be able to see their storage account on the portal or in Storage Explorer when they connect to their subscription using their AAD Credentials. 

In order to access data through portal, the Azure portal first checks whether you have been assigned an Azure role with **Microsoft.Storage/storageAccounts/listkeys/action**. The built-in roles provided by Azure Storage grant access to blob and queue resources, but they don't grant permissions to storage account resources. For this reason, access to the portal also requires the assignment of an Azure Resource Manager role such as the **Reader** role, scoped to the level of the storage account or higher. The **Reader** role grants the most restricted permissions, but another Azure Resource Manager role that grants access to storage account management resources is also acceptable.Customer can choose to create their own custom role which includes the following permission: **Microsoft.Storage/storageAccounts/listkeys/action**. 

Verify if the user in question has this permission on the storage account. Using the failure you found in dgrep, identify the user identity using the **UserObjectID** column. Once you know the objectID of the user, use ASC to verify if the user has appropriate control plane permission.

1. Navigate to customer's storage account in ASC Resource Explorer
2. Navigate to **Access Control** tab and plug in user's ObjectID in the **Check Access** option and run it.
3. You will be able to see user's RBAC permissions on that particular storage account. 
4. Verify if the user has Owner/Contributor/Reader resource manager role assigned to them or have a customer role assigned to them which provides **Microsoft.Storage/storageAccounts/listkeys/action** permission. The scope of this permission should be at the storage account level or higher. These permissions at the container wont help.
5. If the user does not have above permission, please ask them to work with the owner of their storage account to get it. That should help resolve the issue. 
6. If the user has appropriate permissions but they still dont see the storage account, please escalate the ticket to the TA.

