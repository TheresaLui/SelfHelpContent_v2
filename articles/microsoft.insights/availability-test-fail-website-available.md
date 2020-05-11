<properties 
    pageTitle="My availability tests are failing but the website is still available"
    description="My availability tests are failing but the website is still available"
    infoBubbleText="Some suggestions have been found to help solve your availability test issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author = "casocha"
    articleId="availability-test-fail-website-available"
    displayOrder="8"
    selfHelpType="generic"
    cloudEnvironments="public, mooncake, blackforest, fairfax, usnat, ussec"
    productPesIds="15693"
    supportTopicIds="32729576"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>

# My availability tests are failing but the website is still available

I am seeing failures in Availability testing in Application Insights, but when I navigate to my website using a web browser, I don't see any errors.

## **Recommended Steps**

Click on an individual failing test result and examine the error message provided:

![Failed test](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/websiteavailablepic1.jpg)

![Failed test 2](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/websiteavailablepic2.jpg)

Check your error message.

A connection attempt failed because the connected party did not properly respond after a period of time:

A firewall could be blocking App Insights’ access to your website. Whitelist the [IP addresses used by App Insights](https://docs.microsoft.com/azure/azure-monitor/app/ip-addresses#availability-tests).

If your error is The server committed a protocol violation. Section=ResponseHeader Detail=CR must be followed by LF:
This occurs when malformed headers are detected. Specifically, some headers might not be using CRLF to indicate the end of line, which violates the HTTP specification. Application Insights enforces this HTTP specification and fails responses with malformed headers.

* Contact your website host provider or CDN provider to fix the faulty servers
* In the case that the failed requests are resources (e.g. style files, images, scripts), you may consider disabling the parsing of dependent requests. Keep in mind, if you do this you will lose the ability to monitor the availability of those files.

If your error is The Web test was stopped because it encountered an excessive number of exceptions while attempting to submit requests:
The main site may be available, but some dependent requests – images, stylesheets, and scripts – may not be loading properly.

* Check that all of the page resources are loading correctly using your browser’s DevTools
* To desensitize the test to such resource failures, simply uncheck the Parse Dependent Requests from the test configuration

If your error is Could not create SSL/TLS Secure Channel:
Check your SSL version. Only TLS 1.0, 1.1, and 1.2 are supported. SSLv3 is not supported.

If your error is Timeout (subtype 'Timeout') occured with the error 'Request timed out':
The test timed out. We abort tests after 2 minutes.  

* If it is a multi-step test, break the single test into multiple tests that can complete in shorter durations
* If it is a ping test, investigate your server-side logs to discover what server-side failures caused the site to time out

If you test from less than 5 locations:
Web communication fails for multiple reasons from time to time and having only one location enabled will considerably increase the likelihood of false positives. We recommend testing from at least 5 different locations.

![Failed test 3](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/websiteavailablepic3.jpg)

Retries are not set on my availability tests:
Some transient network issues may cause tests to fail. When retries are enabled, if the test fails, we’ll try it again after 20 seconds. We’ll record a failure only if it fails three times in a row.

![Failed test 4](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/websiteavailablepic3.jpg)

My alert threshold is less than 3 locations:
Web communication fails for multiple reasons from time to time and failing from only one location may increase the risk of false positives. We recommend setting an alert threshold of at least 3 locations.

![Failed test 5](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/websiteavailablepic4.jpg)

![Failed test 6](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/availability/websiteavailablepic5.jpg)

## **Recommended Documents**

* [Monitor Web App Availability](https://docs.microsoft.com/azure/azure-monitor/app/monitor-web-app-availability)
* [Multi-step Web Tests](https://docs.microsoft.com/azure/azure-monitor/app/availability-multistep)
* [Dealing with sign-in](https://docs.microsoft.com/azure/azure-monitor/app/availability-multistep#dealing-with-sign-in)
* [Troubleshoot Availability Testing](https://docs.microsoft.com/azure/azure-monitor/app/troubleshoot-availability)
* [Create and run custom Availability Tests using Azure Functions](https://docs.microsoft.com/azure/azure-monitor/app/availability-azure-functions)
* [Multi-step Web Test Pricing Information](https://azure.microsoft.com/pricing/details/monitor/)
