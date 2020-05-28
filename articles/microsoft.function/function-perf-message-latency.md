<properties
	pageTitle="Performance/Message Functions processing latency"
	description="Performance/Message Functions processing latency"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,shrahman"
    ms.author="shrahman,ykchen"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630476"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="4ba3ebd9-5c93-4ead-af8e-457a229c1c50"
	ownershipId="Compute_AppService"
/>

#  Performance/Message Functions processing latency

## **Recommended Steps**

Azure Functions performance issues are commonly related to: <br>

* High CPU or High Memory Consumption<br>
* Port/Outbound Socket Consumption<br>
* Number of threads being spawned<br>
* Number of pending requests in the HTTP Pipeline<br>
* Downstream service interacting with Azure Functions has slow response issue<br>
* Cold start on newly added instance<br> 
* Unhandled exception in Azure Functions code<br>

We can follow the steps below to narrow down root cause:<br>

* Check if the Azure Functions slow response issue could be reproduced locally before publishing to Azure. If yes, add Time StopWatch function call to measure elapsed time in Azure Functions. It can be used to keep track of average request time, to send messages to the user based on how long an action might take, or to benchmark your code. 
* Check if any exception is being thrown while the slow response issue occurred. If yes, catch and handle them properly.
* Access the downstream service interacting with Azure Functions directly and see if response time is abnormal
* Enable Application Insight to trace the callstack while the slow response issue occurs

## **Recommended Documents**

* [What Happens when I Write a Function](https://blogs.msdn.microsoft.com/appserviceteam/2018/02/07/understanding-serverless-cold-start/)<br>
* [Azure Functions Apps: Performance Considerations](https://blogs.msdn.microsoft.com/amitagarwal/2018/04/03/azure-function-apps-performance-considerations/)
