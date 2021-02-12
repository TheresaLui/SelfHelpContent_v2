<properties
    pageTitle="I don't understand a specific metric"
    description="I don't understand a specific metric"
    infoBubbleText="Here are some things to help with the metrics we collect"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-understand-specific-metric"
    productPesIds="17081"
    supportTopicIds="32738510"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

 
# I don't understand a specific metric

## **Recommended Documents**

Azure Monitor for VMs collects several different types of metrics and monitoring data. 

For performance metrics, the list of metrics we collect [can be found here](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-log-search#performance-records).  This data is stored in the Insights Metrics table, with one record every minute.  

To enable additional performance counters that will be stored in the Perf table, refer to [this documentation](https://docs.microsoft.com/azure/azure-monitor/platform/data-sources-performance-counters). 

We also collect network connection data for processes on a VM that are accepting inbound connections, are making outbound connections, or are bound to a port.  Additional information about these data sets can be [found here](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-log-search). 
