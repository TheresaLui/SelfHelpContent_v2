<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - over-requestdisallowedbypolicy"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachinescalesets"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="VMSS_DeploymentFailure_rca-over-requestdisallowedbypolicy"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32641079,32641082,32641076,32641075,32641080,32641074,32641076,32641077,32641072,32641073"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine scale set **<!--$vmssname-->Virtual machine scale set<!--/$vmssname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to a specific Azure resource policy that has been applied to your subscription by your organization.
<!--/issueDescription-->

To find out more about the specific policy that blocked your request, [follow the instructions in this article](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy-requestdisallowedbypolicy-error).<br>

For an overview of Resource policies, [read the following article](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy).<br>

To learn more about how to manage resource policies in the Azure portal, [read the following article](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy-portal).<br>
