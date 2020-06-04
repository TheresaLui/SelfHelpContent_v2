<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-over-constrained-allocation SkuRegRec"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-over_constrained_allocation-SkuRegRec"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"   
	productPesIds="14749,15571"  
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

The Region this VM is associated with did not have enough capacity for the requested VM size at the time of deployment to support its allocation.<br>

>We are currently experiencing high demand for specific regions across the globe. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://aka.ms/CloudCovidResponseFAQ).<br>

<!--issueDescription-->
Based on the analysis of deployment failure: **<!--$CorrelationId-->CorrelationId<!--/$CorrelationId-->**, we saw that deployment failed for the resource **<!--$vmname-->myVM<!--/$vmname-->** in region: **<!--$Region-->Region<!--/$Region-->** for size: **<!--$VMSize-->VMSize<!--/$VMSize-->** due to an allocation failure.<br>

**<!--$SkuRegRec-->No information provided<!--/$SkuRegRec-->**<br>
<!--/issueDescription-->

## **Recommended Steps**

Consider the above alternate VM sizes and/or Regions for your deployment. These recommendations are generated based on the current capacity conditions. If you see the originally requested region and size in the recommendations, please try creating the VM again as the issue might have been temporary and there could be sufficient resources for allocation currently.<br>

## **Recommended Documents**

To learn more about sizes supported in each region:<br>
* Products available by region, [follow these instructions](https://azure.microsoft.com/regions/services/)<br>

To learn more about troubleshooting allocation failures when you create, restart, or resize:<br>
* [Windows troubleshooting](https://docs.microsoft.com/azure/virtual-machines/windows/allocation-failure)<br>
* [Linux troubleshooting](https://docs.microsoft.com/azure/virtual-machines/linux/allocation-failure)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
