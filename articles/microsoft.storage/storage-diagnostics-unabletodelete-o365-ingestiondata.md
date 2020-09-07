<properties
pageTitle="Unable to delete storage resource due to Office 365 Import Service"
description="ingestiondata blob container is preventing deletion of this storage resource"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_UnableToDelete-o365-IngestionData"
diagnosticScenario="Unable to delete storage due to Office 365 Import Service"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to Office 365 Import Service

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be deleted because it contains data added by **Office 365 PST Import service**. The Network upload option was selected for the O365 Import service which created **ingestdata** blob container. This container is used as a temporarily location for the PST files before they are ingested to your **Office** organization. The container will be automatically cleaned up 30 days after the most recent PST file has been uploaded after which it can be deleted.
<!--/issueDescription--> 

For more information, see [Office 365 Import Service](https://docs.microsoft.com/office365/securitycompliance/importing-pst-files-to-office-365).

Let us know if you need to delete this container before the 30 day period. Please note that any pending import from this container to your _Office 365_ organization might be impacted after the deletion.  


