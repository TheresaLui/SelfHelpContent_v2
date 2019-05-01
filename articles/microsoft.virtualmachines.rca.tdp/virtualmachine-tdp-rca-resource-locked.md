﻿<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - resource locked"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-resource-locked"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We detected an operation on a locked resource

<!--issueDescription-->
We detected that the operation on virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the resource is locked.<br>
<!--/issueDescription-->

You must unlock the resource add, delete, or modify it. In the **Settings** blade for the resource, resource group, or subscription, select **Locks**. Select the ellipsis and **Delete** from the available options.

If you do not see options to manage locks, you will need elevated rights to access them.

See [Lock resources to prevent unexpected changes](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources) for detailed information included examples for applying and deleting locks using PowerShell, Azure CLI, and REST.



