<properties
	pageTitle="I am having issues trying to create, edit or delete availability test alert rules in the Azure portal"
	description="I'm trying to create, edit or delete an availability test alert rule in the Azure portal, but I'm getting an error, or I don't know how to configure it"
	infoBubbleText=""
	service="microsoft.insights"
	resource="alertrules"
	authors="harelbr"
	ms.author="harelbr"
	displayOrder="8"
	articleId="alerts-crud-ui-webtest"
	selfHelpType="generic"
	supportTopicIds="32739774,32739812,32739813"
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_Alerts_ActivityLogAndMetricAlerts"
/>

# I am having issues trying to create, edit or delete classic metric alert rules in the Azure portal

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
