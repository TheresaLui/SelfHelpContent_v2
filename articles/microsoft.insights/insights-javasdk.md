<properties 
    pageTitle="I am having problems with my Java SDK data"
    description="General troubleshooting guide for Java SDK."
    infoBubbleText="Some suggestions have been found to help solve your Java SDK issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="dhaval24"
    ms.author="dhdoshi"
    articleId="insights_javasdk"
    diagnosticScenario="ApplicationInsightsJavaSDK"
    displayOrder="6"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32402632, 32632984"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am having problems with my Java SDK data

## **Recommended Steps**

### Try Going Codeless

It is recommended to try a codeless approach (currently in public preview) instead of the SDK. It is super easy to enable and does not require any code instrumentation. Follow the instructions to enable the [Java agent](https://docs.microsoft.com/azure/azure-monitor/app/java-in-process-agent). 

### If you decide to stick with the SDK

The most common types of issues are related to the configuration of the SDK, or a network configuration issue such as a proxy or firewall. Here is a list of recommended items to review to ensure your application is configured correctly. Our [troubleshooting guide](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot) has a list of the most common concerts with problems using the Java SDK.

1. First, review the Java SDK [getting started guide](https://docs.microsoft.com/azure/application-insights/app-insights-java-get-started?toc=/azure/azure-monitor/toc.json) and check the default configuration
1. If you're configuration looks correct, enable the [SDK Logs](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot#debug-data-from-the-sdk) and search for errors prefixed with to `AI`
1. If you spot an exception or strange error ensure the java version you're using does not have any known issues by checking the [Java SDK Releases](https://github.com/Microsoft/ApplicationInsights-Java/releases) page
1. Most errors have been reported on GitHub and you can search the [Java SDK Issues](https://github.com/Microsoft/ApplicationInsights-Java/issues) for existing solutions
1. Lastly, review the [troubleshooting guide](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot) for other possible areas to troubleshoot

**Spring Boot Starter:** The [Spring Boot Starter](https://docs.microsoft.com/java/azure/spring-framework/configure-spring-boot-java-applicationinsights?view=azure-java-stable) for Application Insights that will help simplify the process of instrumenting your Spring Boot applications.

**Please provide following information to help the team investigate issue:**

1.	Describe the actual behavior
2.	Describe the expected behavior
3.	What SDK version are you using? 
4.	What kind of application it is: 

    * SpringBoot (Along with framework version) - > If yes -> Are they using ApplicationInsights SpringBoot Starter -> If yes which version of starter?
    * Traditional Spring MVC (With version)
    * J2EE (with version for servlet specifically)

5.	What version of Java SDK customer is using?
6.	Provide iKey and subscription ID and duration since issue started
7.	Provide [SDK Logs](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot#debug-data-from-the-sdk)

### Known Issues

* SDK versions prior to 2.0.0 have a bug where telemetry will not be persisted or sent if the machine loses connectivity

## **Recommended Documents**

* [Java auto-instrumentation](https://docs.microsoft.com/azure/azure-monitor/app/java-in-process-agent)
* [Getting Started](https://docs.microsoft.com/azure/application-insights/app-insights-java-quick-start?toc=/azure/azure-monitor/toc.json)<br>
* [Java SDK GitHub](https://github.com/Microsoft/ApplicationInsights-Java)<br>
* [Troubleshooting](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot?toc=/azure/azure-monitor/toc.json)
