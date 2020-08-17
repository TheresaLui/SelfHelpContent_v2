<properties
    pageTitle="Azure HPC Cache Client Access Issues"
    description="Resolve issues with Azure HPC Cache client access."
    infoBubbleText="Azure HPC Cache Client Access Issues"
    authors="cfriedel"
    ms.author="clfriede"
    displayOrder="1"
    articleId="storagecache-clientaccessissues"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32674483"
    resourceTags=""
    productPesIds="16790"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="StorageMediaEdge_HPCCache"
/>

# Azure HPC Cache Client Access Issues

Most client connectivity issues will be resolved by completing the following steps.  Before attempting to complete the steps below, please make sure that you have your mount addresses from your HPC cache available as you will need them. If you do not know your mount addresses, the mount IPs are listed in the HPC Cache resource overview as mount addresses.

## **Recommended Steps**

1. First, validate that the Azure HPC Cache is healthy by visiting the Azure HPC Cache resource overview page and verifying that the status shown is Healthy.

2. Determine if a client can ping one of the mount addresses of the HPC cache. Use `ping <HPC-mount-address>` from a Linux or Windows host.

3. If you are connecting via NFS, try connecting to the NFS TCP port (2049) on one of the mount addresses.  From Linux, run `nc -zv <mount-address> <port>`. From Windows, you can use the powershell command `Test-NetConnection -ComputerName <mount-address> -Port <port>`.

4. If the above connectivity tests fail, you will need to [troubleshoot network connectivity between your client and the Avere HPC Cache](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms).

5. If you have basic network connectivity to a HPC cache mount address, try to verify that file system services are running on the remote node. If your client is Linux, run the following command `rpcinfo -p <mount-address>; showmount -e <mount-address>`.  This should show the RPC ports available on the HPC cache, as well as the root export.

## **Recommended Documents**

* [Troubleshooting Connectivity Problems Between Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms)
* [Mount the Azure HPC Cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-mount)
