<properties
	pageTitle="Check if AzCopy transfered the data successfully"
	description="Check if AzCopy transfered the data successfully"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="4755419d-1fe8-4fea-908d-34f88edfbc54"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if AzCopy transfered the data successfully

AzCopy is a command-line utility that you can use to copy blobs or files to or from a storage account. This article helps you download AzCopy, connect to your storage account, and then transfer files. 

**Download**

[AzCopy v10](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10) 

**Run AzCopy**

1. For convenience, consider adding the directory location of the AzCopy executable to your system path for ease of use. That way you can type azcopy from any directory on your system. 
2. If you choose not to add the AzCopy directory to your path, you'll have to change directories to the location of your AzCopy executable and type azcopy or .\azcopy in Windows PowerShell command prompts. 
3. To see a list of commands, type azcopy -h and then press the ENTER key. To learn about a specific command, just include the name of the command (For example: azcopy list -h). 

**Copy blobs between storage accounts**

1. You can use AzCopy to copy blobs to other storage accounts. The copy operation is synchronous so when the command returns, that indicates that all files have been copied. 
2. Copy a blob to another storage account (try double quotes if single quotes fail): 

~~~powershell 

azcopy copy 'https://<source-storage-account-name>.blob.core.windows.net/<container-name>/<blob-path>?<SAS-token>' 'https://<destination-storage-account-name>.blob.core.windows.net/<container-name>/<blob-path>'   

~~~

3. Copy a directory to another storage account. (try double quotes if single quotes fail): 

~~~powershell 

azcopy copy 'https://<source-storage-account-name>.blob.core.windows.net/<container-name>/<directory-path>?<SAS-token>' 'https://<destination-storage-account-name>.blob.core.windows.net/<container-name>' --recursive 

~~~

4. Copy a container to another storage account. (try double quotes if single quotes fail): 


~~~powershell

azcopy copy 'https://<source-storage-account-name>.blob.core.windows.net/<container-name>?<SAS-token>' 'https://<destination-storage-account-name>.blob.core.windows.net/<container-name>' --recursive 

~~~

5. Copy all containers, directories, and blobs to another storage account. (try double quotes if single quotes fail): 

~~~powershell

azcopy copy 'https://<source-storage-account-name>.blob.core.windows.net/?<SAS-token>' 'https://<destination-storage-account-name>.blob.core.windows.net/' --recursive 

~~~