<properties 
    pageTitle="OpenCensus SDK with Application Insights for Python"
    description="OpenCensus SDK with Application Insights for Python"
    service="microsoft.insights"
    resource="components"
    authors="lzchen"
    ms.author="lechin"
    articleId="insights_python"
    displayOrder="1125"
    selfHelpType="generic"
    cloudEnvironments="public"
    productPesIds="15693" 
    supportTopicIds=""
/>
# **OpenCensus SDK with Application Insights for Python**<br>

Application Insights now supports distributed tracing of Python applications through integration with [OpenCensus](https://opencensus.io/). Instrument your Python applications with OpenCensus Python SDK and appropriate extensions to send logs, metrics and traces to the desired ingestion service. Install the [OpenCensus Python Azure Extension](https://pypi.org/project/opencensus-ext-azure/) to begin sending data to Application Insights.


## **Getting Started**<br>

1. Follow [these instructions](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python) to see how to setup and instrument your application to send traces to Application Insights. Take a look at the [Github page](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib/opencensus-ext-azure) for more detailed instructions.
2. See our [GitHub examples](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib/opencensus-ext-azure/examples) for more advanced usages of the Opencensus Azure exporters
3. Make sure your application is running a [version](https://github.com/census-instrumentation/opencensus-python/blob/master/setup.py) of Python that is supported by OpenCensus
4. There are several things you can [customize](https://github.com/census-instrumentation/opencensus-python/blob/master/README.rst#customization) in OpenCensus

## **Troubleshooting**<br>
1. For issues related with [ApplicationInsights-Python SDK](https://github.com/microsoft/ApplicationInsights-Python), please note that the SDK is not supported or maintained by Microsoft. We recommend checking out [Python OpenCensus SDK](https://github.com/census-instrumentation/opencensus-python) for Application Insight's latest Python investments.
2. For issues where you cannot see your telemetry in Application Insights, see [this FAQ](#I-am-not-seeing-any-telemetry-show-up-in-my-Application-Insights-instance).
3. See the rest of the common problems and solutions below and a list of open [Github issues](https://github.com/census-instrumentation/opencensus-python/issues)
4. Create a ticket or file a [bug report](https://github.com/census-instrumentation/opencensus-python/issues/new?labels=bug&template=bug_report.md). Please provide as much information about your environment as possible such as which version of Python is being used (python --version), what platform you are running on, version numbers of installed dependencies, a callstack, and a code snippet to reproduce if possible.

[I am not seeing any telemetry show up in my Application Insights instance]: #I-am-not-seeing-any-telemetry-show-up-in-my-Application-Insights-instance

## **I am not seeing my application's telemetry in Application Insights**<br>
If you are not seeing your telemetry in your instance of Application Insights in the Portal: <br>
1. Wait for 10-20 minutes to make sure that the lack of data is not due to ingestion delay (it takes about that long for sent telemetry data to appear on Azure Monitor)
2. Make sure that the instrumentation key you specified in the <b>APPINSIGHTS_INSTRUMENTATIONKEY</b> environment variable or in your code corresponds to the Application Insights instance you are viewing. The key specified in your code takes precedence over the one specified in the environment variable.
3. Take a look at the output for your logs for any failed telemetry items.

## **Does OpenCensus support X version of Y?**<br>
Take a look at [extension packages](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib) to see if OpenCensus supports the extension that you need. Go to the corresponding (setup.py) file to see what the latest supported version is. The list of integrations can be found at the bottom of [this FAQ](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python) 

## **I want to send telemetry to other ingestion endpoints**<br>
Take a look at the [extension packages](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib) to see what other exporters that OpenCensus supports.

## **What out-of-the-box metrics are available immediately when instrumenting with OpenCensus Azure?**<br>
As of today, important system metrics such as CPU usage, memory usage, and requests/sec, outgoing HTTP requests using the [requests](https://2.python-requests.org/en/master/) library as well as incoming HTTP requests using [http.server](https://docs.python.org/3/library/http.server.html) for Python3 and [BaseHTTPServer](https://docs.python.org/2/library/basehttpserver.html) for Python2.
