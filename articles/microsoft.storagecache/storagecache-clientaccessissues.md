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
    cloudEnvironments="public"
/>

# Azure HPC Cache Client Access Issues

Most client connectivity issues will be resolved by completing the following these steps.

## **Recommended Steps**

1. Determine if a client can ping one of the mount addresses of the HPC cache. Use `ping <HPC-mount-address>` from a Linux or Windows host. If you do not know your mount addresses, the IPs are listed in the HPC Cache resource overview as mount addresses.

2. If you are connecting via NFS, try connecting to the NFS TCP port (2049) on one of the mount addresses.  From Linux, `nc -zv <mount-address> <port>` From Windows, you can use the powershell command `Test-NetConnection -ComputerName <mount-address> -Port <port>`

3. If the above connectivity tests fail, then you need to [troubleshoot network connectivity between your client and the Avere HPC Cache](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms)

4. If you have basic network connectivity to a HPC cache mount address, try to verify that file system services are running on the remote node. If your client is Linux, run `rpcinfo <client-facing-IP-address>; showmount -e <client-facing-IP-address>`.

5. If you've verified basic connectivity and that file system services are running, validate that the Azure HPC cluster is healthy by visiting its resource overview page.  The status should be listed as healthy.

## **Recommended Documents**

* [Troubleshooting connectivity problems between Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms)
* [Mount the Azure HPC Cache](https://docs.microsoft.com/en-us/azure/hpc-cache/hpc-cache-mount)
