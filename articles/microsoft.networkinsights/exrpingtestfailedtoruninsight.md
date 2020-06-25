<properties
    pageTitle="A Ping Test Failed To Execute"
    description="Pings From MSEE To Peer Failed"
    infoBubbleText="A Ping Test Failed To Execute.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    ms.author="jaredr80"
    displayOrder=""
    articleId="ExRPingTestFailedToRunInsight"
    diagnosticScenario="ExRPingTestFailedToRunInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# A Ping Test Failed to Execute

Border Gateway Protocol (BGP) is currently not up on one or more peerings on one or more devices, listed below. ICMP reachability is currently down from the MSEE to the customer. If ICMP or ping is not functioning from the MSEE, this is likely causing BGP to be down.

'**<!--$Message-->[Message]<!--/$Message-->**' <br>
ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'  <br>
MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
VRF Name: '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br>

## **Recommended Steps**

*  If a ping test fails, layer two is likely down or something in the path is blocking communication from MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' to the customer edge
* Check **DumpRoutingInfo** for **incommplete ARP entries**
* Consider asking the customer to involve their service provider if they do not control layer 2 connectivity to the MSEEs. Provider should check that s-tag is correct based on **DumpCircuitInfo** and the **ServiceProviderAPI**.

## **Recommended Document**

* [Verifying ExpressRoute connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview) <br>
