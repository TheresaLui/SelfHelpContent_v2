<properties 
    pageTitle="Configuring OpenCensus Python"
    description="Configuring OpenCensus Python"
    service="microsoft.insights"
    resource="components"
    authors="lzchen"
    ms.author="lechin"
    articleId="insights_python"
    displayOrder="1126"
    selfHelpType="resource"
    cloudEnvironments="public"
    productPesIds="15693" 
    supportTopicIds=""
/>
# No data or Partial Data with OpenCensus Python

## No data/partial data

1. Make sure OpenCensus Python is [configured properly]()
2. Wait for ~5 minutes to make sure that the lack of data is not due to ingestion delay (it takes about that long for sent telemetry data to appear on Azure Monitor)
3. Take a look at the output for your logs for any failed telemetry items.

## Does OpenCensus support X version of Y?
Take a look at [extension packages](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib) to see if OpenCensus supports the extension that you need. Go to the corresponding (setup.py) file to see what the latest supported version is. The list of integrations can be found at the bottom of [this FAQ](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python)

## I'm not seeing metric X out-of-the-box
As of today, important system metrics such as CPU usage, memory usage, and requests/sec, outgoing HTTP requests using the [requests](https://2.python-requests.org/en/master/) library as well as incoming HTTP requests using [http.server](https://docs.python.org/3/library/http.server.html) for Python3 and [BaseHTTPServer](https://docs.python.org/2/library/basehttpserver.html) for Python2.

If you do not find your solution from this page, create a ticket or file a [bug report](https://github.com/census-instrumentation/opencensus-python/issues/new?labels=bug&template=bug_report.md). Please provide which version of Python is being used (python --version), what platform you are running on, version numbers of installed dependencies, a callstack, and a code snippet to reproduce if possible.

## **Recommended Documents**<br>

* [Getting Started](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python)
* [OpenCensus Azure Monitor Exporter](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib/opencensus-ext-azure)
