<properties
pageTitle="Soft delete used capacity"
description="Soft delete used capacity"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="Sijia"
ms.author="siz"
displayOrder=""
articleId="Storagev2insights_monitor_softdelete_capacity"
diagnosticScenario="Check soft delete capacity"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Transfer data with AzCopy v10

<!--issueDescription-->
Storage capacity spike may due to soft delete capacity. If you have soft delete is enabled and there are a lot of delete operations happened recently, you may have high capacity caused by soft delete. 
When data is deleted, it transitions to a soft deleted state instead of being permanently erased. When soft delete is on and you overwrite data, a soft deleted snapshot is generated to save the state of the overwritten data. Soft deleted objects are invisible unless explicitly listed. You can configure the amount of time soft deleted data is recoverable before it is permanently expired.
<!--/issueDescription-->

