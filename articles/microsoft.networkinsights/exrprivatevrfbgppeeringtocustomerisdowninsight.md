<properties 
    pageTitle="Express Route BGP Peering To Customer Edge Is Down"
    description="Express Route BGP Peering To Customer Edge Is Down"
    infoBubbleText="Express Route BGP Peering To Customer Edge Is Down.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    displayOrder=""
    articleId="ExRPrivateVrfBgpPeeringToCustomerIsDownInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# Express Route BGP Peering To Customer Edge Is Down
ExpressRoute utilizes dual/redundant BGP sessions for each peering that the customer has configured (Private/Public/Microsoft peering). One or more BGP sessions are currently down right now, as shown below. <br><br>
'**<!--$Message-->[Message]<!--/$Message-->**' <br>
ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'  <br>
MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
VRF Name: '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br>
## **Recommended steps**
Check **Syslog** entries for MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' looking for issues while establishing a BGP peering to the customer edge.<br><br>
**Syslog Query Sample:**
cluster('Aznw').database('aznwmds').Syslog <br>
| where PreciseTimeStamp >= ago(12h)
and Device contains '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**'
and Message contains '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br>
| project PreciseTimeStamp, Device, EventName, Message, Severity <br>
| order by PreciseTimeStamp asc nulls last<br>
* Engage with the customer and their service provider to inspect BGP logging on the customer edge. <br>
* Check the peering configuration (i.e. - STag, CTag, Peer IPs, shared keys) and compare the settings with the peering configuration settings on the customer edge to ensure the required values match.
## **Recommended document**
[Verifying ExpressRoute connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview) <br>