<properties
    pageTitle="Microsoft Public Prefixes Are Not Advertised From the MSEE to the Customer Edge"
    description="Microsoft Public Prefixes Are Not Advertised From the MSEE To the Customer Edge"
    infoBubbleText="Microsoft Public Prefixes Are Not Advertised From The MSEE To the Customer Edge"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="pareshmu"
    ms.author="pareshmu"
    diagnosticScenario="ExRPublicPeeringMicrosoftPrefixesNotAdvertisedInsight"
    displayOrder=""
    articleId="ExRPublicPeeringMicrosoftPrefixesNotAdvertisedInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# **Microsoft Public Prefixes are Not Advertised from the MSEE to the Customer Edge**
<!--/issueDescription-->

* **Message:** '**<!--$Message--> [Message] <!--/$Message-->**'
* **ServiceKey:** '**<!--$ServiceKey--> [ServiceKey] <!--/$ServiceKey-->**'
* **MSEE:** '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**'
* **VRF Name:** '**<!--$VRF--> [VRF] <!--/$VRF-->**'
<!--/issueDescription-->

## **Recommended Steps**

+ **MSEE:** '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**' is not configured to advertise Public peering prefixes to the customer
+ Check the health of the Public peering between both the MSEEs and the customer edge
+ Check to ensure the customer has configured appropriate route filters in Azure to allow the desired Public peering prefixes to flow to the customer edge

## **Recommended Documents**

* [ExpressRoute circuits and peering](https://docs.microsoft.com/azure/expressroute/expressroute-circuit-peerings)
