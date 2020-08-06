<properties 
    pageTitle="I am having problems with setting up node.js"
    description="General troubleshooting guide for the node.js SDK."
    infoBubbleText="Some suggestions have been found to help solve your node.js issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="markwolff"
    ms.author="marwolff"
    articleId="insights_nodejs"
    displayOrder="1134"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32632985, 32632999"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Application Insights for Node.js

Add this SDK to your Node.js services to include deep info about Node.js processes and their external dependencies such as database and cache services. You can use this SDK for your Node.js services hosted anywhere: your datacenter, Azure VMs and Azure Web Apps, and even other public clouds.

This library tracks the following out-of-the-box:

- Incoming and outgoing HTTP requests
- Important system metrics such as CPU usage, memory usage, and requests/sec
- Unhandled exceptions
- Events from many popular third-party libraries ([GitHub: see supported third-party libraries](https://github.com/microsoft/applicationinsights-node.js#automatic-third-party-instrumentation))

### Getting Started

1. Create an Application Insights resource in Azure by following [these instructions](https://docs.microsoft.com/azure/application-insights/app-insights-nodejs)
2. Grab the _Instrumentation Key_ (aka "ikey") from the resource you created in step 1. Later, you'll either add it to your app's environment variables or use it directly in your scripts.
3. Add the Application Insights Node.js SDK to your app's dependencies and package.json:

     ```
     npm install --save applicationinsights
     ```
     *Note:* If you're using TypeScript, do not install a separate "typings" package. This NPM package contains built-in typings.

4. As early as possible in your app's code, load the Application Insights package:

     ```
     let appInsights = require('applicationinsights');
     ```

5. Configure the local SDK by calling `appInsights.setup('_your_ikey_');` using the ikey you grabbed in step 2, or put this ikey in the **APPINSIGHTS_INSTRUMENTATIONKEY** environment variable and call **appInsights.setup()** without parameters.
6. Finally, start automatically collecting and sending data by calling `appInsights.start();`
7. For advanced configuration see our [GitHub Readme](https://github.com/microsoft/applicationinsights-node.js#configuration)

## **Recommended Steps**

1. Update to the latest version of the Node.js SDK. SDK version should be greater than 1.1.0, which is when SDK was changed to use async_hooks API for correlation.
2. If issue relates to app insights crashing the app or showing up on the top of your callstack, see **Application Insights is causing my application to crash** below. Be sure issue is not reproducible if app insights is not present in your application.
3. For issues where certain telemetry is not being automatically collected, see **Telemetry is not being collected** below
3. If the app is crashing because of application insights, try disabling automatic dependency correlation: `.setAutoDependencyCorrelation(false)`
4. If the app is hanging when it should terminate, disable disk retry caching: `.setDiskRetryCaching(false)` or call `appInsights.flush()` when you expect
5. See rest of FAQs below and the list of open [GitHub issues](https://github.com/microsoft/applicationinsights-node.js/issues)
6. Create a ticket or file a [bug report](https://github.com/microsoft/ApplicationInsights-node.js/issues/new). Please provide which version of the SDK being used, which version of node.js being used (**node --version**), a **package.json** file, a callstack, and a code snippet to reproduce, if possible.

### **I am not seeing any telemetry show up in my Application Insights instance**<br>

If you are not seeing your telemetry in your instance of Application Insights in the Portal:

1. Wait for 10-20 minutes to make sure that the lack of data is not due to ingestion delay
2. Try flushing your telemetry with a callback provided to see if the telemetry was accepted by the ingestion server:

     ```
     appInsights.flush({ callback: (res) => {
          console.log(res); // ItemsAccepted should equal ItemsReceived
     }});
     ```

3. File a ticket or [bug report]

### **I am missing telemetry when my app terminates**<br>

By default, the SDK tries to not prevent your application from terminating (e.g. in a Azure Function App), so if you expect your application to terminate (but not from an exception), you should try to flush the SDK's buffers to prevent any gaps in telemetry:

```
appInsights.flush();
```

### **Application Insights is causing my application to crash**<br>

Please note that when your app crashes, we "rethrow" your error so that we can send telemetry about it and still let your app crash as usual. This causes the SDK to show on the top of your call stack when debugging, even if the crash originated elsewhere in your app. However, we remove ourselves from your call stack in the resulting telemetry.

If removing app insights from your application resolves the crashes, you can try the following:

 1. Upgrade to the latest version of the SDK. Version **1.1.0** fixed a majority of the stability issues with the SDK. Any version prior to this will have stability issues related to dependency correlation.
 2. Disable automatic dependency correlation via **.setAutoDependencyCorrelation(false)**. This will turn off dependency correlation between your applications incoming/outgoing requests.
 3. File a ticket or [bug report]

### **A 3rd party library is not being tracked**<br>

A list of the 3rd party libraries & versions that we support native tracking of is [here](https://github.com/Microsoft/node-diagnostic-channel/blob/master/src/diagnostic-channel-publishers/README.md). If it is not on this list, you may still get tracking of it via our tracking of incoming/outgoing http/s requests, if the library uses it. If the (npm) version of the library you are using is not being automatically tracked, and you are using the latest version of the Application Insights Node.js SDK, please file a ticket or [bug report](https://github.com/microsoft/ApplicationInsights-node.js/issues/new).

### **Telemetry is not being collected**<br>

Make sure that app insights is the first thing that is required into the application. If anything else is required first, e.g. **https** module, or some 3rd party library, then we will not be able to collect telemetry on it.

```
var appInsights = require('applicationinsights'); // this should be the first line of code run in your application, if possible
```

## **Recommended Documents**

* [How can I preprocess or filter my telemetry before it gets sent to Azure?](https://github.com/microsoft/applicationinsights-node.js#preprocess-data-with-telemetry-processors)<br>
* [How do I enable Live Metrics Streaming?](https://github.com/microsoft/applicationinsights-node.js#live-metrics)<br>
* [How can I send my own custom telemetry?](https://github.com/microsoft/applicationinsights-node.js#track-custom-telemetry)<br>
* [How do I enable W3C compatible distributed tracing in my application?](https://github.com/microsoft/applicationinsights-node.js#distributed-tracing-modes)<br>
* [How can I send Node.js specific metrics about my application?](https://github.com/microsoft/applicationinsights-node.js#extended-metrics)<br>
