<properties
	pageTitle="Azure Data Lake Gen 2 storage performance"
	description="Azure Data Lake Gen 2 storage performance high latency troubleshooting"
	infoBubbleText=""
	service="microsoft.storage"
	resource="datalakestoragegen2"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	articleId="dd9d20bd-a659-403d-95e7-d9e79475ebf3"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32612602"
	resourceTags=""
	productPesIds="16598"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_DataLakeStorageGen2"
/>

# Azure Data Lake Gen2 Storage Performance High Latency Troubleshooting

## **Recommended Steps**

### Common Storage Performance Diagnostics and Troubleshooting

* [Troubleshooting latency increase when using Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#troubleshooting-guidance/)<br>

### ADLSGen2 Premium Tier

* [For significantly lower storage latencies use ADLSGen2 Premium Tier](https://azure.microsoft.com/updates/premium-tier-for-azure-data-lake-storage-now-in-public-preview/)<br>


### Troubleshoot client side performance issues when facing high end-to-end latency

* [Troubleshoot client performance issues when Average end-to-end latency is much higher than Average Server side latency](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting?toc=/azure/storage/blobs/toc.json#investigating-client-performance-issues)<br>
* [Troubleshoot high client latency issues when metrics show low Average end-to-end latency and low Average server side latency](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting?toc=/azure/storage/blobs/toc.json#metrics-show-low-AverageE2ELatency-and-low-AverageServerLatency)

### Increase AzCopy Performance for Data Transfer

* [Optimizing Throughput/Performance - Increase concurrent requests](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-configure?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#optimize-throughput)

## **Recommended Documents**

### How to Monitor performance for Storage Services

* [Monitor Storage performance using Azure Monitor](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#monitoring-performance) to identify increase in latency when compared to your baseline

