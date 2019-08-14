<properties
pageTitle="Storage blob container(s) might be recoverable"
description="Some storage blob container(s) might be recoverable"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_blobContainer_recovery_maybe_multiple"
diagnosticScenario="Some storage blob container(s) might be recoverable"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>
# Blob Container may be recoverable

### Blob Container(s) recovered

Microsoft Azure were able to successfully recover the following deleted blob container(s) in storage account _**{ResourceName}**_:<br>

_**[List recovered blob container(s)]**_


### Unable to recover blob container(s)

We sincerely apologizes that we are unable to recover the following deleted blob container(s) in storage account _**{ResourceName}**_:<br>

_**[List container(s) that are not recoverable]**_

As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. This Blob Container and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidently deleted content can be recovered in the future.
