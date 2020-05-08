<properties
    pageTitle="There are long running commands or queries."
    description="Long running commands or queries"
    infoBubbleText="There are long running commands or queries. See details on the right."
    service="microsoft.analysisservices"
    resource="servers"
    authors="brspie"
    ms.author="brspie"
    displayOrder=""
    articleId="analysisserviceslongrunningqueryinsight"
    diagnosticScenario="analysisserviceslongrunningqueryinsight"
    selfHelpType="diagnostics"
    supportTopicIds="32675705"
    resourceTags=""
    productPesIds="1003281"
    cloudEnvironments="Public, Fairfax, MoonCake, usnat, ussec"
    ownershipId="AzureData_AnalysisServices"
/>

# There are long running commands or queries on the server

<!--issueDescription-->
There is memory consumption higher than **<!--$MemoryLimitHigh-->MemoryLimitHigh<!--/$MemoryLimitHigh--> GB** on the server. The memory usage is **<!--$MemoryUsage-->MemoryUsage<!--/$MemoryUsage--> GB** and the hard limit is **<!--$MemoryLimitHard-->MemoryLimitHard<!--/$MemoryLimitHard--> GB**.
<!--/issueDescription-->

## **Recommended Steps**

You may need to enable diagnostics on the Azure Analysis Service instance in order to identify the specific query or command and take action. Please review the [Setup diagnostic logging](https://docs.microsoft.com/azure/analysis-services/analysis-services-logging) page for more details on diagnostic logging.

Please review the [Best practices for long running operations](https://docs.microsoft.com/azure/analysis-services/analysis-services-long-operations) page for additional related content.

## **Recommended Documents**

* [Setup diagnostic logging](https://docs.microsoft.com/azure/analysis-services/analysis-services-logging)
* [Best practices for long running operations](https://docs.microsoft.com/azure/analysis-services/analysis-services-long-operations)
