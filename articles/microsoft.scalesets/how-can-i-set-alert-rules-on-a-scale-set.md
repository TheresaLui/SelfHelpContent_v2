<properties
    pageTitle="How can I set alert rules on a scale set"
    description="How can I set alert rules on a scale set"
    service="scalesets"
    author="negat"
    displayOrder="15"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How can I set alert rules on a scale set?


You can create alerts on metrics on scale sets via PS or CLI. See:

https://azure.microsoft.com/documentation/articles/insights-powershell-samples/#create-alert-rules

https://azure.microsoft.com/documentation/articles/insights-cli-samples/#work-with-alerts

the TargetResourceId of the scale set looks like: /subscriptions/yoursubscriptionid/resourceGroups/yourresourcegroup/providers/Microsoft.Compute/virtualMachineScaleSets/yourvmssname

You can choose any VM perf counter as the metric to alert on:

https://azure.microsoft.com/documentation/articles/insights-autoscale-common-metrics/#compute-metrics-for-windows-vm-v2-as-a-guest-os

https://azure.microsoft.com/documentation/articles/insights-autoscale-common-metrics/#compute-metrics-for-linux-vm-v2-as-a-guest-os
