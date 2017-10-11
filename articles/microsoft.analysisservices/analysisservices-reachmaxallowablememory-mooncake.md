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
	  cloudEnvironments="MoonCake"
 />

# Memory error: You have reached the maximum allowable memory allocation for your tier.

## **Recommended steps**
To resolve common issues, try one or more of the following methods.

1. Check memory limit of your tier [Azure AS Pricing](https://azure.microsoft.com/en-us/pricing/details/analysis-services/). The default MemoryHighLimit is 80% of physical memory or the virtual address space, whichever is less. AS will be in panic mode if the memory usage is above that.
2. Check your [MemoryHeapType](https://docs.microsoft.com/en-us/sql/analysis-services/server-properties/memory-properties) property. It is an advanced option to determine the heap implementation to use internally. The default value for the customer SKU was changed from 2(LFH) to 5(Hybrid) in the deployment(7/26/2017). In most cases, the hybrid heap provides better performance characteristics for small memory allocations. However in some cases, the hybrid heap allocation can result in memory spikes. In those cases, we recommend switch to 2(LFH) using SSMS or XMLA.
3. Connect using Dedicated Admin Connection to cancel long running sessions, drop some databases to reclaim memory. In SSMS, this property can be set in the Advanced setting tab of the connection dialog. This feature is available from SSMS 17.3 onwards.
4. Scale up to a higher SKU.

## **Recommended documents**
[Server Properties in Analysis Services](https://docs.microsoft.com/en-us/sql/analysis-services/server-properties/server-properties-in-analysis-services)
