<properties
    pageTitle="The NAT IP Address Is Not In The Expected NAT IP Address Range"
    description="The NAT IP Address Is Not In The Expected NAT IP Address Range"
    infoBubbleText="The NAT IP Address Is Not In The Expected NAT IP Address Range.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    ms.author="jaredr80"
    displayOrder=""
    articleId="ExRMseeCircuitConfigNatIpNotInRangeInsight"
    diagnosticScenario="ExRMseeCircuitConfigNatIpNotInRangeInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# The NAT IP Address is not in the Expected NAT IP Address Range
<!--/issueDescription-->
Public peering on ExpressRoute uses the NAT to translate private IP space into public IP space. ExpressRoute by default allocates a single unique public IP address on each MSEE device, which corresponds with the public peering configuration that the customer has configured.

**Note**: Private and Microsoft peering do not apply to this insight.

* '**<!--$Message-->[Message]<!--/$Message-->**' <br>
* ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'  <br>
* MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
* VRF Name: '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br>
<!--/issueDescription-->

## **Recommended Steps**

The NAT IP addresses are allocated dynamically at the time of public peering creation and do not change during the lifecycle of the public peering on the circuit. At times, the device configuration may differ than the state in Gateway Manager (GWM).

1. Execute **Jarvis Actions** operation: **Brooklyn->ExR Service Operations->Force Apply Device Configuration** for ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'

## **Recommended Document**

* [ExpressRoute NAT requirements](https://docs.microsoft.com/azure/expressroute/expressroute-nat#nat-requirements-for-azure-public-peering) <br>
