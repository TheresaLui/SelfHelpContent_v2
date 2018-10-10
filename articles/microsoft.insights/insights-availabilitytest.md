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

1. Check the [FAQ](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-web-app-availability#qna) for answers to common questions.
2. Verify you have the test running in multiple geo-locations
  * If not, it’s strongly recommended to run at least from two locations. Web communication fails for multiple reasons from time to time. Having only 1 location enabled will considerably increase the likelihood of false-positives.
3. Check server side logs for the failure, especially if the answer to #2 is yes.
4. Determine if the issue present in all geo-locations
5. Verify the issue intermittent or persistent. 
  * If so, is it possible the URL being tested hits a load balancer, with multiple machines serving the request. In this case, do all machines have the same exact configuration?
6. Do you have parse-dependent requests enabled?
  * If so, it’s possible the issue is being caused by a dependent resource provider (e.g. CDN’s). 
  * Have you investigated that possibility?
7. Ping tests will follow redirects (configurable for multi-step). 
  * Is it possible the redirect is failing.

**Please provide following information to help the team investigate issue**

1. The name of the availability test
2. Is the test running in multiple geo-locations? 
3. Is the issue present in all geo-locations?
4. Is the issue intermittent?

**Known issues**

1. You cannot create more than 10 tests inside of the UI. You must use [PowerShell](https://docs.microsoft.com/azure/application-insights/app-insights-powershell#add-an-availability-test) if you need more. This is by design.

## **Recommended Documents**
[Availability Tests](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-web-app-availability)<br/>
[Automation](https://docs.microsoft.com/azure/application-insights/app-insights-powershell#add-an-availability-test)