<properties
          pageTitle="Choose an Azure solution for data transfer"
          description="Choose an Azure solution for data transfer"
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
          articleId="46f0e5a0-9121-47d5-bb85-11dc3a34cc65"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />


# Choose an Azure solution for data transfer

**How to choose an Azure solution for data transfer**

1. This TSG provides an overview of some of the common Azure data transfer solutions.


2. The best transfer solution is based on a combination of:

    1. Data size: Size of data

    2. Transfer frequency: one time or periodic

    3. Network: bandwidth available


3. The following illustrates the guidelines to choose the various Azure data transfer tools depending upon the network bandwidth available for transfer, data size intended for transfer, and frequency of the transfer.



    | Recommended Tool             | Data Size       | Bandwidth          |
    |------------------------------|-----------------|--------------------|
    | AzCopy                       | 1 MB to 50 TB   | 1 Mbps to 1 Gbps   |
    | Storage Explorer             | 1 MB to 50 TB   | 1 Mbps to 1 Gbps   |
    | Azure portal                 | 1 MB to 50 TB   | 1 Mbps to 1 Gbps   |
    | Data Box Disk*               | 100 GB to 70 TB | 1 Mbps to 100 Mbps |
    | Data Box*                    | 50 TB to 500 TB | 1 Mbps to 1 Gbps   |
    | Data Box Heavy*              | 400 TB to 5 PB  | 1 Mbps to 10 Gbps  |
    | Data Box Gateway             | 50 GB to 5 PB   | 1 Gbps to 100 Gbps |
    | Data Box Edge                | 50 GB to 5 PB   | 1 Gbps to 100 Gbps |
    | Data Factory                 | 50 GB to 5 PB   | 1 Gbps to 100 Gbps |
    | AzCopy programmatic transfer | 50 GB to 5 PB   | 1 Gbps to 100 Gbps |
    | Azure Storage REST APIs      | 50 GB to 5 PB   | 1 Gbps to 100 Gbps |



    **The upper limits of the offline transfer devices -Data Box Disk, Data Box, and Data Box Heavy can be extended by placing multiple orders of a device type.*



<!---


questionAnswer
--

Question: 

**Whats the current scenario regarding data size and bandwidth?**

Answers:

1: Is your available network bandwidth limited or non-existent, and you want to transfer large datasets?

2: Do you want to transfer large datasets over network and you have a moderate to high network bandwidth?

3: Do you want to occasionally transfer just a few files over the network?

4: Are you looking for point-in-time data transfer at regular intervals?

5: Are you looking for on-going, continuous data transfer?


-->