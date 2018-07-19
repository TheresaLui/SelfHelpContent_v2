﻿<properties
pageTitle="Storage Blob Container maybe recoverable"
description="Storage Blob Container maybe recoverable"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_blobContainer_recovery_maybe"
diagnosticScenario="Storage Blob Container maybe recoverable"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>
# Blob Container may be recoverable

## Blob Container **<!--$ContainerName-->[ContainerName]<!--/$ContainerName-->** recovered

We were able to successfully recover Blob Container **<!--$ContainerName-->[ContainerName]<!--/$ContainerName-->** that was deleted:

- **<!--$ClientIp-->[ClientIp]<!--/$ClientIp-->**
- **<!--$DeletionTime-->[DeletionTime]<!--/$DeletionTime-->**

Microsoft may not always be able  to recover your data. You can follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that your deleted data will be recoverable in the future. 

---

## Unable to recover Blob Container **<!--$ContainerName-->[ContainerName]<!--/$ContainerName-->**

Microsoft Azure sincerely apologizes that we are unable to recover the Blob Container **<!--$ContainerName-->[ContainerName]<!--/$ContainerName-->** and all its contents that was deleted:

- **<!--$ClientIp-->[ClientIp]<!--/$ClientIp-->**
- **<!--$DeletionTime-->[DeletionTime]<!--/$DeletionTime-->**

As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. This Blob Container and all its content was cleaned up after deletion and is no longer recoverable by Azure.<br>

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidently deleted content can be recovered in the future.
