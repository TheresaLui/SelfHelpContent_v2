<properties
pageTitle="File handle limit exceeded"
description="Too many file handles are open"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_file_openHandlesLimit"
diagnosticScenario="File handle limit exceeded"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="public"
/>

# File handle limit exceeded on <!--$FileType-->[FileType]<!--/$FileType-->

<!--issueDescription-->
Storage <!--$FileType-->[FileType]<!--/$FileType--> **<!--$FileName-->[FileName]<!--/$FileName-->** has <!--$FileHandleCount-->[FileHandleCount]<!--/$FileHandleCount--> open handles which meets or exceeds the maximum open handles limit per file. For more information, see [Azure Files scale targets](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-scale-targets#azure-files-scale-targets). Please reduce the number of concurrent open handles by closing them. Our support team has the ability to force close all handles in a <!--$FileType-->[FileType]<!--/$FileType-->. Let your support engineer know if you would like all file handles to be force closed.<br>
<!--/issueDescription-->
