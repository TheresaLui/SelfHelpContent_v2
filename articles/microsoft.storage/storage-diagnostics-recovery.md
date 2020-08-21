<properties
pageTitle="Storage resource recovery"
description="Storage resource recovery"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="sijia"
ms.author="siz"
displayOrder=""
articleId="Storagev2insights_recovery"
diagnosticScenario="Storage resource recovery"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Storage resource cannot be recovered

<!--issueDescription-->

Storage resource **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** recovery is not possible. This may due to the reason below.

Storage resource with the same name has been created since deletion.
Soft delete is not enabled and deletion has been over the time period which recovery is possible.
Deletion happened before soft delete retention period.

<!--/issueDescription-->

Please check Recommended Solution below for recovery condition for different scenario.
