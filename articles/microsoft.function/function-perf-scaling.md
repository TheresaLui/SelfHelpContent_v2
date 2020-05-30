<properties
	pageTitle="Performance/Functions scaling issues"
	description="Performance/Functions scaling issues"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,shrahman"
    ms.author="shrahman,ykchen"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630474"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="4caa4f97-234f-4302-a13a-59c16da11dca"
	ownershipId="Compute_AppService"
/>

#  Performance/Functions scaling issues

## **Recommended Steps**

Azure Functions runs in two different modes: **Consumption plan** and **Azure App Service plan**. When you are using a Consumption plan, instances of the Azure Functions host are dynamically added and removed based on the number of incoming events. With an App Service plan, you can manually scale out by adding more VM instances or enabling autoscale. <br>

Scaling can vary based on a number of factors, and scale differently based on the trigger and language selected. However there are a few aspects of scaling that exist in the system today: <br>

* A single function app only scales up to a maximum of 200 instances. A single instance may process more than one message or request at a time though, so there is no set limit on the number of concurrent executions.
* New instances will only be allocated at most once every 10 seconds
* Event Hub related scaling limits

## **Recommended Documents**

* [Azure Functions scale and hosting](https://docs.microsoft.com/azure/azure-functions/functions-scale)<br>
* [Auto Scale in Azure](https://docs.microsoft.com/azure/azure-monitor/platform/autoscale-get-started)<br>
* [Event Hubs Trigger Scaling ](https://docs.microsoft.com/azure/azure-functions/functions-bindings-event-hubs#trigger---scaling)<br>
* [Azure Queue storage bindings for Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-bindings-storage-queue#host-json)
