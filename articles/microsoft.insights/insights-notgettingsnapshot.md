<properties
    pageTitle="I am not getting debug snapshots"
    description="I am not getting debug snapshots"
    service="microsoft.insights"
    resource="components"
    authors="brahmnes"
    displayOrder="41"
    selfHelpType="generic"
    supportTopicIds="32602205"
    producePesIds="15693"
    cloudEnvironments="public"
 />
# I am not getting debug snapshots

# What's the setup?

- Application running in Azure App Service 
  - Monitored with run-time Application Insights (Application Insights blade inside the App Service page).<br>
  See the "Monitoring at run-time (Application Insights extension)" section.
  - Monitored at build time (NuGet package).<br>
  See the Monitoring at build time (NuGet package)" section.


- .NET (Core or full framework) running in any other environment than Azure App Service.<br>
See the Monitoring at build time (NuGet package)" section.

- Application running on a non-Windows OS or non -.NET application.<br>    
    **Not supported**


## **Recommended steps**

## Monitoring at run-time (Application Insights extension)

1. Make sure Snapshot Collector is enabled by navigating to https://<app-service-name>.scm.azurewebsites.net/DiagnosticServices (replace <app-service-name> with your AppService name). 
    - If the page fails to load it means the App Service extension is not enabled. Follow the steps [here](https://docs.microsoft.com/azure/application-insights/app-insights-azure-web-apps) to enable Snapshot Debugger.
    - If the page contains a section "Attach Status for < framework type > application..." then the extension is properly enabled, so you might want to run through the steps outlined [here](https://docs.microsoft.com/azure/application-insights/app-insights-snapshot-debugger#troubleshooting).
2. The site extension currently supports only Windows applications that target .NET Framework or .NET Core.
3. The extension doesn't support self-contained .NET Core applications or .NET Core projects that target the full framework. If that's the case you must enable SnapshotCollector from [code](https://docs.microsoft.com/azure/application-insights/app-insights-snapshot-debugger#configure-snapshot-collection-for-aspnet-applications).


**Monitoring at build time (NuGet package)**<br>

To ensure that you are able to successfully get debug snapshots:<br>

1. Verify that the [snapshot collector is properly configured](https://go.microsoft.com/fwlink/?linkid=848053#configure-snapshot-collection-for-aspnet-applications).
2. Ensure exceptions caught by the ASP .NET framework are being tracked. This requires an [implementation of error handlers](https://go.microsoft.com/fwlink/?linkid=867931#web-forms).
3. Ensure exceptions caught by application code are [reported with TrackException()](https://go.microsoft.com/fwlink/?linkid=867931#reporting-exceptions-explicitly).
4. Verify the latest version of [Microsoft.ApplicationInsights.SnapshotCollector NuGet package](https://www.NuGet.org/packages/Microsoft.ApplicationInsights.SnapshotCollector) is used.<br>
5. If debug snapshots are still not available, run through the steps outlined [here](https://docs.microsoft.com/azure/application-insights/app-insights-snapshot-debugger#troubleshooting).

**Known issues**<br>
For an application running in Azure App Service, if it's using version 1.1.0 or earlier of Microsoft.ApplicationInsights.SnapshotCollector NuGet package, and it either uses no Application Insights site extension or versions 2.4.7 or earlier, snapshots may not be collected. The remedy is to use version 1.1.1 or above of Microsoft.ApplicationInsights.SnapshotCollector NuGet package, or use version 2.4.8 or above of the Application Insights site extension.<br>

## **Recommended documents**

[Debug snapshots on exceptions in .NET apps](https://go.microsoft.com/fwlink/?linkid=848053)<br>
[Snapshot Debugger Troubleshooting Guide](https://go.microsoft.com/fwlink/?linkid=867932)<br>
[Diagnose exceptions in your web apps with Application Insights](https://go.microsoft.com/fwlink/?linkid=867931)<br>
[Monitor Azure App Service](https://docs.microsoft.com/azure/application-insights/app-insights-azure-web-apps)

