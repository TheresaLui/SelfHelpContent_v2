<properties
  pagetitle="worker role (paas)/Deployment/Allocation Failures&#xD;"
  description="worker role (paas)/Deployment/Allocation Failures"
  service="microsoft.classiccompute"
  resource="domainnames"
  ms.author="chiragpa"
  selfhelptype="Generic"
  supporttopicids="32565474"
  resourcetags=""
  productpesids="13185"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="0befd66b-e665-48eb-a2e3-7d2348cafbae"
  ownershipid="Compute_CloudServices_Content" />
# worker role (paas)/Deployment/Allocation Failures

## **Recommended Steps**

When you deploy instances to an Azure Cloud Service, or add new web or worker role instances, Microsoft Azure allocates compute resources. You may occasionally receive errors during these operations even before you reach the Azure subscription limit. 

1. To find the signature of the failure in Azure portal, navigate to your Cloud service (classic), and in the sidebar select **Operation log** (classic) to view the logs.<br>

2. Depending upon the failure signature, check for the matching article in the next section to learn how to resolve it.

## **Recommended Documents**

### Articles by Failure signature
* [FabricInternalServerError or ServiceAllocationFailure](https://docs.microsoft.com/azure/cloud-services/cloud-services-troubleshoot-fabric-internal-server-error)<br>
* [LocationNotFoundForRoleSize](https://docs.microsoft.com/azure/cloud-services/cloud-services-troubleshoot-location-not-found-for-role-size)<br>
* [ConstrainedAllocationFailed](https://docs.microsoft.com/azure/cloud-services/cloud-services-troubleshoot-constrained-allocation-failed)<br>
* [OverconstrainedAllocationRequest](https://docs.microsoft.com/azure/cloud-services/cloud-services-troubleshoot-overconstrained-allocation-request)<br>

### General Allocation failures articles
* [How Allocation works and why it fails](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures)<br>
* [Available sizes and options for Cloud Service role instances (web and worker roles)](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs)<br>
* [Cloud Service Deployment Failure FAQs](https://docs.microsoft.com/azure/cloud-services/cloud-services-deployment-faq)<br>
* [Allocation Failure Remediations](https://azure.microsoft.com/blog/allocation-failure-and-remediation/)
