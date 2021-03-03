<properties
	pageTitle="Monitor Azure Functions"
	description="Monitor Azure Functions"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,shrahman"
    ms.author="shrahman, shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32598332"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	articleId="505bf069-145a-4530-9f9c-eb3dc71f272e"
	ownershipId="Compute_AppService"
/>

# Monitor Azure Functions

## **Recommended Steps**

Azure Functions Monitoring is driven by Application Insights. The users may notice that they cannot see any logs for their Functions Invocations or that the data appears to be inaccurate. Here are some resources that can help diagnose these issues:

* The Diagnose and Solve blade for Azure Functions will check the configuration and advise on the following: 

	* If the Application Insights Instrumentation key and\or Connection String are configured correctly
	* If the AzureWebJobsDashboard built in logging is enabled
	* If sampling is enabled for the Azure Functions telemetry

Here are some links that show how to check these items outside of the Azure Portal:

* [Knowing whether sampling is in operation](https://docs.microsoft.com/azure/azure-monitor/app/sampling#knowing-whether-sampling-is-in-operation)
* [Disable built-in logging](https://docs.microsoft.com/azure/azure-functions/functions-monitoring?tabs=cmd#disable-built-in-logging)
* Reference for Application Insights Application Settings:

  * [Instrumentation Key](https://docs.microsoft.com/azure/azure-functions/functions-app-settings#appinsights_instrumentationkey)
  * [Connection String](https://docs.microsoft.com/azure/azure-functions/functions-app-settings#applicationinsights_connection_string)

You may use Dependency Injection or add custom logging. It is important that you follow the guidance at the links below to avoid overwriting the default configuration:

* [Logging services](https://docs.microsoft.com/azure/azure-functions/functions-dotnet-dependency-injection#logging-services)
* [Log custom telemetry in C# functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring?tabs=cmd#log-custom-telemetry-in-c-functions)
* [Log custom telemetry in JavaScript functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring?tabs=cmd#log-custom-telemetry-in-javascript-functions)
