<properties 
    pageTitle="Configuring OpenCensus Python"
    description="Configuring OpenCensus Python"
    service="microsoft.insights"
    resource="components"
    authors="lzchen"
    ms.author="lechen,neghuman"
    articleId="insights_python_configure"
    displayOrder="1125"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32681426"
    ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Configuring OpenCensus Python

## **Recommended Steps**

Follow [these instructions](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python) to see how to setup and instrument your application to send traces to Application Insights. Take a look at the [README](https://github.com/census-instrumentation/opencensus-python/blob/master/contrib/opencensus-ext-azure/README.rst) for more detailed instructions.

## Versioning

1. Make sure your application is running a [version](https://github.com/census-instrumentation/opencensus-python/blob/master/setup.py#L32-L38) of Python that is supported by OpenCensus
2. Upgrade to the latest version of [opencensus-ext-azure](https://pypi.org/project/opencensus-ext-azure/)

### Instrumentation Key

1. Make sure that the instrumentation key you specified in the `APPINSIGHTS_INSTRUMENTATIONKEY` environment variable or in your code corresponds to the Application Insights instance you are viewing. The key specified in your code takes precedence over the one specified in the environment variable.

## No data is collected

### Tracing

1. You may specify a `sampler` as part of your `Tracer` configuration. If no explicit sampler is provided, the [ProbabilitySampler will be used by default](https://github.com/census-instrumentation/opencensus-python/blob/2457a87165bbe3951ae48a2a56c2177d7f277be2/opencensus/trace/tracer.py#L52). The `ProbabilitySampler` would use a [rate of 1/10000 by default](https://github.com/census-instrumentation/opencensus-python/blob/2457a87165bbe3951ae48a2a56c2177d7f277be2/opencensus/trace/samplers/__init__.py#L16), meaning one out of every 10000 requests will be sent to Application Insights. If you want to specify a sampling rate, see below.
2. When specifying a sampler, make sure your `Tracer` specifies a sampler with a sampling rate between 0.0 and 1.0 inclusive. A sampling rate of 1.0 represents 100%, meaning all of your requests will be sent as telemetry to Application Insights:

```
tracer = Tracer(
    exporter=AzureExporter(
        instrumentation_key='00000000-0000-0000-0000-000000000000',
    ),
    sampler=ProbabilitySampler(1.0),
)
```

### If using opencensus-ext-flask integration

1. Make sure you have the latest version of [opencensus-ext-flask](https://pypi.org/project/opencensus-ext-flask/)
2. Check to see if the requests originating from the url(s) are not in settings.py under `BLACKLIST_PATHS`:

```
app.config['OPENCENSUS'] = {
    'TRACE': {
        'SAMPLER': 'opencensus.trace.samplers.ProbabilitySampler(rate=1)',
        'EXPORTER': '''opencensus.ext.azure.trace_exporter.AzureExporter(
            service_name='foobar',
        )''',
        'BLACKLIST_PATHS': 'https://example.com',  <--- This site will not be traced if a request is sent to it.
    }
}
```

### If using opencensus-ext-django integration

1. Make sure you have the latest version of [opencensus-ext-django](https://pypi.org/project/opencensus-ext-django/)
2. Make sure you have `'opencensus.ext.django.middleware.OpencensusMiddleware'` in your settings.py file under `MIDDLEWARE`:

```
MIDDLEWARE = (
    ...
    'opencensus.ext.django.middleware.OpencensusMiddleware',
    ...
)
```

3. Make sure AzureExporter is properly configured in your settings.py under `OPENCENSUS`:

```
OPENCENSUS = {
    'TRACE': {
        'SAMPLER': 'opencensus.trace.samplers.ProbabilitySampler(rate=0.5)',
        'EXPORTER': '''opencensus.ext.azure.trace_exporter.AzureExporter(
            service_name='foobar',
        )''',
    }`
}
```

4. Check to see if the requests originating from the url(s) are not in settings.py under `BLACKLIST_PATHS`:

```
OPENCENSUS = {
    'TRACE': {
        'SAMPLER': 'opencensus.trace.samplers.ProbabilitySampler(rate=0.5)',
        'EXPORTER': '''opencensus.ext.azure.trace_exporter.AzureExporter(
            service_name='foobar',
        )''',
        'BLACKLIST_PATHS': 'https://example.com',  <--- This site will not be traced if a request is sent from it.
    }`
}
```

### If using opencensus-ext-httplib integration

1. Make sure `config_integration.trace_integrations(['httplib'])` is included in your code
2. Check to see if the url(s) your are making requests to are not in set in `blacklist_hostnames`:

```
from opencensus.trace import config_integration, execution_context
...
config_integration.trace_integrations(['httplib'])
execution_context.set_opencensus_attr(
    'blacklist_hostnames',
    ['https://example.com']  <--- This site will not be traced if a request is sent to it.
)
...

```

3. If using Python2, [httplib](https://docs.python.org/2/library/httplib.html) is the supported library. If using Python3,
[http.client](https://docs.python.org/3/library/http.client.html) is the supported library.

### If using opencensus-ext-requests integration

1. Make sure `config_integration.trace_integrations(['requests'])` is included in your code
2. Check to see if the url(s) your are making requests to are not in set in `blacklist_hostnames`:

```
from opencensus.trace import config_integration, execution_context
...
config_integration.trace_integrations(['requests'])
execution_context.set_opencensus_attr(
    'blacklist_hostnames',
    ['https://example.com']  <--- This site will not be traced if a request is sent to it.
)
...

```

3. Only requests using the [requests](https://pypi.org/project/requests/) library will be tracked.

### Metrics

1. Metrics with type `DistributionAggregation` in their views are not supported to be exported:

```
CARROTS_MEASURE = measure_module.MeasureInt("carrots",
                                            "number of carrots",
                                            "carrots")
CARROTS_VIEW = view_module.View("carrots_view",      <--- Any metric from this view will not be tracked
                                "number of carrots",
                                [],
                                CARROTS_MEASURE,
                                aggregation_module.DistributionAggregation())  <-- DistributionAggregation()
```

If you do not find your solution from this page, create a ticket or file a [bug report](https://github.com/census-instrumentation/opencensus-python/issues/new?labels=bug&template=bug_report.md).

## **Recommended Documents**

* [Getting Started](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python)
* [OpenCensus Azure Monitor Exporters](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib/opencensus-ext-azure)
