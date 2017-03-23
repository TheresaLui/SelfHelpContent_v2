<properties
    pageTitle="Why would you ever create a scale set with fewer than 2 VMs"
    description="Why would you ever create a scale set with fewer than 2 VMs"
    service="microsoft.compute"
    resource="virtualmachinescalesets"
    author="gatneil"
    displayOrder="49"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Why would you ever create a scale set with fewer than 2 VMs

Why would you ever create a scale set with fewer than 2 VMs?


One reason would be to use the elastic properties of a scale set. For example, you could deploy a scale set with zero VMs in order to define your infrastructure without paying VM running costs. Then, when you are ready to deploy VMs, you do so by increasing the “capacity” of the scale set to the production instance count.

Another reason is when you’re doing something with your scale set where you don’t care about availability in the same sense as using an availability set with discrete VMs. Scale sets add a way to work with undifferentiated compute units that are fungible. This uniformity is a key differentiator for scale sets vs. availability sets. Many stateless workloads do not care about individual units, and can scale down to one compute unit if the workload drops, then back to many when the workload increases.

Refer to [this documentation](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-portal-create) to see how to deploy a scale set from the portal.
