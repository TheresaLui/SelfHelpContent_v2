<properties
pageTitle="Unable to delete storage resource due to detached classic disk(s)"
description="There are detached classic disk(s) in this storage resource that prevents deletion"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_UnableToDelete_DiskDetached_Classic"
diagnosticScenario="Unable to delete storage due to detached classic disk(s)"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more classic disk(s)

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be deleted because it contains one or more classic disk(s) that are not attached to a VM. In order to delete the  <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->, you must first delete the following disk(s):<br>

<!--$DiskList-->[DiskList]<!--/$DiskList-->

Alternatively, these disks can be deleted during storage account deletion using [Azure Portal](https://portal.azure.com) with the _'Automatically delete unattached disks and images'_ option.

<!--/issueDescription-->
