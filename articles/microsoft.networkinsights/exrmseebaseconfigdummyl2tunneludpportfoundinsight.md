<properties
    pageTitle="VDummy L2 Tunnel UDP Port Found"
    description="Dummy L2 Tunnel UDP Port Found"
    infoBubbleText="Dummy L2 Tunnel UDP Port Found.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    ms.author="jaredr80"
    displayOrder=""
    articleId="ExRMseeBaseConfigDummyL2TunnelUdpPortFoundInsight"
    diagnosticScenario="ExRMseeBaseConfigDummyL2TunnelUdpPortFoundInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# Dummy L2 Tunnel UDP Port Found
<!--/issueDescription-->
A device-wide configuration used for communication between the MSEE and the Gateway Tenants (GWTs) is missing. This will cause communication to fail, including datapath and BGP.

* '**<!--$Message-->[Message]<!--/$Message-->**' <br>
* MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
<!--/issueDescription-->

## **Recommended Steps**

* Contact a Technical Administrator for approval for **Sev 2** ICM to **ExpressRoute Operations**, asking to update the **base configuration on MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**'**
* The ExpressRoute team scans for these issues, which are rare. When they occur, awareness is raised quickly (which requires using **Sev 2** for the ICM to **ExpressRoute Operations**).
