<properties 
    pageTitle="My Availability tests are failing in a couple regions"
    description="My Availability tests are failing in a couple regions"
    infoBubbleText="Some suggestions have been found to help solve your availability test issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author = "casocha"
    articleId="availability-tests-failing-in-few-regions"
    displayOrder="8"
    selfHelpType="generic"
    cloudEnvironments="public, mooncake, blackforest, fairfax, usnat, ussec"
    productPesIds="15693"
    supportTopicIds="32729577"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# My Availability tests are failing in a couple regions

You may notice that, while your availability test is running successfully in most regions, you are receiving failures in one or a few. This could be caused by misconfigurations of load balancers, traffic managers or firewalls. It may also be indicative of issues in your application, particularly if it is deployed to multiple geographical regions. You can verify this by opening one of the failed test results and checking if the message contains a phrase similar to "A connection attempt failed because the connected party did not properly respond after a period of time".

## **Recommended Steps**

My application is behind a firewall:
Make sure you have whitelisted all of the [IP Addresses](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#availability-tests) used by Availability Tests. Rerouting of certain IP addresses may be occurring via Load Balancers, Geo traffic managers, Azure Express Route.

I am using Azure Express Route:
There are scenarios where packets can be dropped in cases where [Asymmetric Routing](https://docs.microsoft.com/azure/expressroute/expressroute-asymmetric-routing) occurs.

I am using a load balancer:
If you're using a load balancer then verify that all the machines behind the load balancer have the same configuration.

I am using a CDN or Geo traffic manager:
If you have parse-dependent requests enabled then the issue could be caused by a dependent resource provider (e.g. CDN’s).

If none of these steps resolved your issue:
* Check server-side logs for the failure
* Please validate that the redirect is not failing

## **Recommended Documents**

* [Availability Tests](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-web-app-availability)
* [IP Address Used by Availability Tests](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#availability-tests)
