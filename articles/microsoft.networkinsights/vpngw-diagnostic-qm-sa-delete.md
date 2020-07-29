<properties
    pageTitle="IKE Phase2 (Quick Mode) SAs are deleted"
    description="IKE Phase2 (Quick Mode) SAs are deleted"
    infoBubbleText="Need more information about that issue? See details on the right."
    service="microsoft.network"
    resource="vaults"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder=""
    articleId="VPNGwQMSAsdeleted"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16094"
    cloudEnvironments="Public, fairfax, usnat, ussec"
    ownershipId="CloudNet_AzureVPNGateway"
/>

# IKE Phase2 (Quick Mode) SAs are deleted
<!--issueDescription-->
All IPsec Security Associations (IKE Quick Mode SAs) are deleted. Connections may remain in Connected state, but traffic may not flow or connections may be going down.
<!--/issueDescription-->

## **Recommended steps**

Start the traffic and check if a new Quick Mode Security Association (QM SA) has been established. You can also try to reconnect the IKE tunnel after disconnecting it.
