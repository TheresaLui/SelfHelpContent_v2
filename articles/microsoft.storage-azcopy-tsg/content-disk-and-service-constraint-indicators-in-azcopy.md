<properties
	pageTitle="Disk and Service Constraint Indicators in AzCopy"
	description="Disk and Service Constraint Indicators in AzCopy"
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
	articleId="fcfe4f43-53d7-4e26-aa69-d5582932fb6c"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Disk and Service Constraint Indicators in AzCopy

AzCopy logs the following messages in the log file to indicate whether **Customer's disk** or **Storage Service** is the limiting factor for AzCopy transfer.

Note: Messages below never display in the first 30 seconds of a job. Only displays after first 30 seconds, since we want things to stabilize before we consider displaying these messages.

**Disk May be limiting the speed**

This message will be displayed if the data is moving faster over the network than it can be written or read to/from disk. And also, if disk scanning is so slow that we cant feed new files quickly enough to the rest of AzCopy.
This is explained in detail [**here**](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=disk-and-service-constraint-indicators-in-azcopy).

**Service may be limiting speed.**
This message is displayed if AzCopy is receiving "Server Busy" responses from Azure. (I.e. HTTP status 503). Seeing a few Server Busy messages is fine. AzCopy will automatically retry the affected operations, with an exponential delay.
This is explained in detail [**here**](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=disk-and-service-constraint-indicators-in-azcopy).

**PageBlobService may be limiting speed.**

If the job includes at least one page blob and the Storage Service is limiting the transfer rate for that page blob. Page blobs can have per-blob throughput limits, and in many cases those limits are stricter than the overall throughput limit on the storage account. If those limits are affecting the transfer of any file in the job, this message will be displayed.
This is explained in detail [**here**](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=disk-and-service-constraint-indicators-in-azcopy).

If you want to extract all the relevant log files to a separate file, you can use a command like this PowerShell one (substituting in the correct name for your log file):

~~~shell
**-string "Page blob" .\858ebb30-4796-914f-632e-dc355cda0e1c.log | Out-File pageBlobLines.txt**

~~~
