<properties
pageTitle="Where's my data?"
description="Where's my data?"
infoBubbleText="Some suggestions have been found to help solve your missing data issue quicker."
service="microsoft.insights"
resource="components"
authors="debugthings"
ms.author="jamdavi"
displayOrder=""
articleId="diagnostic-missing-ingestion-data-outofrange"
diagnosticScenario="ApplicationInsightsMissingDataDiagnostic"
selfHelpType="diagnostics"
supportTopicIds="32602225"
resourceTags=""
productPesIds="15693"
cloudEnvironments="public"
/>

# Where's my data?

## **Your application sent data that is out of the acceptable date range**
<!--issueDescription-->
Our diagnostic has detected that the Application Insights resource with name <!--$ComponentName-->[ComponentName]<!--/$ComponentName--> and instrumentation key <!--$InstrumentationKey-->[InstrumentationKey]<!--/$InstrumentationKey--> has sent data that is out of range <!--$Time-->[Time]<!--/$Time-->. This is an indication that your application was offline for a long period of time and sent data that was too old to be ingested. It can also mean that you are using an older version of the SDK that has issues when it loses connection to the internet.
<!--/issueDescription-->

## **Recommended Steps**

The most common reason for this is when your application goes offline for more than four hours and then reconnects to the internet. An example where this could happen is an application is hosted behind a firewall that unexpectedly does not allow connections to our ingestion endpoints. Our ingestion endpoints will not accept telemetry that is beyond this four hour window. This scenario is most common for non-web applications that do not send all telemetry on application exit. 

There are older versions of the .NET and Java SDK that can cause this behavior as well. These older versions might have received a bad response code from the ingestion endpoint and were unable to recover. For example in [.net versions prior to 2.10.0](https://github.com/Microsoft/ApplicationInsights-dotnet/issues/1049) and in [Java versions prior to 2.0.0](https://github.com/microsoft/ApplicationInsights-Java/pull/561).

**In all cases there is no way to recover this data as the endpoint does not save a copy of the bad data and the SDK might delete the cached copies before you can recover them.**

1. Verify you are using the latest version of your SDK
2. Verify the application in question was not offline for an extended period of time
3. If this is a custom application use the appropriate [InMemoryChannel](https://docs.microsoft.com/azure/azure-monitor/app/telemetry-channels)
4. If this is a mobile device you should ensure you're up to date in [AppCenter](https://docs.microsoft.com/appcenter/diagnostics/)
 

## **Recommended Documents**

* [Telemetry Channels](https://docs.microsoft.com/azure/azure-monitor/app/telemetry-channels)<br>
* [AppCenter](https://docs.microsoft.com/appcenter/diagnostics/)<br>
* [Application Insights Self Diagnostics Java](https://github.com/microsoft/ApplicationInsights-Java/wiki/ApplicationInsights.XML#sdklogger)
