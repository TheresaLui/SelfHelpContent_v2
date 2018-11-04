<properties
pageTitle="Unable to delete storage resource due to classic image(s)"
description="There are classic image(s) in this storage resource that prevents deletion"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_UnableToDelete_Images_Classic"
diagnosticScenario="Unable to delete storage due to classic image(s)"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more classic image(s)

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be deleted because it contains one or more classic image(s). In order to delete the  <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->, you must first delete the following image(s): <br>

<!--$ImageList-->[ImageList]<!--/$ImageList-->

Alternatively, these images can be deleted during storage account deletion using [Azure Portal](https://portal.azure.com) with the _'Automatically delete unattached disks and images'_ option.

<!--/issueDescription-->
