<properties
	pageTitle="Optimize AzCopy Throughput"
	description="Optimize AzCopy Throughput"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9533a020-3fc1-4325-a7a7-3eb2d099c755"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Optimize AzCopy Throughput

1. You can use the **cap-mbps** flag to place a ceiling on the throughput data rate. 
2. For example, the following command caps throughput to 10 megabits (MB) per second.

~~~shell

azcopy cap-mbps 10

~~~

3. Throughput can decrease when transferring small files. 
4. You can you can increase throughput by setting the **AZCOPY_CONCURRENCY_VALUE** environment variable. 
5. This variable specifies the number of concurrent requests that can occur. 
6. If your computer has fewer than 5 CPUs, then the value of this variable is set to **32**. 
7. Otherwise, the default value is equal to 16 multiplied by the number of CPUs. 
8. The maximum default value of this variable is **300**, but you can manually set this value higher or lower.

| Operating System   |   Command |
| ----------- |  ----------- |
| Windows     | set AZCOPY_CONCURRENCY_VALUE=<value>       |
| Linux   | export AZCOPY_CONCURRENCY_VALUE=<value>     |
| MacOS |  	export AZCOPY_CONCURRENCY_VALUE=<value>          |


9. Use the ** azcopy env**  to check the current value of this variable. If the value is blank, then the ** AZCOPY_CONCURRENCY_VALUE**  variable is set to the default value of ** 300** .

## Recommended Documents

1. [AzCopy Configure](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-configure?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#optimize-throughput) for more info. 
