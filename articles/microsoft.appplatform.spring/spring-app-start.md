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
	cloudEnvironments="public"
/>

# My application cannot start and its endpoint cannot be connected

Please export the logs to _Azure Log Analytics_. The table for Spring application logs is named `AppPlatformLogsforSpring`. For more details, please visit `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/diagnostic-settings-guide.md`

Application start fails because of various reasons, but if you see the following error in the beginning of your logs: 

`org.springframework.context.ApplicationContextException: Unable to start web server`

Basically they can be in either of the two following reasons:

1. One of the beans or one of its dependencies is missing
2. One of the bean properties is missing or invalid. Likely you will see `java.lang.IllegalArgumentException` in this case.

Application start fails might be related with the enabled service bindings as well. Use keywords related to the bound services to query the logs.

_Take MySql for example. The default timezone of a MySql instance is set to local system time. If you bind this MySql instance to your Spring application, it might not start due to the following error shown in the log:_

`java.sql.SQLException: The server time zone value 'Coordinated Universal Time' is unrecognized or represents more than one time zone.`

All you need to do is to go to the `server parameters` of your MySql instance, and change `time_zone` from `SYSTEM` to `+0:00`.

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/README.md`
* Azure Spring Cloud Troubleshooting Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md`
* Analyze logs and metrics with Diagnostic settings: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/diagnostic-settings-guide.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/faq.md`
