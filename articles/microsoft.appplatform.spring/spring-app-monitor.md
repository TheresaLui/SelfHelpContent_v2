<properties
	pageTitle="I cannot find metrics or logs for my application"
	description="I cannot find metrics or logs for my application"
	infoBubbleText=""
	service="microsoft.appplatform"
	resource="spring"
	authors="enihcam"
	ms.author="ericwan"
	articleId="spring-app-monitor"
	displayOrder="8"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I cannot find metrics or logs for my application

First of all, go to _App management_ to make sure the application is in _Running_ status and _UP_ discovery status.

If you can see metrics from _JVM_ but no metrics from _Tomcat_, please check if `spring-boot-actuator` dependency is enabled in your application package and successfully boot up.

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

If your application logs can be archived to a storage account, but not sent to _Azure Log Analytics_, please check whether you [set up your workspace correctly](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace). If you are using a free tier of _Azure Log Analytics_, please be aware that [the free tier does not provide SLA](https://azure.microsoft.com/support/legal/sla/log-analytics/v1_3/).

## **Recommended Documents**

* Azure Spring Cloud Getting Started Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/README.md`
* Azure Spring Cloud Troubleshooting Guide: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/troubleshooting.md`
* Azure Spring Cloud FAQ: `https://github.com/Azure/azure-spring-cloud-docs-pr/blob/master/docs/faq.md`
