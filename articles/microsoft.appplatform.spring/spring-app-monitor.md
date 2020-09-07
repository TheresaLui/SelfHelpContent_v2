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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="DevDivAzServices_SpringCloud"
/>

# I cannot find metrics or logs for my application

Go to _App management_ to ensure the application is in _Running_ status and _UP_ discovery status.

If you can see metrics from _JVM_ but no metrics from _Tomcat_, please ensure that the `spring-boot-actuator` dependency is enabled in your application package and boots successfully.

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

If your application logs can be archived to a storage account, but not sent to _Azure Log Analytics_, please check whether you [set up your workspace correctly](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace). If you are using a free tier of _Azure Log Analytics_, please be aware that [the free tier does not provide an SLA](https://azure.microsoft.com/support/legal/sla/log-analytics/v1_3/).

## **Recommended Documents**

* [Quickstart: Launch a Java Spring app on Azure using the Azure portal](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-quickstart-launch-app-portal)
* [FAQ for Azure Spring Cloud](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-faq)
* [Troubleshooting guidance](https://docs.microsoft.com/azure/spring-cloud/spring-cloud-troubleshoot)
