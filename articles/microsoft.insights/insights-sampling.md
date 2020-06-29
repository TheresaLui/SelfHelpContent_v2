<properties 
    pageTitle="Issue configuring sampling from my code"
    description="General troubleshooting guide for sampling configuration"
    service="microsoft.insights"
    resource="components"
    authors="osvaldorosado"
    ms.author="osrosado"
    articleId="insights-sampling"
    displayOrder="97"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32729606"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# Issue configuring sampling from my code

## **Recommended Steps**
### **Overriding default sampling**

The method to configure sampling, and the default behavior of sampling, depends on the specific SDK implementation you are using. SDKs typically provide means for **Adaptive Sampling** where the sample rate varies with incoming request rate, and **Fixed Sampling** where the sampling rate is a fixed constant.

Follow the guides in [Sampling in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/sampling) to configure sampling from your code for the specific SDK implementation you are using and the kind of sampling you wish to configure.

### **Is sampling taking effect?**

You can use the following Logs query to see the actual sampling rate per type of telemetry item:

~~~kusto
union requests,dependencies,pageViews,browserTimings,exceptions,traces
| where timestamp > ago(1d)
| summarize RetainedPercentage = 100/avg(itemCount) by bin(timestamp, 1h), itemType
~~~

If you see that `RetainedPercentage` for any type is less than `100`, then that type of telemetry is being sampled.


## **Recommended Documents**

* [Sampling in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/sampling)
