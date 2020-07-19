<properties 
    pageTitle="Configuring OpenCensus Python"
    description="Configuring OpenCensus Python"
    service="microsoft.insights"
    resource="components"
    authors="lzchen"
    ms.author="lechen"
    articleId="insights_python_data"
    displayOrder="1126"
    selfHelpType="resource"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds=""
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# No data or Partial data with OpenCensus Python

## No data/partial data

1. Make sure OpenCensus Python is [configured properly](https://github.com/census-instrumentation/opencensus-python/blob/master/contrib/opencensus-ext-azure/README.rst)
2. Wait for ~5 minutes to make sure that the lack of data is not due to ingestion delay (it takes about that long for sent telemetry data to appear on Azure Monitor)
3. Take a look at the output for your logs for any failed telemetry items. Local log files are stored in your local file system. The default storage path is `$HOME\.opencensus\.azure\{FILENAME}`. At the time of writing this document, only request, dependency, trace and exception telemetry will have logs for failed telemetry.

### What core and third party libraries can I monitor by instrumenting with OpenCensus?

1. The core [OpenCensus library](https://pypi.org/project/opencensus/)
2. The [OpenCensus Azure Monitor Exporters](https://pypi.org/project/opencensus-ext-azure/)
2. The OpenCensus [official integrations](https://github.com/census-instrumentation/opencensus-python#integration) to see the list of integrations

### I'm not seeing metric X out-of-the-box
As of today, important system metrics such as CPU usage, memory usage, and requests/sec, outgoing HTTP requests using the [requests](https://pypi.org/project/requests/) library as well as incoming HTTP requests using [http.server](https://docs.python.org/3/library/http.server.html) for Python3 and [BaseHTTPServer](https://docs.python.org/2/library/basehttpserver.html) for Python2.

If you do not find your solution from this page, create a ticket or file a [bug report](https://github.com/census-instrumentation/opencensus-python/issues/new?labels=bug&template=bug_report.md). Please provide which version of Python is being used (python --version), what platform you are running on, version numbers of installed dependencies, a callstack, and a code snippet to reproduce if possible.

## **Recommended Documents**

* [Getting Started](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python)
* [OpenCensus Azure Monitor Exporters](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib/opencensus-ext-azure)
