<properties
    pageTitle="Express Route BGP Peering To Customer Edge Is Down"
    description="Express Route BGP Peering To Customer Edge Is Down"
    infoBubbleText="Express Route BGP Peering To Customer Edge Is Down.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    ms.author="jaredr80"
    displayOrder=""
    articleId="ExRPrivateVrfBgpPeeringToCustomerIsDownInsight"
    diagnosticScenario="ExRPrivateVrfBgpPeeringToCustomerIsDownInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>
# Express Route BGP Peering to Customer Edge is Down

ExpressRoute utilizes dual/redundant BGP sessions for each peering (Private, Public, or Microsoft) that the customer has configured. One or more BGP sessions are currently down right now, as shown below:

'**<!--$Message-->[Message]<!--/$Message-->**' <br>
ServiceKey: '**<!--$ServiceKey-->[ServiceKey]<!--/$ServiceKey-->**'  <br>
MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
VRF Name: '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br>

## **Recommended Steps**

* Check **Syslog** entries for MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' looking for issues while establishing a BGP peering to the customer edge:

**Syslog Query Sample:**
cluster('Aznw').database('aznwmds').Syslog <br>
| where PreciseTimeStamp >= ago(12h)
and Device contains '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**'
and Message contains '**<!--$VRF-->[VRF]<!--/$VRF-->**' <br>
| project PreciseTimeStamp, Device, EventName, Message, Severity <br>
| order by PreciseTimeStamp asc nulls last<br>

* Engage with the customer and their service provider to inspect BGP logging on the customer edge
* Check the peering configuration (i.e. - STag, CTag, Peer IPs, shared keys) and compare the settings with the peering configuration settings on the customer edge to ensure the required values match

## **Recommended Document**

* [Verifying ExpressRoute connectivity](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-expressroute-overview)
