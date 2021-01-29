<properties
    pageTitle="Packet drop is detected"
    description="Packet drop is detected"
    infoBubbleText="Need more information about that issue? See details on the right."
    service="microsoft.network"
    resource="vaults"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder=""
    articleId="VNGVirtualNetworkGateway"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="Public, fairfax, usnat, ussec"
    ownershipId="CloudNet_AzureVPNGateway"
/>

# Packet drop is detected
<!--issueDescription-->
Azure VPN gateway has detected packet drops.
<!--/issueDescription-->

## **Recommended Steps**

This issue occurs due to one of the following reasons:

- On-premises devices refused the Quick Mode (QM) or the devices has restrictions on supporting multiple QMs
- Traffic selectors don't match between Azure VPN gateway and on-premises device: ensure your IPsec configurations on the on-premises device is compatible with Azure VPN gateway
- A corresponding tunnel for the traffic may not be connected:
  - Ensure the connections are showing in Connected state. If the connections are not connected, try to troubleshoot the connections from Azure portal.
