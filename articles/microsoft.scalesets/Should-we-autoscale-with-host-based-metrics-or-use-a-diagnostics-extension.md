<properties
    pageTitle="Should we autoscale with host-based metrics or use a diagnostics extension"
    description="Should we autoscale with host-based metrics or use a diagnostics extension"
    service="scalesets"
    author="negat"
    displayOrder="14"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Should we autoscale with host-based metrics or use a diagnostics extension?


You can create an autoscale setting on a VM to use host-level metrics, or use guest-OS-based metrics.

See this list of supported metrics: https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-autoscale-common-metrics. Here is a full sample for scale sets (in this case we used the host-level CPU metric and a message count metric):

https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-advanced-autoscale-virtual-machine-scale-sets
