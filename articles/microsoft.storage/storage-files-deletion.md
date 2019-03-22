<properties
	pageTitle="Unable to delete file in an Azure file share"
	description=" Unable to delete file in an Azure file share"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="jeffpatt24"
	ms.author="jeffpatt"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds=" 32602743"
	resourceTags=""
	productPesIds="16460"
	cloudEnvironments="public,MoonCake"
	articleId="Unable to delete file in an Azure file share"
/>

# Unable to delete file in an Azure file share

This issue typically occurs if the file still has an open handle. If the clients have closed all open handles on the file and the issue continues to occur, please open a support case and we will force close the handles.
