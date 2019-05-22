<properties
	pageTitle="Your low-priority virtual machine was preempted"
	description="Your low-priority virtual machine was preempted"
	infoBubbleText="Your low-priority virtual machine was preempted"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="dushyantgill"
	articleId="servicehealthinsights-microsoft.compute-virtualmachines-healthannotation_virtualmachinepreempted-withendtime"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinepreempted-withendtime"
/>

# Your low-priority virtual machine was preemted

<!--issueDescription-->
At <!--$startTime--> startTime <!--/$startTime--> UTC, your low-priority virtual machine <!--$resourceName--> resourceName <!--/$resourceName--> was preempted.
<!--/issueDescription-->

Low-priority virtual machines take advantage of surplus capacity in Azure to run your Batch workloads. Low-priority virtual machines are less expensive per hour than dedicated virtual machines. Low-priority virtual machines may be preempted when Azure has insufficient surplus capacity. If a low-priority virtual machine is preempted while running tasks, the tasks are requeued and run again once a virtual machine becomes available again. Low-priority virtual machines are a good option for workloads where the job completion time is flexible and the work is distributed across many virtual machines. 

Before you decide to use low-priority virtual machines for your scenario, make sure that any work lost due to preemption will be minimal and easy to recreate.

## Recommended steps

* **Learn more about use cases for low-priority virtual machines**: please refer to the following article: [use low-priority VMs with Batch](https://docs.microsoft.com/azure/batch/batch-low-pri-vms).