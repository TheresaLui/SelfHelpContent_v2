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
	cloudEnvironments="MoonCake"
/>

# My deployment fails with allocation errors
Your Cloud Service deployment (Staging or Production) can get pinned to a single cluster. Deployments fail when the cluster reaches its capacity. Try the following steps:

## **Recommended steps**

1. Wait and retry the deployment operation.<br>
Resources may be freed up on the cluster after waiting that allow the deployment or scaling request to succeed.   
2. Deploy your package to a new cloud service.<br>
Deploying to a new cloud service often goes on a new cluster with enough capacity. If successful, update the DNS to point to the new cloud service. 
3. Delete both production and staging slots and redeploy to the existing cloud service.<br>
The new deployment goes to a cluster that has enough capacity. However, redeploying incurs downtime until the new deployment is ready. 
4. Remove the affinity group and [migrate to a Regional Virtual Network](https://docs.azure.cn/virtual-network/virtual-networks-migrate-to-regional-vnet/)
 
## **Recommended documents**
[About Cloud Services allocation failures](https://docs.azure.cn/cloud-services/cloud-services-allocation-failures/) <br>
[About general allocation failures](https://azure.microsoft.com/blog/allocation-failure-and-remediation/)
