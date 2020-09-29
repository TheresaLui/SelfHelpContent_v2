<properties
    pageTitle="Pin performance chart to a dashboard doesn't save the time range"
    description="Pin performance chart to a dashboard doesn't save the time range"
    infoBubbleText="Here are some things to help with pinning a chart to a dashboard"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-pin-perf-chart"
    productPesIds="17081"
    supportTopicIds="32738518"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />


# Pin performance chart to a dashboard doesn't save the time range

## **Recommended Steps**
When you attempt to pin a chart to a dashboard, you notice the option is disabled on the performance chart. This happens when you have configured the performance chart to use a custom time range.

### **Time range using Last X format**

When pinning a chart to a dashboard it uses the time range you selected when that time range is of the format **Last X**.  Examples include Last hour, Last 24 hours, Last 7 days.  These time range formats reference the current time and a range of time in the past relative to the current date and time.  These formats are supported when pinning a chart to your dashboard. 

### **Time range using Custom format**

When your chart is using a custom time range such as **Start on 1/1/2019 1:00 pm** and **End on 1/1/2019 4:00 pm** the pin control is not enabled on the chart.  We do not support pinning charts with specific start and end time to a dashboard.  Over time, the data needed to produce this type of chart is not likely to exist if your Log Analytics workspace is configured with the default 30 days of data retention. 

![Pin to dashboard disabled](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/insights-vm/vminsights-pintodashboard/pin-to-dashboard-01.png?branch=pr-en-us-115799)



