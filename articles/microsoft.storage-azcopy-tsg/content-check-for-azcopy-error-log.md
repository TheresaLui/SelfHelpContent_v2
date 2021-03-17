<properties
	pageTitle="Check for AzCopy error log"
	description="Check for AzCopy error log"
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
	articleId="19cc28d1-e76b-4696-a25d-3bd3f6ae066f"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to read AzCopy logs

1. AzCopy creates log and plan files for every job. You can use the logs to investigate and troubleshoot any potential problems.
2. **The relevant error is not necessarily the first error in the file.** For errors such as network errors, timeouts and Server Busy errors, AzCopy will retry up to 20 times and usually the retry process succeeds.? The first error you see may be something harmless that was successfully retried.?**So instead look for the one(s) that are near "UPLOADFAILED, COPYFAILED, or DOWNLOADFAILED?**
3. The logs will contain the status of failure, the full path, and the reason of the failure. Please do a log search on three statuses specified earlier in order to get to the failure.
4. The log will have a **"RequestID"** associated with each job. You can use that "RequestID" in **ASC XDiagnostics** to further troubleshoot customer's issue.
By default, the log and plan files are located in the **%USERPROFILE\\.azcopy** directory on Windows or **$HOME/.azcopy** directory on Mac and Linux.

*Important note: Advise customer to share the redacted version of their commands.*

**The product team maintains and regularly updates [Azcopy v10 Github](https://github.com/Azure/azure-storage-azcopy/issues). Be sure to check for open or known issues.**

