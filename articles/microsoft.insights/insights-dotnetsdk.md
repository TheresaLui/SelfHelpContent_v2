<properties 
    pageTitle="I am having problems with my .NET SDK"
    description="General troubleshooting guide for .NET SDK."
    infoBubbleText="Some suggestions have been found to help solve your .NET SDK issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_dotnetsdk"
    diagnosticScenario="ApplicationInsightsDotNetSDK"
    displayOrder="6"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32402631, 32632986, 32632987"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am having problems with my .NET SDK

## **Recommended Steps**

1. First, review the .NET SDK [getting started guide](https://docs.microsoft.com/azure/azure-monitor/app/asp-net) and check the default configuration
2. If you're using .NET Core, review the .NET Core SDK [getting started guide](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core) and check the default configuration
3. If you're configuration looks correct, enable the [SDK Logs](http://sergeysharp.com/blog/2015/04/16/diagnostic-of-applicationinsights-sdk/) and search for errors
4. If you spot an exception or strange error ensure the SDK version you're using does not have any known issues by checking the [.NET SDK Releases](https://github.com/Microsoft/ApplicationInsights-dotnet/releases) page
5. Most errors have been reported on GitHub and you can search the [.NET SDK Issues](https://github.com/Microsoft/ApplicationInsights-dotnet/issues) for existing solutions
6. Lastly, review the [troubleshooting guide](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data) for other possible areas to troubleshoot

**App Service Integration Change:** We recently changed the way we integrate with App Services. You no longer need to have the extension installed (in the Extensions blade). You should remove the Application Insights extension from the App Service extension blade and use the [new experience](https://docs.microsoft.com/azure/azure-monitor/app/azure-web-apps?toc=%2Fazure%2Fazure-monitor%2Ftoc.json) to enable this.

## **Recommended Documents**

* [Getting Started .NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net)<br>
* [Getting Started .NET Core](https://github.com/Microsoft/ApplicationInsights-aspnetcore)<br>
* [.NET SDK GitHub](https://github.com/Microsoft/ApplicationInsights-dotnet)<br>
* [.NET Core SDK GitHub](https://github.com/Microsoft/ApplicationInsights-dotnet)<br>
* [Troubleshooting](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data)
