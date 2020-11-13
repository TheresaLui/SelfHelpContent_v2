<properties
          pageTitle="Azure PowerShell"
          description="Azure PowerShell"
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
          articleId="6352b97c-4640-4095-9199-11bd9d6686b8"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Azure PowerShell

**Move data with Azure PowerShell**


1. [**Install Azure PowerShell module**](https://docs.microsoft.com/powershell/azure/install-Az-ps?view=azps-4.5.0)
2. **Azcopy or Powershell**: [Upload a VHD to Azure or copy a managed disk to another region - Azure PowerShell](
    https://docs.microsoft.com/azure/virtual-machines/windows/disks-upload-vhd-to-managed-disk-powershell)

3. **Upload data with PowerShell**: You can use windows Azure PowerShell to upload/download huge files from azure
	
    [**Set-AzureStorageBlobContent**](http://msdn.microsoft.com/library/dn408487.aspx) is for uploading

    Set-AzureStorageBlobContent -container containerName -file .\filename -blob blobname
    

    **Upload a file by name**

        This example uploads a file by name
        C:\PS>Set-AzureStorageBlobContent -Container upload -File .\filename -Blob blobname

    **Upload a file using ls command**

        This example lists all files in a directory and its subdirectories, and then uploads the files
        C:\PS>ls -File -Recurse | Set-AzureStorageBlobContent -Container upload

    **Upload a file to a blob using the pipeline**

        This example gets a specific container and blob, and then uses the pipeline to upload a file to the specified blob
        C:\PS>Get-AzureStorageBlob -Container containername -Blob blobname | Set-AzureStorageBlobContent -File filename

    **Upload file to a container using pipeline**

        This example gets all containers whose name starts with ?container?, and then uses the pipeline to upload a file to all the containers
        C:\PS>Get-AzureStorageContainer -Container container* | Set-AzureStorageBlobContent -File filename -Blob blobname

    **Upload file and set metadata**

        This example uploads a file and sets metadata for the blob
        C:\PS>$meta = @{"key" = "value"; "name" = "test"}Set-AzureStorageBlobContent -File filename -Container containername -Metadata $meta

4. **Download data with PowerShell**

    [**Get-AzureStorageBlobContent**](http://msdn.microsoft.com/library/dn408562.aspx) is for downloading

    Get-AzureStorageBlobContent -container containername -blob blob -destination C:\test\
    

    **Download blob content by name**

        This example downloads a blob by name
        C:\PS>Get-AzureStorageBlobContent -Container containername -Blob blob -Destination C:\test\

    **Download blob content using the pipeline**
        
        This example uses the pipeline to find and download blob content
        C:\PS>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent

    **Download blob content using the pipeline and a wildcard character**

        This example uses the asterisk wildcard character and the pipeline to find and download blob content
        C:\PS>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob cbox.exe -Destination C:\test

<!---

questionAnswer
--

Question: 


**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1: Yes

2: No

-->