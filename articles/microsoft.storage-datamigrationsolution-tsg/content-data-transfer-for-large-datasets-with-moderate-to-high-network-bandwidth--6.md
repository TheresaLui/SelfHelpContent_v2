<properties
          pageTitle="Data transfer for large datasets with moderate to high network bandwidth"
          description="Data transfer for large datasets with moderate to high network bandwidth"
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
          articleId="3eb3fd1b-0cac-4b84-9173-aeef8f74001e"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Data transfer for large datasets with moderate to high network bandwidth

**Data transfer for large datasets with moderate to high network bandwidth**


1. The options recommended in this scenario depend on whether you have moderate network bandwidth or high network bandwidth.


2. Moderate network bandwidth (100 Mbps - 1 Gbps)

    1. **Azure Data Box family** for offline transfers: Use devices from Microsoft-supplied Data Box devices to move large amounts of data to Azure when you?re limited by time, network availability, or costs. Copy on-premises data using tools such as Robocopy. Depending on the data size intended for transfer, you can choose from Data Box Disk, Data Box, or Data Box Heavy.

    2. **Azure Import/Export**: Use Azure Import/Export service by shipping your own disk drives to securely import large amounts of data to Azure Blob storage and Azure Files. This service can also be used to transfer data from Azure Blob storage to disk drives and ship to your on-premises sites.

3. High network bandwidth (1 Gbps - 100 Gbps)

    1. **AzCopy**: Use this command-line tool to easily copy data to and from Azure Blobs, Files, and Table storage with optimal performance. AzCopy supports concurrency and parallelism, and the ability to resume copy operations when interrupted

    2. **Azure Storage REST APIs/SDKs**: When building an application, you can develop the application against Azure Storage REST APIs and use the Azure SDKs offered in multiple languages.

    3. **Azure Data Box family for online transfers**: Data Box Edge and Data Box Gateway are online network devices that can move data into and out of Azure. Use Data Box Edge physical device when there is a simultaneous need for continuous ingestion and pre-processing of the data prior to upload. Data Box Gateway is a virtual version of the device with the same data transfer capabilities. In each case, the data transfer is managed by the device.

    4. **Azure Data Factory**: Data Factory should be used to scale out a transfer operation, and if there is a need for orchestration and enterprise grade monitoring capabilities. Use Data Factory to regularly transfer files between several Azure services, on-premises, or a combination of the two. with Data Factory, you can create and schedule data-driven workflows (called pipelines) that ingest data from disparate data stores and automate data movement and data transformation.


4. The following table summarizes the differences in key capabilities such as data size and data size supported by each type:

    https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-moderate-high-network#comparison-of-key-capabilities



5. Now you have been given the recommended tool, if you need more information on how to use them:

    [Transfer data with Data Box disk](https://docs.microsoft.com/azure/databox/data-box-disk-quickstart-portal)

    [Transfer data with Data Box](https://docs.microsoft.com/azure/databox/data-box-quickstart-portal)

    [Transfer data with Import/Export](https://docs.microsoft.com/azure/storage/common/storage-import-export-data-to-blobs)

    [Transfer data with AzCopy Transfer data with AzCopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10)

    [Transfer data with Azure Data Box Gateway](https://docs.microsoft.com/azure/databox-online/data-box-gateway-deploy-add-shares)

    [Transform data with Data Box Edge before sending to Azure](https://docs.microsoft.com/azure/databox-online/data-box-edge-deploy-configure-compute)


<!---

questionAnswer
--

Question: 

**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1. Yes
2. No

-->



