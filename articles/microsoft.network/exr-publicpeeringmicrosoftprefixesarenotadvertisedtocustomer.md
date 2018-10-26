<properties
    pageTitle="Microsoft Public Prefixes Are Not Advertised From the MSEE to the Customer Edge"
    description="Microsoft Public Prefixes Are Not Advertised From the MSEE To the Customer Edge"
    infoBubbleText="Microsoft Public Prefixes Are Not Advertised From The MSEE To the Customer Edge"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="pareshmu"
    displayOrder=""
    articleId="ExRPublicPeeringMicrosoftPrefixesNotAdvertisedInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# **Microsoft Public Prefixes Are Not Advertised From the MSEE to the Customer Edge**

**Message:** '**<!--$Message--> [Message] <!--/$Message-->**'
**ServiceKey:** '**<!--$ServiceKey--> [ServiceKey] <!--/$ServiceKey-->**'
**MSEE:** '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**'
**VRF Name:** '**<!--$VRF--> [VRF] <!--/$VRF-->**'

## **Recommended steps**

+ **MSEE:** '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**' is not configured to advertise Public peering prefixes to the customer.
+ First, check the health of the Public peering between both the MSEEs and the customer edge.
+ Finally, check to ensure the customer has configured appropriate route filters in Azure to allow the desired Public peering prefixes to flow to the customer edge.