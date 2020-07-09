<properties 
    pageTitle=" Availability test doesn't detect when my website is down"
    description=" Availability test doesn't detect when my website is down"
    infoBubbleText="Some suggestions have been found to help solve your availability test issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author = "casocha"
    articleId="availability-test-doesnt-detect-website-down"
    displayOrder="8"
    selfHelpType="generic"
    cloudEnvironments="public, mooncake, blackforest, fairfax, usnat, ussec"
    productPesIds="15693"
    supportTopicIds="32729575"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# My website is down but my availability tests aren't failing

You have determined that your website is down, yet the availability web test is not failing (e.g. you see no red dots in the availability charts)

## **Recommended Steps**

Check that your response code is equal to 200:
Ensure the Success Criteria for your web test is what you expect it to be. By default, a ping test succeeds if the response code is equal to 200. If you have modified that value or specified a value for content matching, ensure it is what you intended to do.

 ![Test image](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/websitedownpic1.jpg)

My website has multiple instances that are geographically distributed:
If so, are all instances down? If not, then it is possible the availability test is pinging a "healthy" instance.  

Check if you are running tests from at least 5 different locations:
Ensure you select at least 5 locations from where the availability test should run to get maximum coverage and avoid transient hiccups.

My website is down & the availability test is failing but I'm not being notified:
Ensure your web test alerts are properly configured. Check the following [link](https://docs.microsoft.com/azure/azure-monitor/app/availability-alerts).

## Known issues

You cannot create more than 10 tests inside of the UI. You must use [PowerShell](https://docs.microsoft.com/azure/application-insights/app-insights-powershell#add-an-availability-test) if you need more. This is by design.

## **Recommended Documents**

* [Availability Tests](https://docs.microsoft.com/azure/application-insights/app-insights-monitor-web-app-availability)
* [Automation](https://docs.microsoft.com/azure/application-insights/app-insights-powershell#add-an-availability-test)
* [IP Address Used by Availability Tests](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#availability-tests)
