<properties
	pageTitle="Allocation Failure RCA Allocation Success Recommender"
	description="Root cause analysis for 'AllocationFailed' when deploying an existing virtual machine."
	infoBubbleText="Allocation success recommendation found. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="mibufo"
	ms.author="v-mibufo"
	displayOrder=""
	articleId="virtualmachine-tdp-gt-rca-vm-allocation-failure-asr-success-existingvm"
	diagnosticScenario="AllocationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>

# We ran diagnostics on your requested parameters to provide guidance

The Allocation Success Recommender predicts the chance of success for your desired allocation based on the inputs specified. If your desired allocation is blocked or has a low chance of success, then the Recommender provides alternate recommendations with a high chance of success. Recommendations are ranked based on the likelihood of success.<br>

<!--issueDescription-->
The current specification for virtual machine **<!--$VMName-->VMName<!--/$VMName-->** has a **high** chance of allocation success. You can expect see successful deployment allocation for your specified deployment.

We recommend that you try to deploy again, using the same parameters.<br><br>
<!--/issueDescription-->

|Parameter  |Value  |
|---------|---------|
|Subscription ID     |<!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId-->|
|Deployment Scenario|<!--$ Scenario-->Scenario<!--/$Scenario-->|
|Region     |<!--$Region-->Region<!--/$Region-->|
|VM SKU size     |<!--$VMSize-->VMSize<!--/$VMSize-->|
|Instances     |<!--$Instances-->Instances<!--/$Instances-->|

## Alternative Deployments

**<!--$SkuRegRec-->No alternate region or size recommendations<!--/$SkuRegRec-->**<br>
