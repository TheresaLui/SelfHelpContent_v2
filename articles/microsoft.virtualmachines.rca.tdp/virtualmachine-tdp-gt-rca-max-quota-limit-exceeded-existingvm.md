
<properties
	pageTitle="Deployment Failure RCA"
	description="Root cause analysis for 'maximum quota limit exceeded' when deploying an existing virtual machine."
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="mibufo"
	ms.author="v-mibufo"
	displayOrder=""
	articleId="virtualmachine-tdp-gt-rca-max-quota-limit-exceeded-existingvm"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# We found a Quota limitation on your subscription

<!--issueDescription-->
We have detected that the deployment of VM size **<!--$VMSize-->VM Size<!--/$VMSize-->** in region **<!--$Region-->Region<!--/$Region-->** failed due to the virtual CPU quota being exceeded for the requested resource.<br>

The virtual machine **<!--$VMName-->Virtual machine<!--/$VMName-->** was unable to deploy the following instances:<br> **<!--$Instances-->Instances<!--/$Instances-->**
<!--/issueDescription-->

We apologize for the inconvenience. Due to various technical constraints, vCPU quotas for virtual machines and virtual machine scale sets are enforced at two tiers for each subscription, in each region. The first tier is the **Total Regional vCPUs** limit (across all VM Series), and the second tier is the **per VM Series vCPUs** limit (such as the D-series vCPUs).

## **Recommended Steps**

To identify the quota limit you are encountering for subscription **<!--$SubscriptionID-->SubscriptionID<!--/$SubscriptionID-->**, use the Azure CLI command [az vm list-usage](https://docs.microsoft.com/azure/virtual-machines/linux/quotas#check-usage).

### Submit Quota Increase Request

* If you are encountering a **Total Regional vCPUs** limit, deploy your desired size by following the steps in [Regional vCPU Quota Increase](https://docs.microsoft.com/azure/azure-supportability/regional-quota-requests#request-total-regional-vcpus-quota-increase-at-subscription-level-using-the-help--support-blade) to submit a streamlined request for increasing the **Total Regional vCPUs** limit
* If you are encountering a **per VM Series vCPUs** limit, deploy your desired size by following the steps in [VM Series vCPU Limit Increase](https://docs.microsoft.com/azure/azure-supportability/per-vm-quota-requests#request-per-vm-series-vcpu-quota-increase-at-subscription-level-using-the-help--support-blade) to submit a streamlined request for increasing the **per VM Series vCPUs** limit.

### Consider Alternate Sizes or Locations

Quota increase requests may take one or more business days to be approved due to business and technical constraints. Consider alternate sizes available to deploy for your subscription. You can use the Azure CLI command [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) to check for the VM sizes available in a region, and any deployment restrictions on the VM size.

## **Recommended Documents**

* [Understand Quota Limits](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)
* [Azure subscription and service limits, quotas, and constraints](https://docs.microsoft.com/azure/azure-subscription-service-limits)<br>
* [Check Azure Resource Quota and Limits in Portal](https://docs.microsoft.com/azure/networking/check-usage-against-limits)
