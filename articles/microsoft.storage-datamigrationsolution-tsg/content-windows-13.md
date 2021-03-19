<properties
          pageTitle="Windows"
          description="Windows"
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
          articleId="559bad0c-da32-418e-9019-ff6c904d1dde"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />


# Windows

**Data Migration Tools available on Windows OS**

1. **AzCopy v10**: AzCopy is a command-line utility designed for copying data to/from Microsoft Azure Blob, File, and Table storage, using simple commands designed for optimal performance. 

<!---
You can copy data between a file system and a storage account, or between storage accounts. 

You can upload, download, copy files concurrently & the biggest advantage you get is, it can resume interrupted operations. It doesn't offer any GUI to play with. 

That means there is a slight learning curve for all those GUI people. 

-->

2. **Azure Storage Explorer**: Microsoft Azure Storage Explorer is a standalone app that makes it easy to work with Azure Storage data on Windows, macOS, and Linux. 

<!---
If azcopy is enabled in storage explorer, it will use the azcopy command line to copy. 

This tool is usefull, when you want to manually copy files/folders across storage accounts.
-->

3. **Azure PowerShell**: For Azure Storage, powershell cmdlets are used to manage the data stored in the storage account. For example, uploading blobs, creating file shares, and adding messages to a queue. 

<!---
This is normally used when we want to move data with scripting programming artifacts.
-->

4. **Azure CLI**: Azure CLI is an open source, cross platform set of tools for different azure services. This is an alternative to the powershell and is available on all platforms, while PS is generally more available on Windows.

5. **Robocopy**: Robocopy is a well known copy tool that ships with Windows and Windows Server.

6. **Other tools**: 
    
    ***Azure Import/Export service***: Azure Import/Export service is used to securely import large amounts of data to Azure Blob storage and Azure Files by shipping disk drives to an Azure datacenter

    ***AzCopy v8.1***: Copy blobs in Blob storage (*Obsolete/Not Recommended*).
    This version is for backward compatibility and not supported by Microsoft. 
    
    ***AzCopy v7.3***: Supports Table copy



<!---

questionAnswer
--

Question: 

**Select which Tool for Windows Operating system is the customer using?**

Answers:

1: Azcopy (Blob/File)

2: Azure Storage Explorer (Blob/File)

3: Azure PowerShell (Blob/File)

4: Azure CLI (Blob/File)

5: Robocopy (File only)

6: Other Tools (Blob/File)

-->