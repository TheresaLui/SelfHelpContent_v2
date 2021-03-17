<properties 
    pageTitle="Diagnose and resolve issues with Ganglia metrics" 
    description="Diagnose and resolve issues with Ganglia metrics" 
    service="microsoft.databricks" 
    resource="workspaces" 
    authors="lahaddad" 
    ms.author="lahaddad" 
    displayOrder="15" 
    selfHelpType="generic" 
    supportTopicIds="32784348" 
    resourceTags="" 
    productPesIds="16432" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="320d46bc-4ecf-48f2-bfa0-0e070d0227c1" 
    ownershipId="AzureData_AzureDatabricks" 
/> 


# Diagnose and resolve issues with Ganglia metrics 

## **Recommended Steps** 

* By default, Azure Databricks collects Ganglia metrics every 15 minutes. To configure the collection period, set the `DATABRICKS_GANGLIA_SNAPSHOT_PERIOD_MINUTES` environment variable by using an [init script](https://docs.microsoft.com/azure/databricks/clusters/init-scripts), or in the `spark_env_vars` field in the [Cluster Create API](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/clusters#clusterclusterservicecreatecluster). 

## **Recommended Documents** 

* Monitor the performance of Azure Databricks clusters using [Ganglia metrics](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#ganglia-metrics) 
* KB: [Cluster slowdown due to Ganglia metrics filling root partition](https://docs.microsoft.com/azure/databricks/kb/clusters/slowdown-from-root-disk-fill) 
