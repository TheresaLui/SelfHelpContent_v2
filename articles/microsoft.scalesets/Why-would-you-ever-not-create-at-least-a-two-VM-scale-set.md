<properties
    pageTitle="Why would you ever not create at least a two-VM scale set"
    description="Why would you ever not create at least a two-VM scale set"
    service="scalesets"
    author="negat"
    displayOrder="18"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Why would you ever not create at least a two-VM scale set?


One reason to not create a two-VM scale set would be to use the elastic properties of a scale set. For example, you could deploy a scale set with zero VMs in order to define your infrastructure without paying VM running costs. Then, when you are ready to deploy VMs, you do so by increasing the “capacity” of the scale set to the production instance count.

Another reason is when you’re doing something with your scale set where you don’t care about availability in the same sense as using an availability set with discrete VMs. Scale sets add a way to work with undifferentiated compute units that are fungible. This uniformity is a key differentiator for scale sets vs. availability sets. Many stateless workloads do not care about individual units, and can scale down to one compute unit if the workload drops, then back to many when the workload increases.
