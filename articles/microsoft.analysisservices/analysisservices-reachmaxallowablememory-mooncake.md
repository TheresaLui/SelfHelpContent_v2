<properties
    pageTitle="Memory error: You have reached the maximum allowable memory allocation for your tier."
    description="Memory error: You have reached the maximum allowable memory allocation for your tier."
    service="microsoft.analysisservices"
    resource="servers"
    authors="brspie"
    ms.author="binf"
    resourceTags=""
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    displayOrder="1"
    cloudEnvironments="MoonCake"
    articleId="15dc089b-0c5c-4e33-b3ad-a40b00a011b1"
    ownershipId="AzureData_AnalysisServices"
/>

# Memory error: You have reached the maximum allowable memory allocation for your tier

## **Recommended Steps**

In Azure Analysis Services, common memory problems such as OOM(Out of Memory) errors during processing/querying, Analysis Services connection timeout, etc. can often be resolved by using the following methods:

1. Check the memory limit for your plan at [Azure Analysis Services pricing](https://azure.microsoft.com/pricing/details/analysis-services/). The default MemoryLimitHigh is 80% of your plan's memory limit. If your server consumes greater than MemoryLimitHigh, it may prevent new sessions from being created or possibly ending them if they were get created. Memory usage can be monitored in Azure portal. To learn more, see [Monitor server metrics](https://docs.microsoft.com/azure/analysis-services/analysis-services-monitor).
2. Check the [MemoryHeapType](https://docs.microsoft.com/sql/analysis-services/server-properties/memory-properties) property. This advanced property is used internally to determine the heap implementation. The default value for servers in Developer and Standard tiers is 5(Hybrid), and Intel TBB for S8/S9 plans. In most cases, the hybrid heap provides better performance for small memory allocations; however, in some cases hybrid heap can result in memory spikes. In such cases, it's recommended you switch to 2(LFH) by using SSMS or by modifying the msmdsrv.ini file. To learn more, see [Configure server properties](https://docs.microsoft.com/sql/analysis-services/server-properties/server-properties-in-analysis-services).
3. If you're unable to connect to the server because of high memory usage, try connecting with a Dedicated Admin Connection to cancel long running sessions and drop some databases to reclaim memory. In SSMS (version 17.3 or higher), this property can be set in the connection dialog by adding it to the **Additional Connection Parameters** tab. For example, `DataSource=asazure://westus.asazure.windows.net/server1;DedicatedAdminConnection=true;`.
4. Upgrade your plan for more available memory. To learn more about plan options, see [Azure Analysis Services pricing](https://azure.microsoft.com/pricing/details/analysis-services/).

## **Recommended Documents**

* [Azure Analysis Services pricing](https://azure.microsoft.com/pricing/details/analysis-services/)
* [Server properties in Analysis Services](https://docs.microsoft.com/sql/analysis-services/server-properties/server-properties-in-analysis-services)
