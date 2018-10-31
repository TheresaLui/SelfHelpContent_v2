<properties 
    pageTitle="VDummy L2 Tunnel UDP Port Found"
    description="Dummy L2 Tunnel UDP Port Found"
    infoBubbleText="Dummy L2 Tunnel UDP Port Found.  See details on right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="jaredro"
    displayOrder=""
    articleId="ExRMseeBaseConfigDummyL2TunnelUdpPortFoundInsight"
    diagnosticScenario="ExRMseeBaseConfigDummyL2TunnelUdpPortFoundInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# Dummy L2 Tunnel UDP Port Found
A device-wide configuration is missing that is used for communication between the MSEE and the Gateway Tenants (GWTs). This will cause communication to fail, including datapath and BGP.<br><br>
'**<!--$Message-->[Message]<!--/$Message-->**' <br>
MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**' <br>
## **Recommended steps**
+ Contact a TA for approval for **Sev 2** ICM to **ExpressRoute Operations** asking to update the **base configuration on MSEE: '**<!--$MSEE-->[MSEE]<!--/$MSEE-->**'**. 
 + The ExpressRoute team scans for these issues, so they should be rare. 
 + When they occur, we need to raise awareness quickly, which is why we are using **Sev 2** for the ICM to **ExpressRoute Operations**.

