<properties 
    pageTitle="I am having problems with my Availability Tests"
    description="General troubleshooting guide for Availability Tests."
    infoBubbleText="Some suggestions have been found to help solve your availability test issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author = "jamdavi"
    articleId="insights_availabilitytests"
    displayOrder="8"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693,15454" 
    supportTopicIds="32422336,32630726,32630727,32630728,32630729,32630730,32630732,32630733,32630734"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I am having problems with my Availability Tests

## **Recommended Steps**

1. Check the [Troubleshooting Guide](https://docs.microsoft.com/azure/azure-monitor/app/troubleshoot-availability) for answers to common questions
2. Make sure you have whitelisted all of the [IP Address Used by Availability Tests](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#availability-tests)
3. Verify you have the test running in multiple geo-locations. It is strongly recommended to run at least from two locations. Web communication fails for multiple reasons from time to time and having only one location enabled will considerably increase the likelihood of false positives
4. Check server side logs for the failure, especially if the answer to #3 is yes
5. Determine if the issue present in all geo-locations
6. Verify if you're using a load balancer and that all the machines behind the load balancer have the same configuration
7. If you have parse-dependent requests enabled the issue could be caused by a dependent resource provider (e.g. CDN’s)
8. Please validate that the redirect is not failing

**Known issues**<br>

You cannot create more than 10 tests inside of the UI. You must use [PowerShell](https://docs.microsoft.com/azure/application-insights/app-insights-powershell#add-an-availability-test) if you need more. This is by design.

## **Recommended Documents**

* [Availability Tests](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-web-app-availability)<br>
* [Automation](https://docs.microsoft.com/azure/application-insights/app-insights-powershell#add-an-availability-test)<br>
* [IP Address Used by Availability Tests](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#availability-tests)<br>
