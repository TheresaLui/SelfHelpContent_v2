<properties
	pageTitle="My application cannot start and its endpoint cannot be connected"
	description="My application cannot start and its endpoint cannot be connected"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-app-start"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# My application cannot start

The behavior can be that the endpoint cannot be connected, or it returns 502/503 after few retries.

Please export the logs to _Azure Log Analytics_. The table for Spring application logs is named `AppPlatformLogsforSpring`. For more information about Azure Spring Cloud diagnostics, please read [Tutorial: Enable Diagnostic Services on your Java Spring app](https://docs.microsoft.com/azure/spring-cloud/diagnostic-services).

If you see the following error in the beginning of your logs:

`org.springframework.context.ApplicationContextException: Unable to start web server`

Basically they can be in either of the two following reasons:

1. One of the beans or one of its dependencies is missing
2. One of the bean properties is missing or invalid. Likely you will see `java.lang.IllegalArgumentException` in this case.

Improperly enabled service bindings are another common cause of application start failures. To find these errors, use keywords related to the bound services to query the logs.

_Take MySql for example. The default timezone of a MySql instance is set to local system time. If you bind this MySql instance to your Spring application, it might not start due to the following error shown in the log:_

`java.sql.SQLException: The server time zone value 'Coordinated Universal Time' is unrecognized or represents more than one time zone.`

In this case, updating the `server parameters` of your MySql instance by changing `time_zone` from `SYSTEM` to `+0:00` fixes the problem.

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [Tutorial: Enable Diagnostic Services on your Java Spring app](https://docs.microsoft.com/azure/spring-cloud/diagnostic-services)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
