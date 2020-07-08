<properties
    pageTitle="Azure HPC Cache Performance Issues"
    description="Resolve Azure HPC Cache Performance Issues."
    infoBubbleText="Resolve Azure HPC Cache Performance Issues."
    authors="cfriedel"
    ms.author="clfriede"
    displayOrder="1"
    articleId="storagecache-performance"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32674487"
    resourceTags=""
    productPesIds="16790"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="StorageMediaEdge_HPCCache"
/>

# Azure HPC Cache Performance Issues

We have created this self-help article to assist with possible performance issues on the Azure HPC Cache.  

## **Recommended Steps**

1. Validate that the Azure HPC Cache is in a healthy state by visiting the Azure HPC Cache resource overview page and verifying that the status shown is Healthy.

2. Determine if a client can ping one of the mount addresses of the HPC cache. Use `ping <HPC-mount-address>` from a Linux or Windows host. Ensure that there are no packets being dropped or signs of latency between the client and the Azure HPC Cache.  If you do see connectivity or latency issues between the client and the Azure HPC Cache, please consult [Troubleshooting Network Connectivity Between Your Client and the Avere HPC Cache](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms).

3. If the Azure HPC Cache is showing a Healthy status and the clients can reach the Azure HPC Cache, please review the metrics by clicking Metrics under the Monitoring heading on the left-hand menu of the Azure HPC Cache resource overview page.  If clients are connected, you should see values on the graphs provided, including cache throughput, cache operations/sec and cache client-facing latency.  If you have questions about performing this task, please review the [Monitor the Azure HPC Cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-manage) page.


## **Recommended Documents**

* [Azure HPC Cache Documentation](https://docs.microsoft.com/azure/hpc-cache/)
* [Troubleshooting Network Connectivity Between Your Client and the Avere HPC Cache](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms)
* [Monitor the Azure HPC Cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-manage)
