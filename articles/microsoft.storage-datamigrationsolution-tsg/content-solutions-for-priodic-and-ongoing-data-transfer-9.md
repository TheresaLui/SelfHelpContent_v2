<properties
          pageTitle="Solutions for Periodic and Ongoing data transfer"
          description="Solutions for Periodic and Ongoing data transfer"
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
          articleId="36564d7b-94fc-47f8-9ea2-e24cbfe2922d"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Solutions for Periodic and Ongoing data transfer

**Solutions for periodic data transfer**


1. The recommended options for periodic data transfer fall into two categories depending on whether the transfer is recurring or continuous.

2. For data transfer that occurs at regular intervals, use the scripted and programmatic tools such as AzCopy and Azure Storage REST APIs. These tools are targeted towards IT professionals and developers. For continuous, ongoing data ingestion, you can select one of Data Box online transfer device or Azure Data Factory. These tools are set up by IT professionals and can transparently automate data transfer.


3. Scripting tools

    1. **AzCopy:** Use this command-line tool to easily copy data to and from Azure Blobs, Files, and Table storage with optimal performance. AzCopy supports concurrency and parallelism, and the ability to resume copy operations when interrupted.

    2. **PowerShell:** For users comfortable with system administration, use the Azure Storage module in Azure PowerShell to transfer data.

    3. **CLI:** Use this cross-platform tool to manage Azure services and upload data to Azure Storage.

    4. **Rest APIs/SDKs:** When building an application, you can develop the application against Azure Storage REST APIs/SDKs and use the Azure client libraries offered in multiple languages.

4. Continuous data ingestion tools

    1. **Azure Data Factory**: Data Factory should be used to scale out a transfer operation, and if there is a need for orchestration and enterprise grade monitoring capabilities. Use Azure Data Factory to set up a cloud pipeline that regularly transfers files between several Azure services, on-premises, or a combination of the two. Azure Data Factory lets you orchestrate data-driven workflows that ingest data from disparate data stores and automate data movement and data transformation.

    2. **Azure Data Box family for online transfers**: Data Box Edge and Data Box Gateway are online network devices that can move data into and out of Azure. Data Box Edge uses artificial intelligence (AI)-enabled Edge compute to pre-process data before upload. Data Box Gateway is a virtual version of the device with the same data transfer capabilities.


**Solutions for Ongoing data transfer**

Ongoing End to End data migration solution to azure files. Data transfer from external sources to file share using Azure File Sync.

1. **Azure File Sync**

    Data transfer from external sources to file share using Azure File Sync

    Today, the maximum size for an Azure file share is 100 TiB. 

    Because of this current limitation, you must consider the expected data growth when deploying an Azure file share.

    It is possible to sync multiple Azure file shares to a single Windows File Server with Azure File Sync. 

    This allows you to ensure that older, large file shares that you may have on-premises can be brought into Azure File Sync.

    **Recommended options**

    As part of a first sync between an Azure file share (a Cloud Endpoint) and a Windows directory namespace (a Server Endpoint), Azure File Sync will replicate all data from the existing file share to Azure Files.

    If you need more information on how to use them, see Planning for [Azure File Sync Deployment](https://docs.microsoft.com/azure/storage/files/storage-files-planning)


2. The following table summarizes the differences in key capabilities
    
    https://docs.microsoft.com/azure/storage/common/storage-solution-small-dataset-low-moderate-network#comparison-of-key-capabilities


3. Now you have been given the recommended tool, if you need more information on how to use them:


    [**Transfer data with AzCopy Transfer data with AzCopy**](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10)

    [**Transfer data with Azure Data Box Gateway**](https://docs.microsoft.com/azure/databox-online/data-box-gateway-deploy-add-shares)

    [**Transform data with Data Box Edge before sending to Azure**](https://docs.microsoft.com/azure/databox-online/data-box-edge-deploy-configure-compute)

    [**Transfer data with Azure Data Factory**](https://docs.microsoft.com/azure/data-factory/tutorial-bulk-copy-portal)

    [**Azure File Sync Deployment**](https://docs.microsoft.com/azure/storage/files/storage-files-planning)


<!---

questionAnswer
--

Question: 

**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1. Yes
2. No

-->




