<properties 
    pageTitle="Configuring OpenCensus Python"
    description="Configuring OpenCensus Python"
    service="microsoft.insights"
    resource="components"
    authors="lzchen"
    ms.author="lechin"
    articleId="insights_python"
    displayOrder="1125"
    selfHelpType="resource"
    cloudEnvironments="public"
    productPesIds="15693" 
    supportTopicIds="32681426"
/>
# **Configuring OpenCensus Python**<br>

Follow [these instructions](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python) to see how to setup and instrument your application to send traces to Application Insights. Take a look at the [Github page](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib/opencensus-ext-azure) for more detailed instructions.

## Versioning
1. Make sure your application is running a [version](https://github.com/census-instrumentation/opencensus-python/blob/master/setup.py) of Python that is supported by OpenCensus
2. Upgrade to the latest version of [opencensus-ext-azure](https://pypi.org/project/opencensus-ext-azure/)

## Instrumentation Key
1. Make sure that the instrumentation key you specified in the <b>APPINSIGHTS_INSTRUMENTATIONKEY</b> environment variable or in your code corresponds to the Application Insights instance you are viewing. The key specified in your code takes precedence over the one specified in the environment variable.

## No data is collected

### Tracing
1. Make sure your AzureExporter specifies a sampler with a sampling rate between 0.0 and 1.0 inclusive.
```
tracer = Tracer(
    exporter=AzureExporter(
        instrumentation_key='00000000-0000-0000-0000-000000000000',
    ),
    sampler=ProbabilitySampler(1.0),
)
```

#### If using opencensus-ext-flask integration
1. Make sure you have the latest version of [opencensus-ext-flask](https://pypi.org/project/opencensus-ext-flask/)
2. Check to see if the host(s) your are making requests to are not in settings.py under BLACKLIST_HOSTNAMES.
3. Check to see if the path(s) your are making requests to are not in settings.py under BLACKLIST_PATHS.

#### If using opencensus-ext-django integration
1. Make sure you have the latest version of [opencensus-ext-django](https://pypi.org/project/opencensus-ext-django/)
2. Make sure you have `'opencensus.ext.django.middleware.OpencensusMiddleware'` in your settings.py file under MIDDLEWARE.
3. Make sure AzureExporter is properly configured in your settings.py under OPENCENSUS.
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
4. Check to see if the host(s) your are making requests to are not in settings.py under BLACKLIST_HOSTNAMES.
5. Check to see if the path(s) your are making requests to are not in settings.py under BLACKLIST_PATHS.

#### If using opencensus-ext-httplib integration
1. Make sure `config_integration.trace_integrations(['httplib'])` is included in your code.
2. Check to see if the host(s) your are making requests to are not in set in `blacklist_hostnames`.
3. If using Python2, [httplib](https://docs.python.org/2/library/httplib.html) is the supported library. If using Python3,
[http.client](https://docs.python.org/3/library/http.client.html) is the supported library.

### Metrics
1. Metrics with type DistributionAggregation in their views are not supported to be exported.
```
CARROTS_MEASURE = measure_module.MeasureInt("carrots",
                                            "number of carrots",
                                            "carrots")
CARROTS_VIEW = view_module.View("carrots_view",
                                "number of carrots",
                                [],
                                CARROTS_MEASURE,
                                aggregation_module.DistributionAggregation())
```

# **Recommended Documents**<br>

* [Getting Started](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python)
* [OpenCensus Azure Monitor Exporter](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib/opencensus-ext-azure)



