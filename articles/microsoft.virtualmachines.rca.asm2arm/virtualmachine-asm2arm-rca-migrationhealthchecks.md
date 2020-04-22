<properties
	pageTitle="ASM to ARM Failure Health Check RCA"
	description="RCA - ASM to ARM Failure Health Check RCA"
	infoBubbleText="Found recent deployment failure. See details on the right"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="ASM2ARM_RCA-migrationhealthchecks"
	diagnosticScenario="ASM2ARMHealthChecks"
	selfHelpType="rca"
	supportTopicIds="32513964"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected the following configuration settings in the virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** or its virtual networking **<!--$VNET-->VNET<!--/$VNET-->** are preventing the migration to succeed:

<!--$Req-->Results<!--/$Req-->
<!--/issueDescription-->

To view these and other unsupported features and best-practices, [please visit this link](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-overview#unsupported-features-and-configurations)<br>
