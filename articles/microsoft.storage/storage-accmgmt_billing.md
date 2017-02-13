<properties
	pageTitle="How does my Azure storage billing works"
	description="How does my Azure storage billing works"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32551653"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
/>

# How does my Azure storage billing works
#### **[Standard Storage Billing](http://blogs.msdn.com/b/windowsazurestorage/archive/2010/07/09/understanding-windows-azure-storage-billing-bandwidth-transactions-and-capacity.aspx)**
When using Windows Azure Blobs, Tables, Queues and Files storage costs can consist of:
1. **Bandwidth** – Since applications need to compute over their stored data, we allow hosted services to be co-located with their storage. This allows us to provide free bandwidth between computation and storage that are co-located, and only charge bandwidth for storage when accessed from outside the location it is stored in.
2. **Transactions** – Each individual Blob, Table and Queue REST request to the storage service is considered as a potential transaction for billing. Applications can then control their transaction costs by controlling how often and how many requests they send to the storage service. We analyze each request received and then classify it as billable or not billable based upon our ability to process the request and the request’s outcome.
3. **Capacity** – We accumulate the size of the objects stored (blobs, entities and messages) as well as their application and system metadata in order to measure the storage capacity for billing.

#### **[Premium Storage Billing](https://docs.microsoft.com/en-us/azure/storage/storage-premium-storage#pricing-and-billing)**
When using Premium Storage, the following billing considerations apply: 
1. **Premium storage disk / blob size**
2. **Premium storage snapshots**
3. **Outbound data transfers**


## **Recommended documents**
- [Azure Storage pricing](https://azure.microsoft.com/pricing/details/storage)
- [Understanding Azure Storage billing](http://blogs.msdn.com/b/windowsazurestorage/archive/2010/07/09/understanding-windows-azure-storage-billing-bandwidth-transactions-and-capacity.aspx)
- [Manage Azure resources through portal](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-portal)
- [Storage Analytics](https://azure.microsoft.com/en-in/documentation/articles/storage-analytics)
- [Storage Analytics Metrics](https://msdn.microsoft.com/library/azure/hh343258.aspx)
- [Storage Analytics Logging](https://msdn.microsoft.com/en-us/library/azure/hh343262.aspx)
- [Enabling Storage Metrics and Viewing Metrics Data](https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/Enabling-Storage-Metrics-and-Viewing-Metrics-Data)
