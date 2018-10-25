<properties
    pageTitle="ER NAT Translation Count Exceeds The Safe Limit"
    description="ExpressRoute NAT Translation Count Exceeds The Safe Limit"
    infoBubbleText="ExpressRoute NAT Translation Count Exceeds The Safe Limit"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="pareshmu"
    displayOrder=""
    articleId="ExpressRouteNATTranslationCountIsTooHigh"
    selfHelpType="diagnostics"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />
# **ExpressRoute NAT Translation Count Is Too High**

'**<!--$Message--> [Message] <!--/$Message-->**'  </br>
ServiceKey: '**<!--$ServiceKey--> [ServiceKey] <!--/$ServiceKey-->**' </br>
MSEE: '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**' </br>
VRF Name: '**<!--$VRF--> [VRF] <!--/$VRF-->**'</br>


 
## **Recommended steps**

Utilize the **Run Show Command** Jarvis Actions operation to run: **'sh ip nat statistics'** on '**<!--$MSEE--> [MSEE] <!--/$MSEE-->**'  to obtain NAT counters.