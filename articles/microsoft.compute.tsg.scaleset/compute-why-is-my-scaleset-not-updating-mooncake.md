<properties
    pageTitle="Why is my scale set not updating"
    description="Why is my scale set not updating"
    service="microsoft.compute"
    resource="virtualmachinescalesets"
    authors="scottAzure"
    ms.author="scotro"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="MoonCake"
    articleId="e0652396-ba3f-449e-b872-31dd98109087"
	ownershipId="Compute_VirtualMachines"
/>

# Why is my scale set not updating

If you update your scale set but the running VMs don't update, this is likely because your upgrade policy mode is set to "Manual". In this mode, changes to the scale set apply to new VMs immediately but are only applied to existing VMs when you call manual upgrade on an existing VM. You can do this programmatically or from the Azure Portal in the "Instances" blade of the scale set. If you wish for updates to automatically be applied to all VMs in the scale set in parallel, you can set the upgrade policy mode to "Automatic" instead.

## **Recommended Documents**

For more information about updating a scale set, see [this article](https://docs.azure.cn/virtual-machine-scale-sets/virtual-machine-scale-sets-deploy-app) that describes how to deploy, manage, and upgrade an app on a scale set.
