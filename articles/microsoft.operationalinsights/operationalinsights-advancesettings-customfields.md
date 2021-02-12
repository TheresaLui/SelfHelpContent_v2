<properties
  pagetitle="Custom Fields in Log Analytics"
  service="microsoft.operationalinsights"
  resource="workspaces"
  ms.author="yossiy"
  selfhelptype="Generic"
  supporttopicids="32745410"
  resourcetags=""
  productpesids="15725"
  cloudenvironments="public,fairfax,usnat,ussec,mooncake"
  disableclouds="blackforest"
  articleid="c8800415-6bac-45c4-8fab-bb72c7a306eb"
  ownershipid="AzureMonitoring_LogAnalytics" />
# Custom Fields in Log Analytics

You can remove a custom field by using the following REST request: 

```
Delete https://management.azure.com/subscriptions/{{subscriptionID}}/resourceGroups//{{resourcegroupname}}/providers/Microsoft.OperationalInsights/workspaces/{{loganalyticworkspacename}}/customfields/AzureDiagnostics!{{customfieldsname}}?api-version=2015-11-01-preview
```

## **Recommended Documents**

* [Create custom fields in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/platform/custom-fields#creating-a-custom-field)
* [View custom fields](https://docs.microsoft.com/azure/azure-monitor/platform/custom-fields#viewing-custom-fields)
* [Learn about how to create custom fields in query using patterns](https://docs.microsoft.com/azure/azure-monitor/log-query/parse-text)<br>
