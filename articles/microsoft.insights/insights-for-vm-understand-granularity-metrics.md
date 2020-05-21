<properties
    pageTitle="I don't understand the time granularity of metrics"
    description="I don't understand the time granularity of metrics"
    infoBubbleText="Here are some things to help with the our charts"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-understand-granularity-metrics"
    productPesIds="17081"
    supportTopicIds="32738512"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

 
# I don't understand the time granularity of metrics

## **Recommended Steps**

### **Data collection sampling frequency**

Data is collected at the following sample rates:

* Every 15 seconds for connections and sent to Azure every 60 seconds
* Every 60 seconds for the performance metrics and sent to Azure every 60 seconds
* Every 60 seconds for health data and sent to Azure every 60 seconds

### **Display of data in our charts**

Charts will use the finest granularity available when viewing an hours worth of data.  When viewing wider time ranges we aggregate the data so that we show no more than 100 points on the chart.  

For example, with a time range of 24 hours for Percent CPU Utilization there would be 1,440 data points for a VM.  We down sample this to 100 data points for purposes of visualizing the chart.  Each data point therefore has 14.4 samples that we can choose from to represent the point on the chart.

When plotting the average value, we get the average across these 14.4 samples and plot that value for the point in the chart.

When plotting the maximum value, we use the maximum value across the 14.4 samples and plot that value for the point on the chart.
