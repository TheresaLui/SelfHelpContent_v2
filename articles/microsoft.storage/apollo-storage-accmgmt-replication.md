<properties
    pageTitle="Issue with changing replication type"
    description="Issue with changing replication type of storage account"
    infoBubbleText="See details on the right"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="Lea"
    ms.author="leakkari"
    displayOrder=""
    selfHelpType="Apollo"
    supportTopicIds="4a37cfaf-a791-70ef-915b-0b4f57df2616"
    resourceTags=""
    productPesIds="15629"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    articleId="eda7f487-251b-4c5c-b6ce-13c03876bfd9"
    ownershipId="StorageMediaEdge_AccountManagement"
    resourceRequired= "false"
/>

# Issue with changing storage account replication type

## Issues with changing storage account replication type


### Diagnostics 
Use the following diagnostics to identify why you're having issues changing the replication type for your storage account.

<insight> 
	<symptomId>StorageReplicationInsight</symptomId> 
	<executionText>We are running a quick check to find out if your storage resource is recoverable</executionText> 
	<timeoutText>We stopped the check, as it was taking too long</timeoutText> 
	<noResultText>Our troubleshooter did not detect any issues with your storage account. Make sure that the selected storage account in the previous blade is the one that you're having issues with concerning changing replication type.</noResultText>
    <maxInsightCount>2</maxInsightCount> 
	<additionalInputsReq>true</additionalInputsReq> 
</insight> 

### Guidelines for changing replication type
To change your storage account replication type:

1. Make sure that the redundancy option you select is supported by your storage account type.
   Refer to this table of [supported account types](https://docs.microsoft.com/azure/storage/common/storage-redundancy#supported-storage-account-types). </br>

2. Refer to this [table](https://docs.microsoft.com/azure/storage/common/redundancy-migration?tabs=portal#switch-between-types-of-replication) to understand how to switch from each type of replication. <br>
   You can change the replication type using any of the following three methods:</br>
    - Using [Azure portal, PowerShell or CLI](https://docs.microsoft.com/azure/storage/common/redundancy-migration?tabs=portal#change-the-replication-setting)
    - [Performing a manual migration](https://docs.microsoft.com/azure/storage/common/redundancy-migration?tabs=portal#perform-a-manual-migration-to-zrs-gzrs-or-ra-gzrs)
    - [Requesting a live migration](https://docs.microsoft.com/azure/storage/common/redundancy-migration?tabs=portal#request-a-live-migration-to-zrs-gzrs-or-ra-gzrs)
   
To learn more about these types of replications, [see this document](https://docs.microsoft.com/azure/storage/common/storage-redundancy#paired-regions).

### Resources
- [Can I change secondary location for my GRS/RA-GRS account?](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#paired-regions)
- [How to perform disaster recovery](https://docs.microsoft.com/azure/resiliency/resiliency-technical-guidance)
- [What to do if Azure Storage failover occurs](https://docs.microsoft.com/azure/storage/storage-disaster-recovery-guidance)
- [API for current status or storage account and its primary and secondary region](https://msdn.microsoft.com/library/azure/ee460802.aspx)
- [Converting to ZRS replication](https://docs.microsoft.com/azure/storage/common/storage-redundancy-zrs?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#converting-to-zrs-replication)
- [Understanding Azure Storage replication](https://azure.microsoft.com/documentation/articles/storage-redundancy)
