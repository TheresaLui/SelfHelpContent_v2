<properties
    pageTitle="ExpressRoute Public/Private peering is down"
    description="ExpressRoute Public/Private peering is down"
    infoBubbleText="ExpressRoute Public/Private peering is down"
    service="microsoft.network"
    resource="ExpressRoute"
    authors="pareshmu"
    ms.author="paresmhu"
    displayOrder=""
    articleId="ExpressRoutePublicPrivatePeeringInsight"
    selfHelpType="diagnostics"
    diagnosticScenario="ExpressRoutePublicPrivatePeeringInsight"
    supportTopicIds="32586802, 32586803, 32586804, 32586805, 32539949, 32539950, 32539954, 32539963"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# **Express Route Circuit Private or Public Peering is Down**
<!--/issueDescription-->
ExpressRoute circuit: '**<!--$ServiceKey--> [ServiceKey] <!--/$ServiceKey-->**'
<!--/issueDescription-->

## **Recommended Steps**

* Execute Jarvis Actions operation: **Brooklyn -> ExR Service Operations->Force Apply Device Configuration** for ServiceKey: **<!--$ServiceKey--> [ServiceKey] <!--/$ServiceKey-->**

## **Recommended Documents**

* [Create and modify peering for an ExpressRoute circuit](https://docs.microsoft.com/azure/expressroute/expressroute-howto-routing-portal-resource-manager)
* [Configure route filters for Microsoft peering](https://docs.microsoft.com/azure/expressroute/how-to-routefilter-portal)
