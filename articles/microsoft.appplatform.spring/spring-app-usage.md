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
	cloudEnvironments="public"
/>

# My application experiences high CPU usage or high memory usage

If your application experiences high CPU/memory usage, it is basically in either of two situations:

1. All the app instances experience high CPU/memory usage, and
2. Some of the app instances experience high CPU/memory usage

To confirm which situation it is:

1. Go to _Metrics_, select either `Service CPU Usage Percentage` or `Service Memory Used`,
2. Add an `App=` filter to specify which application you want to monitor, and
3. Split the metrics by `Instance`

If the situation happens to be that all instances are experiencing high CPU/memory, you need to either scale out the application or scale up the CPU/Memory. For more details, please visit `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/how-to.md#scale-out-an-application-to-multiple-instances`

If the situation happens to be that some of the instances are experiencing high CPU/memory, please check the instance status and its discovery status.

If all instances are up and running, please go to _Azure Log Analytics_ to query your application logs and review your code logics to see if any of them might impact scale partitioning. For more details, please visit `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/diagnostic-settings-guide.md`.

You need to enable [Log Analytics in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal). You will need to query the logs by using [Kusto Query Language](https://docs.microsoft.com/azure/kusto/query/).

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/README.md`
* Azure Spring Cloud Troubleshooting Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md`
* Azure Spring Cloud How-Tos: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/how-to.md`
* Azure Spring Cloud Diagnostic Settings: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/diagnostic-settings-guide.md`
* Azure Spring Cloud Metrics: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/metrics.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/faq.md`
