<properties
	pageTitle="Availability/Messaging function failed to trigger"
	description="Availability/Messaging function failed to trigger"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,cts-shrahman"
    ms.author="shrahman, jebrook"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630468"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="603b3799-55da-47d5-ae20-b6500a3cc7b1"
	ownershipId="Compute_AppService"
/>

#  Availability/Messaging function failed to trigger

## **Recommended Steps**

Message functions may fail to trigger for the following reasons:

1. The Function Runtime host is not starting up due to an exception. If Application Insights is enabled, here is an example query that can be used to help validate if the function host is failing to start. <br>

   ```
   traces
   | where message contains '"state": "Error"'
   ```

2. The Function invocation triggered, but failed to complete due to an exception during the invocation. Here is an example query to use in Application Insights:

   ```
   traces
   | where message contains "Exception while executing function"
   ```

	* [Monitoring Azure Functions with Application Insights](https://docs.microsoft.com/azure/azure-functions/functions-monitoring)<br>

3. Another Function App is pulling messages from the same queue. If two Azure Function Apps are triggered from the same queue, one Azure Function App may appear to be idle. <br>
4. The Function App is idle due to no HTTP requests from the scale controller in the Consumption Plan or Always On is not enabled in the Dedicated plan. <br>

	* [Always On with the Dedicated Plan](https://docs.microsoft.com/azure/azure-functions/functions-scale#always-on)<br>
	* [How the Consumption Plan Works](https://docs.microsoft.com/azure/azure-functions/functions-scale#how-the-consumption-plan-works)

