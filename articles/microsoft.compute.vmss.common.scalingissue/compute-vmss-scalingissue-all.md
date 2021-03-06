<properties
	pageTitle="Scaling issue with my scale set"
	description="Scaling issue with my scale set"
	service="microsoft.compute"
	resource=""
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32641082,32641116,32641131,32641132,32641133,32641142"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="83305c9c-1097-4a09-88a6-f6bd85717bf5"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>

# Scaling issue with my scale set

## **Recommended Steps**

For general troubleshooting, follow these guides:<br>

1. Understand your specific error ([SkuNotAvailable](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-sku-not-available), [Quota Limit](https://docs.microsoft.com/azure/azure-resource-manager/templates/error-resource-quota), or [Allocation Failure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure))<br>
2. Deploy to another region <br>
3. Use another size in the given region ([Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm) or [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size))

## Autoscale Best Practices

* [Ensure the maximum and minimum values are different and have an adequate margin between them](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#ensure-the-maximum-and-minimum-values-are-different-and-have-an-adequate-margin-between-them)
* [Manual scaling is reset by autoscale min and max](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#manual-scaling-is-reset-by-autoscale-min-and-max)
* [Choose the appropriate statistic for your diagnostics metric](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#choose-the-appropriate-statistic-for-your-diagnostics-metric)
* [Choose the thresholds carefully for all metric types](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#choose-the-thresholds-carefully-for-all-metric-types)
* [Considerations for scaling threshold values for special metrics](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#considerations-for-scaling-threshold-values-for-special-metrics)
* [Considerations for scaling when multiple profiles are configured in an autoscale setting](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#considerations-for-scaling-when-multiple-profiles-are-configured-in-an-autoscale-setting)
* [Considerations for scaling when multiple rules are configured in a profile](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#considerations-for-scaling-when-multiple-rules-are-configured-in-a-profile)
* [Always select a safe default instance count](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#always-select-a-safe-default-instance-count)
* [Configure autoscale notifications](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-best-practices#configure-autoscale-notifications)

## **Recommended Documents**

* [FAQ for VMSS](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq)<br>
* [Best practices for Azure AutoScale](https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-autoscale-best-practices)<br>
* [Learn how to scale up and scale down - vertical scaling](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-vertical-scale-reprovision)<br>
* [Learn how to scale out and scale in - horizontal scaling](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-vertical-scale-reprovision)<br>
* [Troubleshoot FAQ for VMSS](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq#troubleshooting)
