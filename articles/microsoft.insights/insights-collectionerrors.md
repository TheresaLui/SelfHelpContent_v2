<properties 
    pageTitle="I am seeing errors or latency with telemetry collection"
    description="I am seeing errors or latency with telemetry collection"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights_collectionerrors"
    displayOrder="101"
    selfHelpType="generic"
    supportTopicIds="32546624"
    productPesIds="15693"
    cloudEnvironments="public"
 />
# I am seeing errors or latency with telemetry collection

## **Recommended Steps**

**For Latency**<br>

Latency is expected in a highly distributed system. Our average latency is **15 minutes or less**. During outages or when we are experiencing other issues, it can be upwards of **an hour**. It is best to wait to see if the latency is persistent for more than an hour before attempting to open a ticket, as most latency issues are transient.<br>

1. Verify the version of the SDK you are using is up to date or a [supported version](https://github.com/Microsoft/ApplicationInsights-Home#officially-supported-sdks)  
2. Check the [Service Blog](https://blogs.msdn.microsoft.com/servicemap-status/) for latency warnings
3. Execute a comparable query in Analytics and compare it to the other screens, as it's possible the data latency is only during display
4. If the latency is persistent, it is recommended to open a case for tracking

**For Errors**<br>

For all supported SDKs you should not see any errors relating to telemetry collection. If you are seeing errors that are specific to **dc.services.visualstudio.com**, please use the steps below. If you are seeing other errors coming from your application, please go back and open a case for the SDK.

1. Verify the version of the SDK you are using is up to date or a [supported version](https://github.com/Microsoft/ApplicationInsights-Home#officially-supported-sdks)
2. Check the [Service Blog](https://blogs.msdn.microsoft.com/servicemap-status/) for warnings
3. If the errors are inside of your telemetry, please go back and open a case for the correct SDK
4. If you are receiving an error message from the service, it is likely that we are experiencing issues and it is recommended to open a case for tracking

## **Recommended Documents**

* [Service Blog](https://blogs.msdn.microsoft.com/servicemap-status/)
