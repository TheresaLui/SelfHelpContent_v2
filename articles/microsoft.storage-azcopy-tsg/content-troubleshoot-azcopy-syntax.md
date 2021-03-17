<properties
	pageTitle="Troubleshoot AzCopy Syntax"
	description="Troubleshoot AzCopy Syntax"
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
	articleId="079e96cf-51b1-4d5f-896d-5598892dbf3c"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Troubleshoot AzCopy Syntax

1. Verify data transfer method is supported 
2. Confirm authorization utilized 
3. SAS token is appended correctly to both source and destination
4. The name of the file/folder should match in source & destination path
5. If using AAD auth, ensure source URL includes SAS token. 
6. Cross reference [**transfer files**](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10#transfer-files) documentation to ensure correct syntax is utilized 
7. [Reference parameters and syntax for different scenarios. ](https://docs.microsoft.com/en-us/azure/storage/common/storage-ref-azcopy?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json)

## URL Encode Special Characters

If you have a file with a special character in the name e.g. `test#ing.txt`. The transfer will fail due to **improper URL encoding**. Fix is to URL escape the reserved characters after percent-encoding. Therefore, pound sign in test#ing.txt should be represented by `%23`. More details [Here.](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=url-encode-special-characters)
