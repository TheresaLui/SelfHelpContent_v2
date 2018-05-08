<properties
pageTitle="Cannot recover container"
description="Cannot recover container - not GRS/RA-GRS"
infoBubbleText="Cannot recover container"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_blob_recovery_CannotRecoverContainer"
diagnosticScenario="Cannot recover container - not GRS/RA-GRS"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# **Cannot recover container of this type**

<!--issueDescription-->
Microsoft Azure identified that Container **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** and all its content are not recoverable. We use the geo-replicated copy of the Container for recovery. Since this storage account is not GRS/RA-GRS, recovery is not possible. <br>

Please follow our [Best Practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) or [Designing Highly Available Applications using RA-GRS](https://docs.microsoft.com/azure/storage/common/storage-designing-ha-apps-with-ragrs) to ensure that your deleted data will be recoverable in the future. <br>

Regards,<br>
Microsoft Azure Team
<!--/issueDescription-->
