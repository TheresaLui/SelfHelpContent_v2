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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# My application crashes or throws an unexpected error

Before diagnosing the cause of an application crash or error, check the running status and discovery status. Go to _App management_ to make sure all the applications are in _Running_ status and _UP_ discovery status.

If the status is _Running_ but the discovery status is not _UP_, please go to another diagnostic blade, _My application cannot be registered_.

If the discovery status is _UP_, you can go to _Metrics_ to check the application's health. The following metrics are helpful:

- `TomcatErrorCount` (_tomcat.global.error_):
  All Spring application exceptions will be counted here. If this number is larger than expected, please go to _Azure Log Analytics_ to inspect your application logs.

- `AppMemoryMax` (_jvm.memory.max_):
  The maximum amount of memory, in bytes, that can be used for memory management. It may be undefined or may change over time. If defined, the amount of used and committed memory will always be less than or equal to `AppMemoryMax`. However, a memory allocation may fail with `OutOfMemoryError` if it attempts to increase the used memory beyond the committed value. This is true even if the used value is smaller than `AppMemoryMax`. In this case, increase the maximum heap size via the `-Xmx` parameter.

- `AppMemoryUsed` (_jvm.memory.used_):
  The amount of memory in bytes that is currently used. For a normal load Java application, this metric series will form a repeating 'sawtooth' pattern, where the memory usage steadily increases and decreases in small increments with occasional large drops. These drops represent garbage collection actions inside the Java virtual machine. This metric helps identify memory issues, such as 1) memory explosion at the very beginning, 2) surge memory allocation for a specific logic path, 3) gradual memory leaks.

You need to enable [Log Analytics in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal). You can query the logs using [Kusto Query Language](https://docs.microsoft.com/azure/kusto/query/).

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
