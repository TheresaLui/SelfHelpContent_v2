﻿<properties
pageTitle="Unable to delete due to active lease with no attached VM"
description="Stray lease or CRP lock exists on Storage resource"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_UnableToDelete_Lease"
diagnosticScenario="Leased page blobs without an attached VM"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# Cannot delete <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** due to one or more active lease(s)

<!--issueDescription-->
The <!--$ResourceType-->[ResourceType]<!--/$ResourceType--> **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** cannot be deleted because it contains one or more active lease(s) associated with it. In order to delete the  <!--$ResourceType-->[ResourceType]<!--/$ResourceType-->, you must first [break the lease(s)](https://azure.microsoft.com/updates/support-for-blob-storage-lease-management-from-azure-portal/) of resources listed below:<br>

<!--$LeasedResourcesList-->[LeasedResourcesList]<!--/$LeasedResourcesList-->

<!--/issueDescription-->
