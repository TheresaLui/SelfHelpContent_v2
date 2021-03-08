<properties
    pageTitle="Azure  - VM to internet (Outbound) connectivity"
    description="Azure  - VM to internet (Outbound) connectivity"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="v-miegge"
    editor="v-jesits"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32785489"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="c28d2536-4e1f-45da-aecb-42f717183505"
/>

# VM to internet (Outbound) connectivity

The following diagnostic steps can help you to identify issues that affect the internet connectivity of Microsoft Azure virtual machines.

The most common issues in this scenario are blocking network security groups (NSGs) and virtual machine (VM) firewall and application issues.

## **Recommended Steps**

1. In [the Azure portal](https://portal.azure.com), navigate to the **Virtual Machine resource** that is experiencing the outbound internet connectivity issue. The resource will default to the **Overview** blade in the left pane.

2. Scroll to the bottom of the **Overview** blade, and select **Connection Troubleshoot** under the **Support + Troubleshooting** header.

3. Select **Outbound Connections**, and then specify the following options:

   - Connection Destination: **Other IP address/CIDR**
   - IP address/CIDR: the internet protocol (IP) address that you are trying to connect to (or enter **8.8.8.8** for a general internet connectivity check)
   - Service: **HTTPS**
   - Port: Leave set as **443**
   - Protocol: Leave set as **TCP**

4. Select **Test connection**.

5. If the connection fails, the test results will indicate which NSG or UDR is interfering with connectivity.

6. If the connection is successful, this means that the Azure platform is allowing outbound internet connectivity. Check within the VM for configuration issues in the destination configuration.

## **Recommended Documents**

- [Network security groups - Outbound](https://docs.microsoft.com/azure/virtual-network/network-security-groups-overview#outbound)
- [Check remote endpoint connectivity](https://docs.microsoft.com/azure/network-watcher/network-watcher-connectivity-portal#check-remote-endpoint-connectivity)
