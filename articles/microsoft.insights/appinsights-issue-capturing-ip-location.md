<properties 
    pageTitle="Issue capturing IP address or location of the client"
    description="IP address collected by Application Insights are 0.0.0.0"
    service="microsoft.insights"
    resource=""
    authors="ramthi"
    ms.author="ramthi"
    selfHelpType="generic"
    articleId="appinsights-issue-capturing-ip-location"
    productPesIds="15693"
    supportTopicIds="32729604"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# IP addresses my app sends are all 0.0.0.0  


Application Insights now sets all octets of the IP address collected by client/server side SDKs to zero after looking up the City, Country and other geo location attributes. This strengthens privacy and is a change from prior processing that set only the last octet to zero. 

This change was made to address customer concerns with IP addresses given GDPR. 

Note: 

This does not affect data collected prior to February 5, 2018 

## **Recommended Steps**

IP address can be captured in a custom property if you wish, using the [Telemetry Initializers](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling#add-properties-itelemetryinitializer). 

## **Recommended Documents**

* [How Application Insights calculates city, country and other geolocation data.](https://docs.microsoft.com/azure/azure-monitor/faq#how-are-city-countryregion-and-other-geo-location-data-calculated)
* [How to add telemetry initializers to add custom properties or modify telemetry data.](https://docs.microsoft.com/azure/azure-monitor/app/api-filtering-sampling)
