<properties
    pageTitle="I am not getting debug snapshots"
    description="I am not getting debug snapshots"
    service="microsoft.insights"
    resource="components"
    authors="brahmnes"
    displayOrder="41"
    selfHelpType="resource"
    supportTopicIds="32602205"
    producePesIds="15693"
    cloudEnvironments="public"
 />
# I am not getting debug snapshots
## **Recommended steps**
To ensure that you are able to successfully get debug snapshots:

1. Verify that the [snapshot collector is properly configured](https://go.microsoft.com/fwlink/?linkid=848053#configure-snapshot-collection-for-aspnet-applications).
2. Ensure exceptions caught by the ASP.NET framework are being tracked. This requires an [implementation of error handlers](https://go.microsoft.com/fwlink/?linkid=867931#web-forms).
3. Ensure exceptions caught by application code are [reported with TrackException()](https://go.microsoft.com/fwlink/?linkid=867931#reporting-exceptions-explicitly).
4. Verify the latest version of [Microsoft.ApplicationInsights.SnapshotCollector nuget package](https://www.nuget.org/packages/Microsoft.ApplicationInsights.SnapshotCollector) is used.<br>

If debug snapshots are still not available, run through the steps outlined [here](https://go.microsoft.com/fwlink/?linkid=867932#is-the-snapshot-collector-working-properly).<br><br>
**Known issues**<br>
For an application running in Azure App Service, if it's using version 1.1.0 or earlier of Microsoft.ApplicationInsights.SnapshotCollector nuget package, and it either uses no Application Insights site extension or versions 2.4.7 or earlier, snapshots may not be collected. The remedy is to use version 1.1.1 or above of Microsoft.ApplicationInsights.SnapshotCollector nuget package, or use version 2.4.8 or above of the Application Insights site extension.
<br>
## **Recommended documents**
[Debug snapshots on exceptions in .NET apps](https://go.microsoft.com/fwlink/?linkid=848053)<br>
[Snapshot Debugger Troubleshooting Guide](https://go.microsoft.com/fwlink/?linkid=867932)<br>
[Diagnose exceptions in your web apps with Application Insights](https://go.microsoft.com/fwlink/?linkid=867931)
