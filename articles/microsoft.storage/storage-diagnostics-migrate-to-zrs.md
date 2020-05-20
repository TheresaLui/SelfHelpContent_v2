<properties
pageTitle="Migrate to ZRS within a region"
description="Migrate to ZRS within a region"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="Sijia"
ms.author="siz"
displayOrder=""
articleId="storagev2insights_datamigration_migratetozrswithinaregion"
diagnosticScenario="Migrate to ZRS within a region"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Migrate to ZRS within a region

<!--issueDescription-->
Changing redundancy type to zone redundant storage (ZRS) involves moving the physical data from a single storage stamp to multiple stamps within a qualified region. Live migration is only supported for Standard accounts. Premium accounts are not supported.
<!--/issueDescription-->

## **Recommended Steps**

1. Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** is in [RegionName], which is not in a qualified region. We were unable to successfully migrate Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. Please check [Qualified Region](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs#support-coverage-and-regional-availability) for more information.

2. Unable to migrate Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** to ZRS due to account type is premium



