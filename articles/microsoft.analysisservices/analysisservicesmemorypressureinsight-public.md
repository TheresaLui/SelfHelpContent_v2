<properties
    pageTitle="There is memory pressure on the server."
    description="Memory Pressure"
    infoBubbleText="There is memory pressure on the server. See details on the right."
    service="microsoft.analysisservices"
    resource="servers"
    authors="brspie"
    ms.author="brspie"
    displayOrder=""
    articleId="analysisservicesmemorypressureinsight"
    diagnosticScenario="analysisservicesmemorypressureinsight"
    selfHelpType="diagnostics"
    supportTopicIds="32558776"
    resourceTags=""
    productPesIds="1003281"
    cloudEnvironments="Public, Fairfax, MoonCake, usnat, ussec"
    ownershipId="AzureData_AnalysisServices"
/>

# There is memory pressure on the server
<!--issueDescription-->
There is memory consumption higher than **<!--$MemoryLimitHigh-->MemoryLimitHigh<!--/$MemoryLimitHigh--> GB** on the server. The memory usage is **<!--$MemoryUsage-->MemoryUsage<!--/$MemoryUsage--> GB** and the hard limit is **<!--$MemoryLimitHard-->MemoryLimitHard<!--/$MemoryLimitHard--> GB**.
<!--/issueDescription-->


## **Recommended Steps**

We have identified there is memory pressure on your server which can impact your query and processing performance. We recommend scaling up to a higher tier to improve your performance. Please review the [Azure Analysis Services pricing](https://azure.microsoft.com/pricing/details/analysis-services/) page for more details on Tiers and Memory Limits.

## **Recommended Documents**

* [Azure Analysis Services pricing](https://azure.microsoft.com/pricing/details/analysis-services/)
