<properties
pageTitle="Storage account name already taken"
description="Storage account name is not unique within Azure"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_AccountCreationIssue_NameTaken"
diagnosticScenario="Storage account name already taken"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_AccountManagement"
/>

# Storage account name already taken
<!--issueDescription-->

Storage account name **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be used because it is already taken in Azure. Please create a new storage account with a different unique name.
<!--/issueDescription-->

[Storage accounts name must be globally unique across Azure](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-storage-account-name-errors). If you do not provide a unique name, you will receive an error:

```
Code=StorageAccountAlreadyTaken
Message=The storage account named mystorage is already taken.
```

## **Recommended Documents**

* [Storage accounts name must be globally unique across Azure](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-storage-account-name-errors)
