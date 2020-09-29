<properties
    pageTitle="Avere vFXT Client Access Issues"
    description="Resolve issues with Avere vFXT client access."
    infoBubbleText="Avere vFXT Client Access Issues"
    authors="jbut"
    ms.author="jebutl"
    displayOrder="1"
    articleId="averevfxt-clientaccessissues"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32609686"
    resourceTags=""
    productPesIds="16506"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>

# Avere vFXT Client Access Issues

Most client connectivity issues will be resolved by following these steps.

## **Recommended Steps**

1. Determine if the client can ping a client-facing IP address. Use `ping <client-facing-IP-address>` from a Linux or Windows host. If you don't know your client-facing IP addresses, you may find these via the [Avere Control Panel](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-manage-cluster#manage-the-cluster-with-avere-control-panel).

2. If you are connecting via NFS, try connecting to the NFS TCP port (2049). If you are connecting via SMB, try connecting to the SMB TCP port (445). From Linux, `nc -zv <client-facing-IP-address> <port>` From Windows, `Test-NetConnection -ComputerName <client-facing-IP-address> -Port <port>`

3. If the above connectivity tests fail, then you need to [troubleshoot network connectivity between your client and the Avere vFXT](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms)

4. If you have basic network connectivity to the server, try to verify that file system services are running on the remote node. If Linux, run `rpcinfo <client-facing-IP-address>; showmount -e <client-facing-IP-address>` On Windows, connectivity tests may harder if the problem is an authentication problem. A simple connectivity test with Windows is `net view \\<client-facing-IP-address>`

5. If you've verified basic connectivity and that file system services are running, validate that the Avere vFXT cluster is healthy by visiting its management UI and checking for alerts

## **Recommended Documents**

* [Troubleshooting connectivity problems between Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms)
* [Mount the Avere vFXT cluster](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-mount-clients)
* [Access the vFXT cluster](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-cluster-gui)
