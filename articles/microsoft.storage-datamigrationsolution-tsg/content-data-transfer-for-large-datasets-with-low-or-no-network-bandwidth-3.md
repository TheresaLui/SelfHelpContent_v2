<properties
          pageTitle="Data transfer for large datasets with low or no network bandwidth"
          description="Data transfer for large datasets with low or no network bandwidth"
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
          articleId="25818a95-9999-46ec-8a42-55464314c38c"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Data transfer for large datasets with low or no network bandwidth

**Data transfer for large datasets with low or no network bandwidth**


1. The options available in this scenario are devices for Azure Data Box offline transfer or Azure Import/Export

    1. **Azure Data Box family for offline transfers**: Use devices from Microsoft-supplied Data Box devices to move large amounts of data to Azure when you?re limited by time, network availability, or costs. Copy on-premises data using tools such as Robocopy. Depending on the data size intended for transfer, you can choose from Data Box Disk, Data Box, or Data Box Heavy.

    2. **Azure Import/Export**: Use Azure Import/Export service by shipping your own disk drives to securely import large amounts of data to Azure Blob storage and Azure Files. This service can also be used to transfer data from Azure Blob storage to disk drives and ship to your on-premises sites.


2. There is a table that shows the projected time depending on network bandwidth and data size

    https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network#offline-transfer-or-network-transfer


3. The following table summarizes the differences in key capabilities such as data size and data size supported by each type

    https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network#comparison-of-key-capabilities


4. Now you have been given the recommended tool, if you need more information on how to use them:

    [Transfer data with Data Box disk](https://docs.microsoft.com/azure/databox/data-box-disk-quickstart-portal)

    [Transfer data with Data Box](https://docs.microsoft.com/azure/databox/data-box-quickstart-portal)

    [Transfer data with Import/Export](https://docs.microsoft.com/azure/storage/common/storage-import-export-data-to-blobs)


<!---

questionAnswer
--

Question: 

**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1. Yes
2. No

-->


