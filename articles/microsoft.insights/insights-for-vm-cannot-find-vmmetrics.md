<properties
     pageTitle="I cannot find some of my VM metrics in Azure Metrics Explorer"
    description="I cannot find some of my VM metrics in Azure Metrics Explorer"
    infoBubbleText="Here are some things to help with metrics explorer"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-cannot-find-vmmetrics"
    productPesIds="17081"
    supportTopicIds="32738504"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />


# I cannot find some of my VM metrics in Azure Metrics Explorer

## **Recommended Steps**

After you have enabled Azure Monitor for VMs, your monitoring data will be collected and stored in a Log Analytics workspace.  The performance data sets which have data for CPU, memory, disk and more are saved in the `InsightsMetrics` table in the workspace.  For information about this table, refer to our documentation. 

If you are trying to chart data from the `InsightsMetric` table in Metrics Explorer, you won't find it by setting the scope to your VM.  You need to set the scope of the chart to reference the Log Analytics workspace that contains the monitoring data for your VM.  By default, the chart averages the selected metric across all VMs reporting that data set to the workspace. 

![Metrics explorer](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/insights-vm/vminsights-metricsexplorer/metrics-explorer-01.png?branch=pr-en-us-115799)

You can choose the option to [Apply splitting](https://docs.microsoft.com/azure/azure-monitor/platform/metrics-charts#apply-splitting-to-a-chart) and split the metric by dimensions based on Computer name, but this is only effective for workspaces with 50 or fewer computers reporting data to the workspace.  

![Metrics explorer with splitting applied](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/insights-vm/vminsights-metricsexplorer/metrics-explorer-02.png?branch=pr-en-us-115799)

### **Log query and chart** 

To create custom charts for a particular VM or set of VMs, we recommend running log queries in Log Analytics and then [render charts](https://docs.microsoft.com/azure/azure-monitor/log-query/charts) from within the query view where you have more control of the data presented in the charts. 
