<properties
	pageTitle="My application crashes or throws an unexpected error"
	description="My application crashes or throws an unexpected error"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-app-error"
	displayOrder="2"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# My application crashes or throws an unexpected error

Application crashes and errors happen because of various reasons. It's good to start by checking the running status and discovery status first. You can go to _App management_ to make sure all the applications are in _Running_ status and _UP_ discovery status.

If the status is _Running_ but the discovery status is not _UP_, please visit `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md#my-application-cannot-be-registered`.

If the discovery status is _UP_, you can go to _Metrics_ to check the application's health, especially the following metrics:

- `TomcatErrorCount` (_tomcat.global.error_):
  All Spring application exceptions will be counted here. If you see this number is large, please go to _Azure Log Analytics_ to inspect your application logs.

- `ServiceMemoryMax` (_jvm.memory.max_):
  The maximum amount of memory in bytes that can be used for memory management. It may be undefined or may change over time if defined. The amount of used and committed memory will always be less than or equal to max if it is defined. However, a memory allocation may fail with `OutOfMemoryError` if it attempts to increase the used memory such that used > committed even if used <= max would still be true. In such a situation, try to increase the maximum heap size via the `-Xmx` parameter.

- `ServiceMemoryUsed` (_jvm.memory.used_):
  The amount of memory in bytes that is currently used. For a normal load Java application, this metric series will form into a 'sawtooth' pattern, where the memory usage steadily increases and decreases in small increments and drops a lot suddenly and this pattern repeats. This is because of garbage collection inside Java virtual machine, where collection actions represent drops on the sawteeth. This metric is important for identify memory issues, such as 1) memory explosion at the very beginning, 2) surge memory allocation for a specific logic path, 3) gradual memory leaks.

  For more details, please visit `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/metrics.md`.

You need to enable [Log Analytics in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal). You will need to query the logs by using [Kusto Query Language](https://docs.microsoft.com/azure/kusto/query/).

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/README.md`
* Azure Spring Cloud Troubleshooting Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md`
* Azure Spring Cloud Metrics: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/metrics.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/faq.md`
