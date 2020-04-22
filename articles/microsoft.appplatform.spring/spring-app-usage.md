<properties
	pageTitle="My application experiences high CPU usage or high memory usage"
	description="My application experiences high CPU usage or high memory usage"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-app-usage"
	displayOrder="3"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# My application experiences high CPU usage or high memory usage

If your application experiences high CPU/memory usage, it is basically in either of two situations:

1. All the app instances experience high CPU/memory usage, and
2. Some of the app instances experience high CPU/memory usage

To determine which situation is true for your application:

1. Go to _Metrics_, select either `Service CPU Usage Percentage` or `Service Memory Used`,
2. Add an `App=` filter to specify the application you want to monitor, and
3. Split the metrics by `Instance`

If all instances are experiencing high CPU/memory usage, either scale out the application or scale up the CPU/Memory.

If only some instances are experiencing high CPU/memory usage, check the instance status and its discovery status.

If all instances are up and running, please go to _Azure Log Analytics_ to query your application logs and review your code to see if any of them might impact scale partitioning. For more information about Azure Spring Cloud diagnostics, please read [Tutorial: Enable Diagnostic Services on your Java Spring app](https://docs.microsoft.com/azure/spring-cloud/diagnostic-services).

You need to enable [Log Analytics in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal). You will need to query the logs by using [Kusto Query Language](https://docs.microsoft.com/azure/kusto/query/).

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
* [Tutorial: Enable Diagnostic Services on your Java Spring app](https://docs.microsoft.com/azure/spring-cloud/diagnostic-services)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
