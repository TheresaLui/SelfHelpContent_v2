<properties
    pageTitle="A Connectivity Check Between MSEE and Gateway Manager (GWM) Failed"
    description="A Connectivity Check Between MSEE and Gateway Manager (GWM) Failed"
    infoBubbleText="A Connectivity Check Failed. See details on the right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    ms.author="krisney"
    displayOrder=""
    articleId="ExRGwmConnectivityIndividualReachabilityStatusInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32539944, 32539947"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	ownershipId="CloudNet_AzureExpressRoute"
/>

# Microsoft Azure has identified an issue regarding the MSEE (Microsoft Enterprise Edge router)
<!--/issueDescription-->
An MSEE is the Microsoft Datacenter side of the network connection, which connects to the Gateway Manager.  A connectivity check between the MSEE and the Gateway Manager has failed, which results in a lack of network connectivity.
<!--/issueDescription-->

## **Recommended Steps**

We are actively working to resolve the issue. You can receive updates by subscribing to [Service Health Alerts](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-activity-log-alerts-on-service-notifications?toc=%2fazure%2fservice-health%2ftoc.json), or view your peering status from the portal: <br>

1. On the left pane choose All Services <br>
2. In the middle choose ExpressRoute circuits <br>
3. Once the circuit is selected, you can check your Peerings on the bottom left
