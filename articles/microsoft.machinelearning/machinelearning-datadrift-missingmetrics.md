<properties 
    pageTitle="Why are some or all drift metrics missing?"
    description="Why are some or all drift metrics missing?"
    service="microsoft.machinelearning"
    resource="datadrift"
    authors="WeiLengUSC"
    ms.author="kicha"
    selfHelpType="generic"
    supportTopicIds="32690851"
    resourceTags=""
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
 	articleId="machinelearning-datadrift-missingmetrics"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Why are some or all drift metrics missing?

There are three common reasons why some or all drift metrics are not available. The following steps below can help you identify the reason drift metrics are not available after a monitor is set up and running.

## Common reasons for missing drift metrics

### Missing or insufficient input data

Please check that new data for your target dataset are ingested correctly to configured storage location defined during dataset creation and that the latest data contains sufficient amount of data. Please see the recommended documents about minimum data requirement.

### Incorrect schedule delay setting

If the delay from which your data are ingested to azure has increased, the delay for schedule job trigger should be updated as a job that is triggered prematurely do not have access to data that do not exist yet. Please see the recommended documents about updating delay.

### Missing features

Your latest data may be missing some or all features that are initially configured for monitoring. No metrics can be generated for the missing features column.

## **Recommended Documents**

* [Detect data drift on datasets](https://docs.microsoft.com/azure/machine-learning/how-to-monitor-datasets)<br>
