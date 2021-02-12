<properties 
    pageTitle="Is there a service outage?"
    description="Is there a service outage?"
    service="microsoft.insights"
    resource="components"
    articleId="insights-serviceoutage"
    authors="debugthings"
    ms.author="jamdavi"
    displayOrder="1014"
    selfHelpType="generic"
    productPesIds="15693"
    supportTopicIds="32402638"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# Is there a service outage?

## **Recommended Steps**

A service outage can manifest itself in two ways. The first way is data in the portal is not displayed; this will be accompanied by an error message such as "Error retrieving data". The second type of outage is for data ingestion and possible latency. In most cases our team will be notified of a large drop in traffic or ingestion latency and will start investigating right away. You can validate the two types of errors, portal outage and data collection using the steps below.

**Investigate Azure Portal Outage Checklist**<br>

* Check the [Azure Monitor Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog) and [Azure Status Blog](https://status.azure.com/status) pages for outages
* Does the screen show an error message?
    - if not this is likely an issue with **data collection**

* Is it the Metrics Explorer blade?
    - if no, you should should try to run a query in Log Analytics
    - if yes, you should should verify other resources are also experiencing an issue and open a case using the **Metrics** service

* Open your browsers developer console by hitting F12 and look for any errors to **api##.applicationisights.io** in the Network tab
    - if you see 404, 500, 502, 503 these are indications of a **service outage**
    - if you see other error codes there may be a proxy blocking the connection

**Investigate Data Collection Checklist**<br>

* Check the [Azure Monitor Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog) and [Azure Status Blog](https://status.azure.com/status) pages for outages
* Follow the [no data guide](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-troubleshoot-no-data) to ensure your configuration is correct
* Navigate to https://dc.services.visualstudio.com/v2/track/ in a browser
    - it should show "Method Not Allowed" or a 405 error code (this is expected)

## **Recommended Documents**

* [Azure Monitor Service Blog](https://techcommunity.microsoft.com/t5/Azure-Monitor-Status/bg-p/AzureMonitorStatusBlog)<br>
* [Azure Status Blog](https://status.azure.com/status)<br>
