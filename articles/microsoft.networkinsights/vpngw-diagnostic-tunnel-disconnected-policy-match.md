<properties
    pageTitle="Tunnel disconnected because of policy match error"
    description="Tunnel disconnected because of policy match error"
    infoBubbleText="Need more information about this issue? See details on the right."
    service="microsoft.network"
    resource="vaults"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder=""
    articleId="VPNGwTunnelDisconnectPolicyMatchMMSA"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="Public, fairfax, usnat, ussec"
    ownershipId="CloudNet_AzureVPNGateway"
/>

# Tunnel disconnected because of policy match error
<!--issueDescription-->
The tunnel connection could not establish because of a "Policy match error" during main mode security association.
<!--/issueDescription-->

## **Recommended Steps**

Tunnel connectivity issues are due to IKE policy mismatch between Azure VPN Gateway and on-premises gateway

You can set IPsec custom policy on Azure VPN Gateway by using Azure PS commands ([New-AzIpsecPolicy](https://docs.microsoft.com/powershell/module/az.network/new-azipsecpolicy?view=azps-3.5.0) to create specific policy and [Set-AzVirtualNetworkGatewayConnection](https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnection?view=azps-3.5.0) to set that policy on particular connection or tunnel). Azure VPN Gateway default policy covers many combinations, so if your policy is part of the default policy set, you do not need to set custom policy on Azure Gateways.  See [here](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-ipsecikepolicy-rm-powershell) for additional information.
Alternatively, you can change the policy of the on-premises to match with Azure configuration.
