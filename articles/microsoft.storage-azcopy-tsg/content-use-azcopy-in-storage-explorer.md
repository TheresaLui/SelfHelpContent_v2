<properties
	pageTitle="Use AzCopy in Storage Explorer"
	description="Use AzCopy in Storage Explorer"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0dd927c8-0b52-4adc-86c2-c2cec373e143"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Use AzCopy in Storage Explorer

1. If an error is returned from AzCopy then it will show in the activity window of ASE.  The activity window will also show the progress of the upload or download as well as link to copy the AzCopy command line used to the clipboard.  This can be used for isolation troubleshooting to know if the issue is with ASE or AzCopy.
2. The log files written by AzCopy will be written to the folder `C:\Users\<username>\.azcopy\ (Windows)`.
3. You can isolate the issue by running the same AzCopy command that ASE is running.  ASE may not have the latest released version of AzCopy so you can try the latest release.  If this resolves the issue then you can download AzCopy.exe and update it in the location where it is loaded by ASE:
4. `C:\Program Files (x86)\Microsoft Azure Storage Explorer\resources\app\node_modules\se-az-copy-exe-win\dist\bin (Windows)`
5. Replacing the AzCopy.exe here should just work.  You need to restart ASE.  In some cases there might be some incompatibilities so be sure to back up the existing AzCopy.exe in this directory before copying in the newer version.
