<properties
	pageTitle="My deployment fails with allocation errors"
	description="My deployment fails with allocation errors"
	service="microsoft.classiccompute"
	resource="domainnames"
	authors="jluk"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	 
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="06689373-2b72-4fb3-b8d9-189d28ec8228"
	ownershipId="Compute_VirtualMachines"
/>

# My deployment fails with allocation errors

Your Cloud Service deployment (Staging or Production) can get pinned to a single cluster. When deployments fail when the cluster reaches its capacity, try the following steps:<br>

## **Recommended steps**

1. Wait and retry the deployment operation.<br>

	Resources may be freed up on the cluster after waiting that allow the deployment or scaling request to succeed.<br>

2. Deploy your package to a new cloud service.<br>

	Deploying to a new cloud service often goes on a new cluster with enough capacity. If successful, update the DNS to point to the new cloud service.<br>

3. Delete both production and staging slots and redeploy to the existing cloud service.<br>

	The new deployment goes to a cluster that has enough capacity. However, redeploying incurs downtime until the new deployment is ready.<br>

4. Remove the affinity group and [migrate to a Regional Virtual Network](https://azure.microsoft.com/documentation/articles/virtual-networks-migrate-to-regional-vnet/)

## **Recommended documents**

* [About Cloud Services allocation failures](https://azure.microsoft.com/documentation/articles/cloud-services-allocation-failures/)<br>
* [About general allocation failures](https://azure.microsoft.com/blog/allocation-failure-and-remediation/)
