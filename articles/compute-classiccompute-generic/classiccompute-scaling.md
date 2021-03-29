<properties
  pagetitle="worker role (paas)/configuration and management/scaling&#xD;"
  description="worker role (paas)/configuration and management/scaling"
  service="microsoft.classiccompute"
  resource="domainnames"
  ms.author="chiragpa"
  selfhelptype="Generic"
  supporttopicids="32569897"
  resourcetags=""
  productpesids="13185"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="aa0b9406-4e53-48ee-8d38-9c7e0c4aa58f"
  ownershipid="Compute_CloudServices_Content" />
# worker role (paas)/configuration and management/scaling

## **Recommended Steps**

When you scale up a Cloud Service, Microsoft Azure try to allocates compute resources as per the request. You may occasionally receive errors during these operations even before you reach the Azure subscription limit. 

To find the signature of the failure in Azure portal:
1. Navigate to your Cloud service (classic) and in the sidebar select Operation log (classic) to view the logs.<br>
2. Depending upon the failure signature, check for the matching article in the next section to learn how to resolve it.

## **Recommended Documents**

### Articles by Failure signature
* [FabricInternalServerError or ServiceAllocationFailure](https://docs.microsoft.com/azure/cloud-services/cloud-services-troubleshoot-fabric-internal-server-error)<br>
* [LocationNotFoundForRoleSize](https://docs.microsoft.com/azure/cloud-services/cloud-services-troubleshoot-location-not-found-for-role-size)<br>
* [ConstrainedAllocationFailed](https://docs.microsoft.com/azure/cloud-services/cloud-services-troubleshoot-constrained-allocation-failed)<br>
* [OverconstrainedAllocationRequest](https://docs.microsoft.com/azure/cloud-services/cloud-services-troubleshoot-overconstrained-allocation-request)<br>

### General Scaling Best Practices articles
* [How to Scale your Cloud Services?](https://azure.microsoft.com/documentation/articles/cloud-services-how-to-scale/) <br>
* [How to change the VM size of an existing role](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs#changing-the-size-of-an-existing-role)<br>
* [Not able to scale more than 25 instances?](https://azure.microsoft.com/documentation/articles/vs-azure-tools-debug-cloud-services-virtual-machines/#limitations-of-remote-debugging-in-azure)<br>
* [Auto-Scaling isn't happening as expected?](https://blogs.msdn.microsoft.com/cie/2017/01/03/troubleshooting-azure-auto-scale-profile-does-not-change/)
* [How Allocation works and why it fails](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures)<br>
* [Available sizes and options for Cloud Service role instances (web and worker roles)](https://docs.microsoft.com/azure/cloud-services/cloud-services-sizes-specs)<br>
