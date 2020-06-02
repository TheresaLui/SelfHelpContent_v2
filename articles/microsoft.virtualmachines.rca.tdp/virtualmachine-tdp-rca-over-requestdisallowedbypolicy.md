<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - over-requestdisallowedbypolicy"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-over-requestdisallowedbypolicy"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to a specific Azure resource policy that has been applied to your subscription by your organization. 
<!--/issueDescription-->

To find out more about the specific policy that blocked your request, [follow the instructions in this article](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy-requestdisallowedbypolicy-error).<br>

For an overview of Resource policies, [read the following article](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy).<br>

To learn more about how to manage resource policies in the Azure portal, [read the following article](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-policy-portal).<br>