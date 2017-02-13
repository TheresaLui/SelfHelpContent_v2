<properties
	pageTitle="Which account replication type do I need"
	description="Which account replication type do I need"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32551648"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
/>

# Which account replication type do I need

## **Recommended steps**
The data in your Microsoft Azure storage account is always replicated to ensure durability and high availability. Replication copies your data, either within the same data center, or to a second data center, depending on which replication option you choose. Replication protects your data and preserves your application up-time in the event of transient hardware failures. If your data is replicated to a second data center, that also protects your data against a catastrophic failure in the primary location.1 

Replication ensures that your storage account meets the [Service-Level Agreement (SLA) for Storage](https://azure.microsoft.com/support/legal/sla/storage/) even in the face of failures. See the SLA for information about Azure Storage guarantees for durability and availability. 

When you create a storage account, you can select one of the following replication options: 
- [LRS - Locally Redundant Storage](https://docs.microsoft.com/azure/storage/storage-redundancy#locally-redundant-storage)<br>    
- [ZRS - Zone Redundant Storage](https://docs.microsoft.com/azure/storage/storage-redundancy#zone-redundant-storage)<br>
- [GRS - Geo Redundant Storage](https://docs.microsoft.com/azure/storage/storage-redundancy#geo-redundant-storage)<br>     
- [RA-GRS - Read-Access Geo Redundant Storage](https://docs.microsoft.com/azure/storage/storage-redundancy#read-access-geo-redundant-storage)
 
Read-access geo-redundant storage (RA-GRS) is the default option when you create a new storage account. 

The following table provides a quick overview of the differences between LRS, ZRS, GRS, and RA-GRS, while subsequent sections address each type of replication in more detail. 
| **Replication strategy**        														| **LRS**		| **ZRS**	| **GRS**	| **RA-GRS**	|
| ------------------------------------------------------------------------------------- |:-------------:| :--------:| :--------:| :------------:|
| Data is replicated across multiple datacenters.										| No			| Yes		| Yes		| Yes			| 
| Data can be read from the secondary location as well as from the primary location.	| No			| No		| No		| Yes			|
| Number of copies of data maintained on separate nodes. 								| 3				| 3			| 6			| 6				|

## **Recommended documents**
- [Understanding Azure Storage replication](https://azure.microsoft.com/documentation/articles/storage-redundancy)
- [Azure resiliency technical guidance](https://docs.microsoft.com/azure/resiliency/resiliency-technical-guidance)

