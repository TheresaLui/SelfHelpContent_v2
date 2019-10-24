﻿<properties
pageTitle="File open handles limit exceeded"
description="Too many file handles are open"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_file_openHandlesLimit"
diagnosticScenario="File open handles limit exceeded"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# File open handles limit exceeded on <!--$FileType-->[FileType]<!--/$FileType-->

<!--issueDescription-->
The <!--$FileType-->[FileType]<!--/$FileType--> **<!--$FileName-->[FileName]<!--/$FileName-->** has <!--$FileHandleCount-->[FileHandleCount]<!--/$FileHandleCount--> open handles which meets or exceeds the open handles limit per file. Please reduce the number of open handles by closing the file if it is no longer in use. If you need our assistance closing these open handles from the Azure Files service, please let us know.
<!--/issueDescription-->

For more information on the scalability and performance targets of Azure Files, refer to the article [Azure Files scale targets](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets#azure-files-scale-targets). 



