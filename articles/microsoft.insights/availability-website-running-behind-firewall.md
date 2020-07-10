<properties 
    pageTitle="I can't see availability of website running behind a firewall"
    description="I can't see availability of website running behind a firewall"
    infoBubbleText="Some suggestions have been found to help solve your availability test issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author = "casocha"
    articleId="availability-website-running-behind-firewall"
    displayOrder="8"
    selfHelpType="generic"
    cloudEnvironments="public, mooncake, blackforest, fairfax, usnat, ussec"
    productPesIds="15693"
    supportTopicIds="32729588"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# I can't see availability of website running behind a firewall

I have a website running behind a firewall or in Azure Government or Azure China. I want to configure a web test to ping my website but am unable to or I do not see availability results in the portal.

## **Recommended Steps**

I am able to configure my firewall:
* Ensure your firewall allows incoming requests from the IP addresses of our web test agents. Make sure you have whitelisted all of the [IP Address Used by Availability Tests](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#availability-tests).

I cannot configure my firewall or my website is in the government cloud:
* Write your own code to periodically test your internal server
* Run the code as a background process on a test server behind your firewall
* Your test process can send its results to Application Insights by using the [Track Availability](https://docs.microsoft.com/dotnet/api/microsoft.applicationinsights.telemetryclient.trackavailability?view=azure-dotnet) API in the core SDK package. This requires your test server to have outgoing access to the Application Insights ingestion endpoint, but that is a much smaller security risk than the alternative of permitting incoming requests.
* The results will appear in the availability web tests blades though the experience will be slightly simplified from what is available for tests created via the portal. Custom availability tests will also appear as availability results in Analytics, Search, and Metrics.

## **Recommended Documents**

* [Availability Tests](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-web-app-availability)
* [IP Address Used by Availability Tests](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#availability-tests)
