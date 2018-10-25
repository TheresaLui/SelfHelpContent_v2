<properties 
    pageTitle="ExpressRoute BGP Peering To VNet Gateway Is Down"
    description="ExpressRoute BGP Peering To VNet Gateway Is Down"
    infoBubbleText="ExpressRoute BGP Peering To VNet Gateway Is Down.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    displayOrder=""
    articleId="ExRPrivateVrfBgpPeeringToGatewayIsDownInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# ExpressRoute BGP Peering To VNet Gateway Is Down
BGP is currently down between the MSEE private peering and the gateway that the customer has deployed in their VNet. <br><br>
'**<!--$Message-->[Message]<!--/$Message-->**' <br>
ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'  <br>
MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
VRF Name: '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br> 
## **Recommended steps**
+ Check the VNet Gateway in ASC for any health issues.
+ Check for User Defined Route (UDR) on the GatewaySubnet. This route if plumbed with blocking routes, may cause the control path between MSEE, GWM, and the Gateway Tenant (GWT) to fail. 
+ Utilize **Syslog** for MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' to check for an attempt to establish BGP peering to the peer for Private VRF: '**<!--$VRF-->[VRF]<!--/$VRF-->**'.
+ **Syslog Query Sample:** <br>
cluster('Aznw').database('aznwmds').Syslog <br>
| where PreciseTimeStamp >= ago(12h)
and Device contains '{MSEE}'
and Message contains '{VRF}' <br>
| project PreciseTimeStamp, Device, EventName, Message, Severity <br>
| order by PreciseTimeStamp asc nulls last<br>
## **Recommended document**
[Verifying ExpressRoute connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview) <br>