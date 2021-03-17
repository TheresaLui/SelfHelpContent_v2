<properties
    pageTitle="Azure  - Internet to VM (Inbound) connectivity"
    description="Azure  - Internet to VM (Inbound) connectivity"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="v-miegge"
    editor="v-jesits"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32785488"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="42a1e521-5fb1-4dc2-8a14-f8665993fff4"
/>

# Internet to VM (Inbound) connectivity

The following diagnostic steps can help you to identify issues that affect the internet connectivity of Microsoft Azure virtual machines.

The most common issues in this scenario are blocking network security groups (NSGs) and user-defined routes (UDRs).

## **Recommended Steps**

1. In [the Azure portal](https://portal.azure.com), navigate to the **Virtual Machine resource** that is experiencing the inbound internet connectivity issue. The resource will default to the **Overview** blade in the left pane.

2. Scroll to the bottom of the **Overview** blade, and select **Connection Troubleshoot** under the **Support + Troubleshooting** header.

3. Select **Inbound connections**, and then specify the following options:

   - Connection source: **Other IP address/CIDR**
   - IP address/CIDR: **My IP address**
   - Service: **HTTPS**
   - Port: Leave set as **443**
   - Protocol: Leave set as **TCP**

4. Select **Test connection**.

5. If the connection fails, the test results will indicate which NSG or UDR is interfering with connectivity.

6. If the connection is successful, this means that the Azure platform is allowing inbound internet connectivity. Check within the VM for configuration issues, such as misconfiguration of the host OS firewall or the source configuration.
  
## **Recommended Documents**

- [Troubleshoot Azure VM connectivity problems](https://docs.microsoft.com/azure/virtual-network/troubleshoot-vm-connectivity)
- [Public IP addresses](https://docs.microsoft.com/azure/virtual-network/public-ip-addresses)
- [Troubleshoot virtual network peering issues](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-peering-issues)
- [Network virtual appliance issues in Azure](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)
- [Network security groups - Inbound](https://docs.microsoft.com/azure/virtual-network/network-security-groups-overview#inbound)
- [Virtual network traffic routing](https://docs.microsoft.com/azure/virtual-network/virtual-networks-udr-overview)
