<properties
          pageTitle="AzCopy (Blobs)"
          description="AzCopy (Blobs)"
          service="Microsoft.Storage"
          resource="Microsoft.Storage/storageAccounts"
          authors="akshaymatmicrosoft"
          ms.author="akshaym"
          displayOrder=""
          selfHelpType="TSG_Content"
          supportTopicIds=""
          resourceTags=""
          productPesIds=""
          cloudEnvironments="public, fairfax, usnat, ussec"
          articleId="6f119812-4504-44b3-bc17-ee352d2e0975"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# AzCopy (Blobs)

**Move data with AzCopy**

You can use AzCopy to Migrate on-premises data to cloud storage accounts

[Download AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10#download-azcopy)

1. **Copy blobs** between storage accounts

	Copy operation is synchronous so when the command returns, that indicates that all files have been copied. 
	
	*Note: **Try double quotes if single quotes fail***

	Copy a **blob** to another storage account:
	
	```dos
	azcopy copy 'https://<source-storage-account-name>.blob.core.windows.net/<container-name>/<blob-path>?<SAS-token>' 'https://<destination-storage-account-name>.blob.core.windows.net/<container-name>/<blob-path>'  
	```

	Copy a **directory** to another storage account:

	```dos
	azcopy copy 'https://<source-storage-account-name>.blob.core.windows.net/<container-name>/<directory-path>?<SAS-token>' 'https://<destination-storage-account-name>.blob.core.windows.net/<container-name>' --recursive 
	```

	Copy a **container** to another storage account:

	```dos
	azcopy copy 'https://<source-storage-account-name>.blob.core.windows.net/<container-name>?<SAS-token>' 'https://<destination-storage-account-name>.blob.core.windows.net/<container-name>' --recursive 
	```

	Copy **all containers, directories, and blobs** to another storage account:

	```dos
	azcopy copy 'https://<source-storage-account-name>.blob.core.windows.net/?<SAS-token>' 'https://<destination-storage-account-name>.blob.core.windows.net/' --recursive 
	```

2. **Upload blobs** to storage accounts

	You can use AzCopy to upload blobs to storage accounts. 

    Upload a **File**
    
    ```dos
	azcopy copy '<local-file-path>' 'https://<storage-account-name>.<blob or dfs>.core.windows.net/<container-name>/<blob-name>'
	```
    Upload a **Directory**

	```dos
	azcopy copy '<local-directory-path>' 'https://<storage-account-name>.<blob or dfs>.core.windows.net/<container-name>' --recursive
	```
    Upload a **Directory within container**
	
	```dos
	azcopy copy 'C:\myDirectory' 'https://mystorageaccount.blob.core.windows.net/mycontainer/myBlobDirectory' --recursive
	```


3. **Download blobs** to storage accounts

	You can use AzCopy to download blobs to other storage accounts. 

	Download a **File**

	```dos
	azcopy copy 'https://<storage-account-name>.<blob or dfs>.core.windows.net/<container-name>/<blob-path>' '<local-file-path>'
	```
	
	Download **contents of a directory**
	You can download the contents of a directory without copying the containing directory itself by using the wildcard symbol (*)

	```dos
	azcopy copy 'https://<storage-account-name>.blob.core.windows.net/<container-name>/*' '<local-directory-path>/'
	```


**Troubleshoot AzCopy**

If AzCopy did not transfered the data successfully, troubleshoot AzCopy via [Configure, optimize, and troubleshoot AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-configure)

<!---

questionAnswer
--

Question: 

**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1: Yes

2: No

-->
