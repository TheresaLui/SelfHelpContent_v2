<properties 
    pageTitle="I am having problems with my Availability Tests"
    description="General troubleshooting guide for Availability Tests."
    infoBubbleText="Some suggestions have been found to help solve your availability test issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    articleId="insights_availabilitytests"
    displayOrder="8"
    selfHelpType="generic"
    cloudEnvironments="public"
    productPesIds="15693" 
    supportTopicIds="32422336"
 />
# I am having problems with my Availability Tests
## **Recommended Steps**

1. Check the [FAQ](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-web-app-availability#qna) for answers to common questions
2. Verify you have the test running in multiple geo-locations. It is strongly recommended to run at least from two locations. Web communication fails for multiple reasons from time to time and having only one location enabled will considerably increase the likelihood of false positives
3. Check server side logs for the failure, especially if the answer to #2 is yes
4. Determine if the issue present in all geo-locations
5. Verify if you're using a load balancer and that all the machines behind the load balancer have the same configuration
6. If you have parse-dependent requests enabled the issue could be caused by a dependent resource provider (e.g. CDN’s)
7. Please validate that the redirect is not failing

**Please provide following information to help the team investigate issue**

1. The name of the availability test
2. Is the test running in multiple geo-locations? 
3. Is the issue present in all geo-locations?
4. Is the issue intermittent?

**Known issues**

1. You cannot create more than 10 tests inside of the UI. You must use [PowerShell](https://docs.microsoft.com/azure/application-insights/app-insights-powershell#add-an-availability-test) if you need more. This is by design.

## **Recommended Documents**
[Availability Tests](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-web-app-availability)<br>
[Automation](https://docs.microsoft.com/azure/application-insights/app-insights-powershell#add-an-availability-test)