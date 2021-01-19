<properties
pageTitle="Service Endpoint Policies detected on GatewaySubnet"
description="Service Endpoint Policies detected on GatewaySubnet"
infoBubbleText="Service Endpoint Policies detected on GatewaySubnet"
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="stegag"
ms.author="stegag"
displayOrder="10"
articleId="ServiceEndpointPolicy-on-GatewaySubnet"
diagnosticScenario="ServiceEndpointPolicy-on-GatewaySubnet"
selfHelpType="Diagnostics"
supportTopicIds="4427d63a-aeb1-8a8b-434c-f93de806bd3c,ce423144-c8f2-ba63-dcf5-76ae2658b584,c66265ed-a6a1-b155-34a4-6f7116757910,caf1656c-c7d0-6086-16ca-5801f401bb7e"
resourceTags="windows"
productPesIds="16094"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="CloudNet_AzureVPNGateway"
/>
# Service Endpoint Policies detected on GatewaySubnet

<!--issueDescription-->
Microsoft detected Service Endpoint Policies applied to the Gateway Subnet. When a Service Endpoint Policy is configured on the GatewaySubnet, it will cause availability issues for the Virtual Network Gateway Resource and potentially VPN service disruption. It is not supported to place a Service Endpoint Policy on the GatewaySubnet.
<!--/issueDescription-->

## **Recommended Steps**

Please disassociate the Service Endpoint Policies from the Gateway Subnet to restore VPN Gateway functionality.

## **Recommended Documents**

* [Virtual network service endpoint policies limitations](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview#limitations)
