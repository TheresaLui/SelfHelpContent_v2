<properties
          pageTitle="AzCopy"
          description="AzCopy"
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
          articleId="25b324ee-828c-4f4e-9cc2-dc7a2a2851ee"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# AzCopy

**Move data with AzCopy**

AzCopy is a command-line utility that you can use to copy blobs or files to or from a storage account. Before you begin, see the [Get started with AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10?toc=%2fazure%2fstorage%2ffiles%2ftoc.json) article to [Download AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10#download-azcopy) and familiarize yourself with the tool. 

AzCopy is optimized for performance. One way that it's faster, is that data is copied directly between storage servers, so AzCopy doesn't use the network bandwidth of your computer (if applicable). Use AzCopy at the command line or as part of a custom script. 

*Note: To learn about a specific command, just include the name of the command (For example: azcopy list -h)*

Run AzCopy to copy Blob and File data:



<!---

questionAnswer
--

Question: 


**What kind of data are you moving?**

Answers:

1: Blobs

2: Files

-->
