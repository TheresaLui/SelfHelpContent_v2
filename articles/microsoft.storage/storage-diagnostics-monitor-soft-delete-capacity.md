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
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Soft delete capacity caused Storage capacity spike

<!--issueDescription-->
Storage capacity spike may due to soft delete capacity. If you have soft delete enabled and there are a lot of delete operations happened recently or soft delete retention time period is set for long, you may have high capacity or low performance for some operations caused by soft delete. You can configure the amount of time soft deleted data is recoverable before it is permanently expired. 
<!--/issueDescription-->

