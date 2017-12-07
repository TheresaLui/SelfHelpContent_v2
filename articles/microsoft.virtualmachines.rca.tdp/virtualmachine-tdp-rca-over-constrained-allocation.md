﻿<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-over-constrained-allocation"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-over_constrained_allocation"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"   
	productPesIds="14749,15571"  
	cloudEnvironments="public"
/>
# We detected a recent issue with your deployment attempt:

<!--issueDescription-->
We identified that your deployment failed for **<!--$vmname-->Virtual machine<!--/$vmname-->:** at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. There are currently not enough cores of the VM Size Family you requested in this region. 
<!--/issueDescription-->

This is not a quota issue. To self-mitigate, please use a different VM Size Family or a different region.<br>

To learn more about sizes supported in each region:<br>
* Products available by region, [follow these instructions](https://azure.microsoft.com/regions/services/)<br>

To learn more about troubleshooting allocation failures when you create, restart, or resize:<br>
* [Windows troubleshooting](https://docs.microsoft.com/azure/virtual-machines/windows/allocation-failure)<br>
* [Linux troubleshooting](https://docs.microsoft.com/azure/virtual-machines/linux/allocation-failure)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>