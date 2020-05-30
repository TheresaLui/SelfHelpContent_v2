<properties
    pageTitle="What metrics can I use to autoscale my scale set"
    description="What metrics can I use to autoscale my scale set"
    service="microsoft.compute"
    resource="virtualmachinescalesets"
    authors="scottAzure"
    ms.author="scotro"
    displayOrder="9"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="MoonCake"
    articleId="compute-autoscale-metrics-mooncake"
	ownershipId="Compute_VirtualMachines"
/>

# What metrics can I use to autoscale my scale set

There are two kinds of metrics for VMs and scale sets in Azure: host and guest metrics. Host metrics come from the VM host, while guest metrics come from the guest OS. All VMs automatically emit host metrics, but to see guest metrics, you need to add either the Windows Diagnostics Extension or the Linux Diagnostics Extension to your VMs/scale sets.

## **Recommended Documents**

For more information, see [this documentation](https://docs.azure.cn/azure-monitor/platform/autoscale-common-metrics) that describes commonly used metrics.
