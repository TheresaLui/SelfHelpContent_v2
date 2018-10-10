<properties 
    pageTitle="I am having problems with my Java SDK data"
    description="General troubleshooting guide for Java SDK."
    infoBubbleText="Some suggestions have been found to help solve your Java SDK issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    articleId="insights_javasdk"
    diagnosticScenario="ApplicationInsightsJavaSDK"
    displayOrder="6"
    selfHelpType="generic"
    cloudEnvironments="public"
    productPesIds="15693" 
    supportTopicIds="32402632"
 />
# I am having problems with my Java SDK data

## **Recommended steps**

1. Review the Java SDK [troubleshooting guide](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot)
  * Specifically the [No Data](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot#no-data) guide
2. Enable the [SDK Logs](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot#debug-data-from-the-sdk) for errors
3. Search the [Java SDK Issues](https://github.com/Microsoft/ApplicationInsights-Java/issues)
4. Check the [Java SDK Releases](https://github.com/Microsoft/ApplicationInsights-Java/releases) page for a comprehensive list of known issues


**Please provide following information to help the team investigate issue**

1.	Describe the actual behavior.
2.	Describe the expected behavior.
3.	What SDK version are you using? 
4.	What kind of application it is: 
  *	SpringBoot (Along with framework version) - > If yes -> Are they using ApplicationInsights SpringBoot Starter -> If yes which version of starter?
  *	Traditional Spring MVC (With version)
  *	J2EE (with version for servlet specifically)
5.	What version of Java SDK customer is using?
6.	Provide iKey and subscription ID and duration since issue started
7.	Provide SDK logs

**Known issues**

1.	SDK versions prior to 2.0.0 have a bug where telemetry will not be persisted or sent if the machine looses connectivity

## **Recommended Documents**
[Getting Started](https://docs.microsoft.com/azure/application-insights/app-insights-java-quick-start?toc=/azure/azure-monitor/toc.json)<br/>
[Java SDK GitHub](https://github.com/Microsoft/ApplicationInsights-Java)<br/>
[Troubleshooting](https://docs.microsoft.com/azure/application-insights/app-insights-java-troubleshoot?toc=/azure/azure-monitor/toc.json)<br/>
