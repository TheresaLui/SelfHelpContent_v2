<properties
          pageTitle="Data transfer for small datasets with low to moderate network bandwidth"
          description="Data transfer for small datasets with low to moderate network bandwidth"
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
          articleId="a8cf853c-9a47-4aab-9c1e-81f01f775de0"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Data transfer for small datasets with low to moderate network bandwidth

**Data transfer for small datasets with low to moderate network bandwidth**


1. Small datasets refer to data sizes in the order of GBs to a few TBs. Low to moderate network bandwidth implies 45 Mbps (T3 connection in datacenter) to 1 Gbps.


2. If you are transferring only a handful of files and you don?t need to automate data transfer, consider the tools with a graphical interface. If you are comfortable with system administration, consider command line or programmatic/scripting tools.


3. Graphical interface tools

    1. **Azure Storage Explorer**: This cross-platform tool lets you manage the contents of your Azure storage accounts. It allows you to upload, download, and manage blobs, files, queues, tables, and Azure Cosmos DB entities. Use it with Blob storage to manage blobs and folders, as well as upload and download blobs between your local file system and Blob storage, or between storage accounts.

    2. **Azure portal**: Azure Storage in Azure portal provides a web-based interface to explore files and upload new files one at a time. This is a good option if you do not want to install any tools or issue commands to quickly explore your files, or to simply upload a handful of new ones.


4. Scripting tools

    1. **AzCopy**: Use this command-line tool to easily copy data to and from Azure Blobs, Files, and Table storage with optimal performance. AzCopy supports concurrency and parallelism, and the ability to resume copy operations when interrupted.

    2. **PowerShell**: For users comfortable with system administration, use the Azure Storage module in Azure PowerShell to transfer data.

    3. **CLI**: Use this cross-platform tool to manage Azure services and upload data to Azure Storage.

    4. **Rest APIs/SDKs**: When building an application, you can develop the application against Azure Storage REST APIs/SDKs and use the Azure client libraries offered in multiple languages.


5. The following table summarizes the differences in key capabilities
    
    https://docs.microsoft.com/azure/storage/common/storage-solution-small-dataset-low-moderate-network#comparison-of-key-capabilities

    The following table shows the projected time depending on network bandwidth and data size

    https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network#offline-transfer-or-network-transfer

    The following table summarizes the differences in key capabilities such as data size and data size supported by each type

    https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network#comparison-of-key-capabilities


<!---

questionAnswer
--

Question: 

**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1. Yes
2. No

-->


