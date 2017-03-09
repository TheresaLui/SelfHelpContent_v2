<properties
    pageTitle="Are there any examples of autoscaling based on a service bus topic and queue length"
    description="Are there any examples of autoscaling based on a service bus topic and queue length"
    service="scalesets"
    author="negat"
    displayOrder="13"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Are there any examples of autoscaling based on a service bus topic and queue length?

Yes. See:
https://azure.microsoft.com/documentation/articles/insights-autoscale-common-metrics/
for service bus queue:
```json
"metricName": "MessageCount",
"metricNamespace": "",
"metricResourceUri": "/subscriptions/s1/resourceGroups/rg1/providers/Microsoft.ServiceBus/namespaces/mySB/queues/myqueue"
For storage queues use this format:
```json
"metricName": "ApproximateMessageCount",
"metricNamespace": "",
"metricResourceUri": "/subscriptions/s1/resourceGroups/rg1/providers/Microsoft.ClassicStorage/storageAccounts/mystorage/services/queue/queues/mystoragequeue"
replace these sample values with the appropriate resource URIs.