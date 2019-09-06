# **Configuring OpenCensus Python**<br>

Follow [these instructions](https://docs.microsoft.com/azure/azure-monitor/app/opencensus-python) to see how to setup and instrument your application to send traces to Application Insights. Take a look at the [Github page](https://github.com/census-instrumentation/opencensus-python/tree/master/contrib/opencensus-ext-azure) for more detailed instructions.

## Versioning
1. Make sure your application is running a [version](https://github.com/census-instrumentation/opencensus-python/blob/master/setup.py) of Python that is supported by OpenCensus
2. Upgrade to the latest version of [opencensus-ext-azure](https://pypi.org/project/opencensus-ext-azure/)

## Instrumentation Key
1. Make sure that the instrumentation key you specified in the <b>APPINSIGHTS_INSTRUMENTATIONKEY</b> environment variable or in your code corresponds to the Application Insights instance you are viewing. The key specified in your code takes precedence over the one specified in the environment variable.

## Unable to see telemetry in Application Insights

### Tracing
1. Make sure your AzureExporter specifies a sampler with a sampling rate between 0.0 and 1.0 inclusive.
`tracer = Tracer(
    exporter=AzureExporter(
        instrumentation_key='00000000-0000-0000-0000-000000000000',
    ),
    sampler=ProbabilitySampler(1.0),
)`

#### If using opencensus-ext-flask
1. Make sure you have the latest version of [opencensus-ext-flask](https://pypi.org/project/opencensus-ext-flask/)
2. Check to see if the host(s) your are making requests to are not in settings.py under BLACKLIST_HOSTNAMES.
3. Check to see if the path(s) your are making requests to are not in settings.py under BLACKLIST_PATHS.

#### If using opencensus-ext-django
1. Make sure you have the latest version of [opencensus-ext-django](https://pypi.org/project/opencensus-ext-django/)
2. Make sure you have `'opencensus.ext.django.middleware.OpencensusMiddleware'` in your settings.py file under MIDDLEWARE.
3. Make sure AzureExporter is properly configured in your settings.py under OPENCENSUS.
`OPENCENSUS = {
    'TRACE': {
        'SAMPLER': 'opencensus.trace.samplers.ProbabilitySampler(rate=0.5)',
        'EXPORTER': '''opencensus.ext.azure.trace_exporter.AzureExporter(
            service_name='foobar',
        )''',
    }
}`
4. Check to see if the host(s) your are making requests to are not in settings.py under BLACKLIST_HOSTNAMES.
5. Check to see if the path(s) your are making requests to are not in settings.py under BLACKLIST_PATHS.

### Metrics
1. Metrics with type DistributionAggregation in their views are not supported to be exported.
`CARROTS_MEASURE = measure_module.MeasureInt("carrots",
                                            "number of carrots",
                                            "carrots")
CARROTS_VIEW = view_module.View("carrots_view",
                                "number of carrots",
                                [],
                                CARROTS_MEASURE,
                                aggregation_module.DistributionAggregation())`

4. There are several things you can [customize](https://github.com/census-instrumentation/opencensus-python/blob/master/README.rst#customization) in OpenCensus


