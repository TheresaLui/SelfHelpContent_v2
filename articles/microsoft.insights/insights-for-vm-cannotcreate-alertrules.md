<properties
    pageTitle="I can't create alert rules for my VM"
    description="I can't create alert rules for my VM"
    infoBubbleText="Here are some things to help with creating alert rules"
    service="microsoft.insights"
    authors="rashmian"
    ms.author="rashmia"
    selfHelpType="generic"
    articleId="insights-for-vm-cannotcreate-alertrules"
    productPesIds="17081"
    supportTopicIds="32738499"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_Essentials"
 />

 # I can't create alert rules for my VM

## **Recommended Steps**

### **Map and Performance alert rules**

The Performance and Map features collect and send data to your Log Analytics workspace.  You can configure alerts on this data using Log based alert rules. 

For information on creating a log based alert rule, please refer to this article on [Log alerts in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log). 

### **Sample alert queries and rules**

For example queries on data we collect, refer to our [example log searches](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-log-search). 

For example alert rules, refer to [example alert rules](https://docs.microsoft.com/azure/azure-monitor/insights/vminsights-alerts).

To learn how to create alert rules using an example template file and PowerShell script, see the [Alert toolkit](https://github.com/Microsoft/manageability-toolkits).  
