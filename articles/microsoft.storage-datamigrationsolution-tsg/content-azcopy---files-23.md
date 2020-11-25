<properties
          pageTitle="AzCopy (Files)"
          description="AzCopy (Files)"
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
          articleId="35b3e74e-e051-489a-b4c4-1bd1e27c9ca6"
           ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# AzCopy (Files)

**Move data with AzCopy**

You can use AzCopy to Migrate on-premises data to cloud storage accounts

[Download AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10#download-azcopy)

1. **Upload** data to Azure Files

	You can use AzCopy to copy data to an azure files

	Upload a **File**
	```dos
	azcopy copy '<local-file-path>' 'https://<storage-account-name>.file.core.windows.net/<file-share-name>/<file-name><SAS-token>'
	```

	Upload a **Directory**

	This example copies a directory (and all of the files in that directory) to a file share. The result is a directory in the file share by the same name.
	```dos
	azcopy copy '<local-directory-path>' 'https://<storage-account-name>.file.core.windows.net/<file-share-name><SAS-token>' --recursive
	```
	Upload **Content of a Directory**
	You can upload the contents of a directory without copying the containing directory itself by using the wildcard symbol (*).
	```dos
	azcopy copy '<local-directory-path>/*' 'https://<storage-account-name>.file.core.windows.net/<file-share-name>/<directory-path><SAS-token>
	```

2. **Download** data to Azure Files

	Download a **File**

	```dos
	azcopy copy 'https://<storage-account-name>.file.core.windows.net/<file-share-name>/<file-path><SAS-token>' '<local-file-path>'
	```

	Download a **Directory**

	This example results in a directory represented by **directory-path** that contains all of the downloaded files.

	```dos
	azcopy copy 'https://<storage-account-name>.file.core.windows.net/<file-share-name>/<directory-path><SAS-token>' '<local-directory-path>' --recursive
	```

	Download **Content of a Directory**

	You can download the contents of a directory without copying the containing directory itself by using the wildcard symbol (*).

	```dos
	Syntax	azcopy copy 'https://<storage-account-name>.file.core.windows.net/<file-share-name>/*<SAS-token>' '<local-directory-path>/'
	```

3. **Copy Files** between storage accounts

	
	```dos
	azcopy copy 'https://<source-storage-account-name>.file.core.windows.net/<file-share-name>/<file-path><SAS-token>' 'https://<destination-storage-account-name>.file.core.windows.net/<file-share-name>/<file-path><SAS-token>'
	```

	**Copy a Directory** to another Storage Account
	
	```dos
	azcopy copy 'https://<source-storage-account-name>.file.core.windows.net/<file-share-name>/<directory-path><SAS-token>' 'https://<destination-storage-account-name>.file.core.windows.net/<file-share-name><SAS-token>' --recursive
	```

	**Copy a FileShare** to another Storage Account

	```dos
	azcopy copy 'https://<source-storage-account-name>.file.core.windows.net/<file-share-name><SAS-token>' 'https://<destination-storage-account-name>.file.core.windows.net/<file-share-name><SAS-token>' --recursive
	```
	
	**Copy all file shares, directories, and files** to another storage account

	```dos
	azcopy copy 'https://<source-storage-account-name>.file.core.windows.net/<SAS-token>' 'https://<destination-storage-account-name>.file.core.windows.net/<SAS-token>' --recursive'
	```

**Troubleshoot AzCopy**

If AzCopy did not transfered the data successfully, troubleshoot AzCopy via [Configure, optimize, and troubleshoot AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-configure)

<!--

questionAnswer
--

Question: 


**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1: Yes

2: No

-->