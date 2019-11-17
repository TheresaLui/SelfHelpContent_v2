<properties
pageTitle="Sync failed error -ECS_E_SYNC_BLOCKED_ON_SUSPENDED_SUBSCRIPTION "
description="Sync failed error - ECS_E_SYNC_BLOCKED_ON_SUSPENDED_SUBSCRIPTION"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="FileSync_FailedError_ECS_E_SYNC_BLOCKED_ON_SUSPENDED_SUBSCRIPTION"
diagnosticScenario="Sync failed error - ECS_E_SYNC_BLOCKED_ON_SUSPENDED_SUBSCRIPTION"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Azure File Sync failed error - ECS_E_SYNC_BLOCKED_ON_SUSPENDED_SUBSCRIPTION
<!--issueDescription-->
Sync failed for one or more server endpoints under the Storage Sync Service resource  **<!--$storageSyncServiceName-->[storageSyncServiceName]<!--/$storageSyncServiceName-->** due to **error code 0x80C83076 or -2134364042**. This error occurred between **<!--$startTime-->[startTime]<!--/$startTime-->** and **<!--$endTime-->[endTime]<!--/$endTime-->**.<br/><br/>This error occurs when the Azure subscription is suspended. Sync will be reenabled when the Azure subscription is restored.<br/><br/>
<!--/issueDescription-->

## **Recommended Documents**
See [Why is my Azure subscription disabled and how do I reactivate it?](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable) for more information.

