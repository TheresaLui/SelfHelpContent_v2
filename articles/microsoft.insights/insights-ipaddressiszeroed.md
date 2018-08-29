<properties 
    pageTitle="IP addresses my app sends are all 0.0.0.0"
    description="IP addresses my app sends are all 0.0.0.0"
    service="microsoft.insights"
    resource="components"
    authors="mcosner"
    displayOrder="15"
    selfHelpType="resource"
    productPesIds="15693"
    supportTopicIds=""
    cloudEnvironments="public"
 />
# IP addresses my app sends are all 0.0.0.0
## **Recommended steps**
Application Insights now sets all octets of the IP address collected by client/server side SDKs to zero after looking up the City, Country and other geo location attributes. This strengthens privacy and is a change from prior processing that set only the last octet to zero.<br><br>
This change was made to address customer concerns with IP addresses given GDPR.<br><br>
**Notes:**

  * If you need to collect the IP address, you can use telemetry initializer to add a custom property.
  * This does not affect data collected prior to February 5, 2018.

## **Recommended documents**
[Azure Application Insights service blog](https://blogs.msdn.microsoft.com/applicationinsights-status/2018/02/01/all-octets-of-ip-address-will-be-set-to-zero/)<br>
[How Application Insights calculates city, country and other geolocation data](https://docs.microsoft.com/azure/application-insights/app-insights-troubleshoot-faq#how-are-city-country-and-other-geo-location-data-calculated)