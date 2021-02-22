<properties
    pageTitle="Express Route Circuit Private Peering is down"
    description="Express Route Circuit Private Peering is down"
    infoBubbleText="Need more information about this issue? See details on the right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="TobyTu"
    ms.author="pareshmu, mariliu"
    diagnosticScenario="ExpressRoutePublicPrivatePeeringDownInsight"
    displayOrder=""
    articleId="ExpressRoutePublicPrivatePeeringDownInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32627979, 32627985"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    ownershipId="CloudNet_AzureExpressRoute"
/>

# Express Route Circuit Private Peering is down
<!--issueDescription-->
ExpressRoute facilitates hybrid connectivity to Azure resources created privately inside an Azure virtual network and publicly via public IP addresses. Private peering enables connectivity to resources deployed within an Azure virtual network and Microsoft peering enables access to online Microsoft resources. 

We have identified that the **[affected circuit peering]** configured on your ExpressRoute circuit **[Azure resource name]** is currently down.
<!--/issueDescription-->

## **Recommended Steps**

Review the following Azure configuration and make sure on-premises network configuration is properly set up:

- ASN: The Autonomous System Number (ASN) is used to identify BGP-peered networks. Please make sure the ASN set in Azure **[private peering ASN]** matches the on-premises ASN.
- Primary subnet: The primary subnet is used to define the point-to-point (p2p) IP address for the BGP session over the primary physical link. Azure reserves the first usable address for the on-premises side of the BGP connection. The second usable address is applied to the Microsoft side of the session. Please confirm that the primary subnet **[primary subnet used to configure peering]** is correct.
- Secondary subnet: The primary subnet is used to define the point-to-point (p2p) IP address for the BGP session over the secondary physical link. Azure reserves the first usable address for the on-premises side of the BGP connection. The second usable address is applied to the Microsoft side of the session. Please confirm that the primary subnet **[secondary subnet used to configure peering]** is correct.
