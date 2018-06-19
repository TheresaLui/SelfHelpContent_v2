<properties
    pageTitle="A Connectivity Check Between MSEE and Gateway Manager (GWM) Failed"
    description="A Connectivity Check Between MSEE and Gateway Manager (GWM) Failed"
    infoBubbleText="A Connectivity Check Failed. See details on the right."
    service="microsoft.network"
    resource="ExpressRoute"
    authors="KristinaNeyens"
    displayOrder=""
    articleId="ExRConnChkBtwnMSEEGWMFaileddiag"
    selfHelpType="diagnostics"
    supportTopicIds="32539944, 32539947"
    resourceTags="windows"
    productPesIds="15480"
    cloudEnvironments="public"
 />

# Microsoft Azure has identified an issue regarding the MSEE (Microsoft Enterprise Edge router)
An MSEE is the Microsoft Datacenter side of the network connection, which connects to the Gateway Manager.  A connectivity check between the MSEE and the Gateway Manager has failed, which results in a lack of network connectivity.

## **Recommended steps**


We are actively working to resolve the issue and you can receive updates by subscribing to Service Health Alerts using [service health alerts documentation](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-activity-log-alerts-on-service-notifications?toc=%2fazure%2fservice-health%2ftoc.json), or view your peering status from the portal following below steps: <br>

1. On the left pane choose All Services <br>
2. In the middle choose Express Route circuits <br>
3. Once the circuit is selected, you can check your Peerings on the bottom left
