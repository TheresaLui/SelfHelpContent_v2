<properties
    pageTitle="Customer Prefixes Missing From VNet Gateway Adjacency Table"
    description="Customer Prefixes Missing From VNet Gateway Adjacency Table"
    infoBubbleText="Customer Prefixes Missing From VNet Gateway Adjacency Table"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="pareshmu"
    displayOrder=""
    articleId="ExRPrivateVrfCustomerPrefixesInGatewayAdjacencyTableInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
## **Customer Prefixes Missing From VNet Gateway Adjacency Table**


**ServiceKey:** '**<!--$ServiceKey--> [ServiceKey] <!--/$ServiceKey-->**' 

**MSEE:** '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**' 

**VRF Name:** '**<!--$VRF--> [VRF] <!--/$VRF-->**' 

**VnetID:** '**<!--$VNetId--> [VNetId] <!--/$VNetId-->**' 


## **Recommended steps**

+ Ensure BGP peering is up between customer edge and MSEEs and also between MSEEs and VNet Gateway.
+ If all peerings are up, investigate route filtering on the MSEEs and the VNet Gateway and check if customer routes are dropped on MSEE due to ASN issues or some other reason.
+ Consider a VNet Gateway reset using Jarvis Actions.
+ **Note:** Set customer expectations that downtime is expected during a Gateway Reset operation.

## **Recommended Documentation**
[Verify ExpressRoute Connectivity](https://docs.microsoft.com/en-us/azure/expressroute/expressroute-troubleshooting-expressroute-overview)
