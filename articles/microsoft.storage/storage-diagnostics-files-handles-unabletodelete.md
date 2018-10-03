<properties
pageTitle="Unable to delete file due to open handles"
description="File handles must be closed before deletion"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_unableToDelete_file_openHandles"
diagnosticScenario="Open file handles prevents file deletion"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="public"
/>

# Unable to delete <!--$FileType-->[FileType]<!--/$FileType--> due to open handles

<!--issueDescription-->
The storage <!--$FileType-->[FileType]<!--/$FileType--> **<!--$FileName-->[FileName]<!--/$FileName-->** cannot be deleted because it contains <!--$FileHandleCount-->[FileHandleCount]<!--/$FileHandleCount--> open handles. Before you can delete an Azure Storage <!--$FileType-->[FileType]<!--/$FileType--> all handles need to be closed. Usually you can close these on the client side by closing all open instances of the file. However, if needed, we can force close these for you from the server side. If you need our assistance with this, please let us know.   

<!--/issueDescription-->
