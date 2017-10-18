<properties
    pageTitle="Memory error: You have reached the maximum allowable memory allocation for your tier."
    description="Memory error: You have reached the maximum allowable memory allocation for your tier."
    service="microsoft.analysisservices"
    resource="servers"
    authors="binf"
    resourceTags=""
	selfHelpType="resource"
	supportTopicIds=""
	productPesIds=""
	displayOrder="1"
	cloudEnvironments="public"
 />

# Memory error: You have reached the maximum allowable memory allocation for your tier.

## **Recommended steps**
Following methods are used to resolve the common memory problems, the symptoms include: OOM(out of memory) Error during processing/querying, Analysis Service connection Timeout etc.<br>
To resolve the issues, try one or more of the following methods.<br>

1. Check memory limit of your tier [Azure AS Pricing](https://azure.microsoft.com/en-us/pricing/details/analysis-services/). The default MemoryHighLimit is 80% of the SKU memory limit. If above that, AS will be in "panic mode" which means, it will stop accepting any new sessions being created or killing them if they did get created. The memory usage can be monitored through Azure portal: [Monitor Server Metrics](https://docs.microsoft.com/en-us/azure/analysis-services/analysis-services-monitor).<br>
2. Check your [MemoryHeapType](https://docs.microsoft.com/en-us/sql/analysis-services/server-properties/memory-properties) property. It is an advanced option to determine the heap implementation to use internally. The default value for the Developer/Standard SKU is 5(Hybrid) and for S8/S9 SKU is Intel TBB. In most cases, the hybrid heap provides better performance characteristics for small memory allocations. However in some cases, the hybrid heap allocation can result in memory spikes. In those cases, we recommend switch to 2(LFH) using SSMS or modifying msmdsrv.ini. [Configure properties in Analysis Service](https://docs.microsoft.com/en-us/sql/analysis-services/server-properties/server-properties-in-analysis-services).<br>
3. If you fail to connect to the server due to the high memory usage, connect using Dedicated Admin Connection to cancel long running sessions, drop some databases to reclaim memory. In SSMS(after 17.3), this property can be set in the connection dialog, add it in the "Additional Connection Parameters" tab, for example: DataSource=asazure://westus.asazure.windows.net/server1;DedicatedAdminConnection=true;.<br>
4. [Scale up to a higher SKU](https://azure.microsoft.com/en-us/blog/latest-release-of-azure-analysis-services-brings-scale-up-and-down/).<br>

## **Recommended documents**
[Azure AS Pricing](https://azure.microsoft.com/en-us/pricing/details/analysis-services/).<br>
[Server Properties in Analysis Services](https://docs.microsoft.com/en-us/sql/analysis-services/server-properties/server-properties-in-analysis-services).<br>
[Scale up to a higher SKU](https://azure.microsoft.com/en-us/blog/latest-release-of-azure-analysis-services-brings-scale-up-and-down/).<br>
